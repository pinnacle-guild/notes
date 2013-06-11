## Routing
We want to map the following URL patterns in a special manner.

# Pages
Direct the default view to the news page.
```php
Router::connect(
    '/',
    [
        'controller' => 'pages',
        'action'     => 'display',
        'news'
    ]
);
```

This will map the URL `/` to PagesController::display('news').

------

`/:page_slug` should map to `PagesController::display()`, where `page_slug` fits the regular expression pattern `[a-z]+`. Additionally, using this URL pattern, we should be able to access the `page_slug` argument through `$this->request->params` in the `PagesController`.
```php
Router::connect(
    '/:page_slug',
    [
        'controller' => 'pages',
        'action'     => 'display'
    ],
    [
        'page_slug' => '[a-z]+'
    ]
);
```

# Users
These URLs are used for accessing user-related views.

`UsersController::profile_view('nathadir')` from `/users/nathadir`, `/users/nathadir/`, `/users/nathadir/profile`:

```php
Router::connect(
    '/users/:name_slug',
    [
        'controller' => 'users',
        'action'     => 'display'
    ],
    [
        'name_slug' => '[a-z]+',
        'view'      => '[a-z]+'
    ]
);
```

`/users/nathadir/` and `/users/nathadir/profile` should both map to `UsersController::display()`, where `$this->request->params` will hold `['view' => 'profile', 'user_slug' => 'nathadir']`, and where both `view` satisfies the regular expression pattern `[a-z]+`, while `user_slug` satisfies whatever regular expression pattern fits the slug output (assuming this is a method available on the `String` class).
```php
Router::connect(
    '/users/:name_slug/:view',
    [
        'controller' => 'users',
        'action'     => 'display'
    ],
    [
        'name_slug' => '[a-z]+',
        'view'      => '[a-z]+'
    ]
);
```