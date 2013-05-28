## Routing
We want to map the following URL patterns in a special manner:

`/:page_slug` should map to `PagesController::display('page_slug')`, where `page_slug` fits the regular expression pattern `[a-z]+`. This *should* be achieved by the following routing:
```php
Router::connect(
    '/:page_slug',
    ['controller' => 'pages', 'action' => 'display'],
    ['page_slug' => '[a-z]+']
);
```

`/users/nathadir/profile` should map to `UsersController::display()`, where we are provided the parameters `['view' => 'profile', 'user_slug' => 'nathadir']`, and where both `view` and satisfies the regular expression pattern `[a-z]+`, while `user_slug` satisfies whatever regular expression pattern fits the slug output (assuming this is a method available on the `String` class).