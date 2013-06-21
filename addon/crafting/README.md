# Crafting Module
The following is a list of features that should be implemented in the Crafting module of the addon.

## Request
The user should be able to request the crafting of an item (in given quantity). All requests should be sent to officers for approval. Permissions to send crafting requests should be limited to
Raiders, Raider alts, Officers, Officer alts, GM. When officers view a request, it should be listed whether or not the requestee provides materials him/herself (and how many, if only partial).
If no (or partial) amount of materials are provided, the approximate cost of the remaining materials should be listed, as well as how many materials are available for the craft in the Guild Bank.
Furthermore, if the item is available on the Auction House, the price of the item there should also be displayed.
The date of the request should be display, as well as the user requesting it. User should be able to accompany the crafting request with a note, and also be able to select the character for which
the request is made (ie. who should the finished product be sent to).

Once a request has been approved, the request will be forwarded to the people able to craft said item (it should always send the request to Officer/GM if they are able, and only send it to Raiders
if they are not able to craft it).

If the requestee is (partially) providing materials for the requested item, then once the request has been approved, requstee should be prompted to deposit the materials in the Guild Bank (Tab number something - can be determined later).
Once the items are deposited, the request will be sent.

Once the request lands at the people able to craft the item, and an item has been crafted (per item, if quantity is greater than one), addon should communicate that the request has been (partially) fulfilled.
When the person handling the request either mails the item to the requestee (or any character associated with requestee), it should be noted, and the requestee should be able to see that the request
has been fulfilled (and that the item is in the mail). This information should be available on any character of the requestee.
Once a product that was requested is crafted, the request status should be updated to reflect where the product is (ie. Nathadir should be able to see that his request for 6 Royal Scribe's Satchel has been
(partially) handled by Asaki, and that he currently has made 6 of the bags, 2 of which are in his inventory, 3 of which are in the Guild Bank and 1 of which has been mailed to Keanaran).