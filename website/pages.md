Proposed features, functionality and considerations for website pages.

## User 
URL: `/user`

# Application
Only accessible when an application has been posted by the user. Commenting disabled when application is locked (accepted/declined).
Can have three status flags: `accepted`, `declined`, `pending`.
URL: `user/nathadir/application/`

*User can*
* View application [`/view/`]
* Edit application (done from 'view' page) [`/edit/`]
* Comment

Should save all versions of application (if application edited, comments should link to version that was active at time of posting).
Can NEVER edit older versions of application - ONLY the latest version can be edited, and will create new version of application.

*Raider can*
* Comment
* Vote up/down for application

Votes should never be displayed to author of application (even if accepted/declined)

*Officer can*
* Comment
* Flag application as accepted/declined/pending

# Profile

* get gear rankings from WoWProgress (?)