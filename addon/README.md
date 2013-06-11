## Addon / AIR application
Notes regarding proposed addon for viewing/updating data in-game (synching information to/from website in .lua files using AIR app).

# Features
* Limit use
    * Should limit use to trialists/raiders/officers?
* Versioning
    * Update addon automatically (via AIR app)
        * Addon code hosted on website
    * Always require latest version
        * Communicate with other raiders (via ADDON channel) on login
        * Disable (deprecated) features if newer version available - will avoid conflicts when sync
* Calendar
    * Update calendar to reflect website
    * Notification of raids (needed?)
        * Should be available both in and out of game (addon / AIR app)
        * Should be customizable
* Raid roster
    * Addon should load guild roster on login - save information
    * Any conflicts (due to differences in rosters) should be handled on website - give officers/admin notification
* Items
    * Save equipped gear per character
    * Save score for each item (if Mr. Robot weights available)
* Wishlist
    * Access to wishlist only for characters on user's account (officers cannot view all wishlists from here - information displayed in in-game raidcomp builder)
    * In-game view of wishlist - should have listing per character [can access other char's wishlists from that account] 
        * Remove items from wishlist
        * Add items to wishlist (using item link/id)
        * Shows item tooltip
        * Shows currently equipped item in same row
        * If Mr. Robot stat weights can be fetched, should display score
            * Score for item displayed for character wishlist belongs to
            * Show score for item (absolute)
            * Show score relative to equipped item (absolute, percentage)
    * Dungeon Journal interfacing
        * If Journal allows us to hook into it, we can enable adding/removing items to wishlists (for any of the user's characters) from here.
        * If adding/removing items, show confirmation dialog
        * Show indication in Journal interface if item is in wishlist (show which character's wishlist - and for which spec)
* Character optimization
    * Monitor currency information
        * Is the player getting VP for upgrades [when those are listed as available from officer-part of site]?
        * Is player getting bonus roll coins [only check when char does not have all items from wishlist]
        * This information should be viewable on user's profile page, and for officers [on 'performance' part of officer page]
        
# Design
The AIR app should mirror the design of the website (mimicking the mock-ups released of the Battle.net Launcher).
The in-game addon should (if possible) look like the AIR app.