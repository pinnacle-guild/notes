## Widgets
Features, design, functionality and considerations for site widgets.

# Item tooltip
Parse page after load to determine if any item tooltips are needed. Put item information in table. Start fetching and saving data in the background immediately.
If user mouses over an item before it has been fetched, we pause the background loading and force-load the item that a tooltip was requested for.