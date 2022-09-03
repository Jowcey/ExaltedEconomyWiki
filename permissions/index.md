---
layout: default
title: Commands and Permissions
nav_order: 2
has_children: true
---

# Exalted Economy Commands and Permissions

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


---

## Exalted Economy Permissions and Commands FAQ

* **<span style="color: orange;">Question: `<PLUGIN>` is overriding a command from ExaltedEconomy, what can i do?!</span>**
    * *<span style="color: #99cc00;">Answer: Run the commands as follows instead `/<command>:<alias>`</span>*

---

## Misc Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.dev` | **<span style="color: #cc0000">Admin</span>** | Gives full access to the assigned user or group. Primarily used to give **Jowcey (plugin creator)** full access for diagnostic purposes. | [NoCommand] |
| `exaltedeconomy.command.economy` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to `take`, `set`, `add`, `remove` economy from players <span style="color: #3366ff;"></span> | `/economy` `<give/set/take>` `<player>` `<range [min] [max]/amount>` `[currency_name]` | `/eco` |

---

## Plugin Administration Permissions

**_There are additional administrative permissions in the other sections._**

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.command.admin` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to open the Exalted Economy control panel <span style="color: #3366ff;">(Note: Additional permissions are required to view content in this control panel, see "**Admin Permissions**" below)</span> | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.admin` | **<span style="color: #cc0000">Admin</span>** | Gives the admin user access to **_ALL TABS AND SETTINGS_** in `/exaltedeconomy` and allows the admin user to configure all of Exalted Economy parameters. **<span style="color: orange;">(IMPORTANT NOTE: Only assign this permission to the Systems Administrator in charge of server development, as the user with this permission will be able to view and modify database connection information.</span>** _If you want to allow the user to configure aspects of the economy without the ability to view and modify the primary plugin configuration, look below for specific permissions pertaining to modification of economy aspects.)</span>_ | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.admin.shop` | **<span style="color: #cc0000">Admin</span>** | Allows access to the shop tab in `/exaltedeconomy` **<span style="color: #3366ff;">(Note: Only applied if you don't have `exaltedeconomy.admin`)</span>** | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.admin.currency` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user access to the `currency` configuration tab in `/exaltedeconomy` **<span style="color: #3366ff;">(Note: Only applied if you don't have `exaltedeconomy.admin`)</span>** | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.admin.bank` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user access to the `Banks` management tab in `/exaltedeconomy` **<span style="color: #99cc00">(_Create Banks_, _Delete Banks_, _Assign Banks_ to physical blocks, and _Modify Banks Inventory_ including the custom Physical Economy that has been configured)</span>** **<span style="color: #3366ff;">(Note: Only applied if you don't have `exaltedeconomy.admin`)</span>** | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.admin.sellwand` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user access to the `Sell Wands` configuration settings tab in `/exaltedeconomy` **<span style="color: #3366ff;">(Note: Only applied if you don't have `exaltedeconomy.admin`)</span>** | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.admin.settings` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user access to the `plugin settings` and `general settings` sections in `/exaltedeconomy` **<span style="color: #3366ff;">(Note: Only applied if you don't have `exaltedeconomy.admin`)</span>** | `/exaltedeconomy` | `/ee` |
| `exaltedeconomy.update.notification` | **<span style="color: #cc0000">Admin</span>** | Sends a message on login if there is an update available. | _[None]_ | _[None]_ |
| `exaltedeconomy.admin.item.bypass` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to bypass item permission requirements in shops | _[None]_ | _[None]_ |

---

## Shop Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.interact.shop.view` | **<span style="color: #33cc33">Player</span>** | Allows a player to interact with shops that have been assigned to blocks in the world. | _[None]_ | _[None]_ |
| `exaltedeconomy.shop.break` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to break blocks that have shops assigned to them in the world. | _[None]_ | _[None]_ |
| `exaltedeconomy.shop.user` | **<span style="color: #33cc33">Player</span>** | Allows the player to open the shops menu via a command and bypass the requirement of physically visiting blocks with shops assigned to them. | `/shop` `<Shop Name>` | _[None]_ |
| `exaltedeconomy.shop.user.other` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user with this assigned permission to open the shop menu to be viewed by other players. | `/shop [open <player name>]` | _[None]_ |
| `exaltedeconomy.shop.user.category` | **<span style="color: #33cc33">Player</span>** | Allows the player to view the list of all `ADMIN SHOPS` when using the `/shop` command. | `/shop` | _[None]_ |
| `exaltedeconomy.shop.category.back` | **<span style="color: #33cc33">Player</span>** | Allows the player to view and interact with the "back" button in the shop view. | _[None]_ | _[None]_ |
| `exaltedeconomy.shop.sell` | **<span style="color: #33cc33">Player</span>** | Allows the player to use the `/sell` command and bypass the requirement of visiting shop blocks to sell items. This command opens a window for the player to sell items. | `/sell` | _[None]_ |

---

## Shop Tax Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.shop.tax.view` | **<span style="color: #cc0000">Admin</span>** | Allows a admin user to view the tax account amount. | `/tax` | _[None]_ |
| `exaltedeconomy.shop.tax.modify` | **<span style="color: #cc0000">Admin</span>** | Allows a player to withdraw from the tax account account. | `/tax` | _[None]_ |

---

## Bank Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.interact.bank.view` | **<span style="color: #33cc33">Player</span>** | Allows a player to interact with bank blocks. | _[None]_ | _[None]_ |
| `exaltedeconomy.bank.break` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to break blocks that have been assigned as banks. | _[None]_ | _[None]_ |
| `exaltedeconomy.command.bank` | **<span style="color: #33cc33">Player</span>** | Allows the player to open the Banks menu with a command, and bypass the requirement to visit physical bank blocks. | `/bank [Bank Name]` | _[None]_ |
| `exaltedeconomy.command.bank.other` | **<span style="color: #3366ff">Console</span>** | Allows the admin user to open the bank view for another player to view. **<span style="color: #3366ff">(Note: Command can only issued from the server console.)</span>** | `/bank player:<player name>` | _[None]_ |
| `exaltedeconomy.command.bank.view` | **<span style="color: #33cc33">Player</span>** | Allows the player to view all banks through the use of a command.  | `/bank` | _[None]_ |
| `exaltedeconomy.user.bank.back` | **<span style="color: #33cc33">Player</span>** | Allows the player to view and interact with the back button while using the Banks view. | _[None]_ | _[None]_ |

---

## Trade Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.command.trade` | **<span style="color: #33cc33">Player</span>** | Allows the player to use a command to initiate trades with other players. This can bypass the requirement of the two players being required to be near each other. | `/trade [Player Name]` | _[None]_ |
| `exaltedeconomy.command.trade.toggle` | **<span style="color: #33cc33">Player</span>** | Allows the player to toggle if they allow trades from other players. | `/trade toggle` | _[None]_ |
| `exaltedeconomy.trade.interact` | **<span style="color: #33cc33">Player</span>** | Allows the player to initiate a trade through the use of `SHIFT+CLICK`. (Note: The two players must be physically near each other to initiate trades with this permission.) | `SHIFT+CLICK` while looking at the player you wish to trade with. | _[None]_ |

---

## Currency Balance Permissions


| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.command.balance.other` | **<span style="color: #33cc33">Player</span>** | Allows the player to view the balance of other players. | **`/pbalance`** `<Player Name>` `[Currency Name]` | `/pbal` |
| `exaltedeconomy.command.balance` | **<span style="color: #33cc33">Player</span>** | Allows the player to view their own balance of the given currency. | `/balance [Currency Name]` You can leave `[Currency Name]` blank to view the default currency balance. | _[None]_ |
| `exaltedeconomy.command.balancetop` | **<span style="color: #33cc33">Player</span>** | Allows the user of the command to view the balance of the top, most wealthy players. | `/balancetop` | `/baltop` |

---

## Currency / Bank Interaction Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.command.deposit` | **<span style="color: #33cc33">Player</span>** | Allows the player to deposit item currency they are holding in their hand into their bank balance through the use of a command. **<span style="color: #99cc00;">(Note: This command bypasses the requirement to visit a physical bank to deposit funds. This command does not open a GUI window.)</span>** | `/deposit` `[amount]` | _[None]_ |
| `exaltedeconomy.command.pay` | **<span style="color: #33cc33">Player</span>** | Allows the player to transfer a portion or all of their bank balance to another player through the use of a command. **<span style="color: #99cc00;">(Note: This command bypasses the requirement of withdrawing and transfering physical item currency between players.)</span>** | `/pay` `[Player Name]` `[Amount]` | _[None]_ |
| `exaltedeconomy.command.withdraw` | **<span style="color: #33cc33">Player</span>** | Allows the player to open a gui or enter an ammount to withdraw a portion or all of their bank balance. **<span style="color: #99cc00;">(Note: This command bypasses the requirement of having to visit a physical bank to deposit the physical currency from their inventory into the bank.)</span>** | `/withdraw` or `/withdraw` `[Amount]` `[Currency Name]` | _[None]_ |

---

## Auction House Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.ah.command` | **<span style="color: #33cc33">Player</span>** | Allows the player to open the auction house panel through the use of a command. **<span style="color: #99cc00;">(Note: You must assign permissions for which parts of the auction house you allow the player to</span>** | `/auctionhouse` | `/ah` |
| `exaltedeconomy.ah.interact.view` | **<span style="color: #33cc33">Player</span>** | Allows the player to open the auction house panel by visiting a physical block with the auction house assigned to it. **<span style="color: #99cc00;">(Note: You must assign permissions for which parts of the auction house you allow the player to</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.ah.user` | **<span style="color: #33cc33">Player</span>** | Allows the player to access view and interact with `ALL` auction house tabs through the use of a command. | *[None]* | *[None]* |
| `exaltedeconomy.ah.user.main` | **<span style="color: #33cc33">Player</span>** | Allows the user to view and interact with `MAIN` tab in the auction house. **<span style="color: #99cc00;">(Note: Only applied if you don't have `exaltedeconomy.ah.user` assigned to the user or permissions group)</span>** | *[None]* | *[None]* |
| `exaltedeconomy.ah.user.selling` | **<span style="color: #33cc33">Player</span>** | Allows the player to access the `SELL` tab in the auction house. **<span style="color: #99cc00;">(Note: Only applied if you don't have `exaltedeconomy.ah.user` assigned to the user or permissions group)</span>** | *[None]* | *[None]* |
| `exaltedeconomy.ah.user.expired` | **<span style="color: #33cc33">Player</span>** | Allows the user to view and retrieve their `EXPIRED` auctions. **<span style="color: #99cc00;">(Note: Only applied if you don't have `exaltedeconomy.ah.user` assigned to the user or permissions group)</span>** | *[None]* | *[None]* |
| `exaltedeconomy.ah.user.sold` | **<span style="color: #33cc33">Player</span>** | Allows the player to view their `SOLD` items in the auction house. **<span style="color: #99cc00;">(Note: Only applied if you don't have `exaltedeconomy.ah.user` assigned to the user or permissions group)</span>** | *[None]* | *[None]* |
| `exaltedeconomy.ah.user.purchased` | **<span style="color: #33cc33">Player</span>** | Allows the player to view and retrieve their `PURCHASED` items in the auction house. **<span style="color: #99cc00;">(Note: Only applied if you don't have `exaltedeconomy.ah.user` assigned to the user or permissions group)</span>** | *[None]* | *[None]* |
| `exaltedeconomy.ah.user.bids` | **<span style="color: #33cc33">Player</span>** | Allows the player to access the `BIDS` tab in the auction house. **<span style="color: #99cc00;">(Note: Only applied if you don't have `exaltedeconomy.ah.user` assigned to the user or permissions group)</span>** | *[None]* | *[None]* |
| `exaltedeconomy.ah.limit.[amount]` | **<span style="color: #33cc33">Player</span>** | Limits the amount of items a player can list in the auction house. **<span style="color: #99cc00;">(Note: The `[amount]` should be replaced with a number.)</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.ah.break` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to break blocks that have been assigned as an auction house. | _[None]_ | _[None]_ |
| `exaltedeconomy.ah.admin.expire` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to expire a listed item in the auction house. | _[None]_ | _[None]_ |

---

## Player Shop Permissions

| PERMISSION | TYPE | DESCRIPTION | COMMAND | COMMAND ALIAS |
| --- | --- | --- | --- | --- |
| `exaltedeconomy.playershop.command.create` | **<span style="color: #33cc33">Player</span>** | Allows the player to assign their own shops to a physical block. | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.manage` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to edit or delete player shops with the `/pshop` command or by visiting the physical block which has a player shop assigned to it. | *[None]* | _[None]_ |
| `exaltedeconomy.playershop.view.all` | **<span style="color: #33cc33">Player</span>** | Allows the player to open a list of **ALL AVAILABLE PLAYER SHOPS** through the use of a command. | `/pshop` | _[None]_ |
| `exaltedeconomy.playershop.view` | **<span style="color: #33cc33">Player</span>** | Allows the player to open a specific player shop through the use of a command. | `/pshop [Name of Shop]` | _[None]_ |
| `exaltedeconomy.playershop.editor` | **<span style="color: #33cc33">Player</span>** | Allows the player to edit their own shops. | `/pshop [Their Own Name]` | _[None]_ |
| `exaltedeconomy.playershop.edit.inventory.command` | **<span style="color: #33cc33">Player</span>** | Allows the player to edit their own shop inventory through the use of a command. | *[None]* | _[None]_ |
| `exaltedeconomy.playershop.edit.inventory.location` | **<span style="color: #33cc33">Player</span>** | Allows the player, while viewing the inventory of their shops, to move and relocate items. | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.locations.new` | **<span style="color: #33cc33">Player</span>** | Allows the player to create an additional shop location, for shops that are assigned to physical blocks. | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.stock.max.[max-stock]` | **<span style="color: #33cc33">Player</span>** | Modified the amount of items a player can list within their own shops. **<span style="color: #99cc00;">(Note: The `[max-stock]` should be replaced with a number.)</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.rows.max.[max-rows]` | **<span style="color: #33cc33">Player</span>** | Limits the amount of inventory rows that the user may put their listed items. **<span style="color: #99cc00;">(Note: The `[max-rows]` should be replaced with a number. Min = 1, Max = 6)</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.pages.max.[max-pages]` | **<span style="color: #33cc33">Player</span>** | Limits the amount of pages that the user can can use for their inventory. **<span style="color: #99cc00;">(Note: The `[max-pages]` should be replaced with a number.)</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.locations.max.[max-locations]` | **<span style="color: #33cc33">Player</span>** | Limits the amount of physical locations that the user can create, per shop. **<span style="color: #99cc00;">(Note: The `[max-locations]` should be replaced with a number.)</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.shops.max.[max-shops]` | **<span style="color: #33cc33">Player</span>** | Limits the amount of shops that a player can create. **<span style="color: #99cc00;">(Note: The `[max-shops]` should be replaced with a number.)</span>** | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.force.physical.currency.`[<span style="color: #33cc33">`true`</span>/<span style="color: #cc0000">`false`</span>] | **<span style="color: #33cc33">Player</span>** | Forces the player to use physical currency from their inventory while purchasing items from player shops. The user will need to withdraw physical currency from a bank or spend physical currency obtained by other means. | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.interact.view` | **<span style="color: #33cc33">Player</span>** | Allows the player to interact with blocks that have player shops assigned to them. | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.break` | **<span style="color: #33cc33">Player</span>** | Allows the user to destroy blocks that have their own shop assigned to them. | _[None]_ | _[None]_ |
| `exaltedeconomy.playershop.break.force` | **<span style="color: #cc0000">Admin</span>** | Allows the admin user to destroy any block that has a shop assigned to them. | _[None]_ | _[None]_ |

---

## Suggested Permissions Setups

### Require Physical Interaction for all Economy Transactions

**_This suggested permissions setup will allow players to interact with Exalted Economy windows by visiting physical blocks as well as with commands. Using this setup will allow players to remotely access any of the economy features._**

| PERMISSION | PERMISSIONS VALUE |
| :--- | :---: |
| `exaltedeconomy.interact.shop.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.user` | **<span style="color: #cc0000">FALSE</span>** |
| `exaltedeconomy.shop.user.category` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.category.back` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.sell` | **<span style="color: #cc0000">FALSE</span>** |
| `exaltedeconomy.interact.bank.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.bank` | **<span style="color: #cc0000">FALSE</span>** |
| `exaltedeconomy.user.bank.back` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.trade.toggle` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.trade.interact` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.balance` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.ah.user` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.ah.interact.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.ah.limit.[amount]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.command.create` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.editor` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.edit.inventory.location` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.locations.new` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.stock.max.[max-stock]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.rows.max.[max-rows]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.pages.max.[max-pages]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.locations.max.[max-locations]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.shops.max.[max-shops]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.force.physical.currency.true` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.interact.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.break` | **<span style="color: #33cc33">TRUE</span>** |

### Allow players the option to open Economy Windows via Commands

**_This suggested permissions setup will force players to visit and interact with physical entities for their various economy related transactions. All permissions in this list are listed above, this is only a suggested permissions setup for this desired result._**

| PERMISSION | PERMISSIONS VALUE |
| :--- | :---: |
| `exaltedeconomy.command.admin` | **<span style="color: #cc0000">FALSE</span>** |
| `exaltedeconomy.admin` | **<span style="color: #cc0000">FALSE</span>** |
| `exaltedeconomy.interact.shop.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.user` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.user.category` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.category.back` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.shop.sell` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.interact.bank.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.bank` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.bank.other` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.user.bank.back` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.trade` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.trade.toggle` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.trade.interact` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.balance` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.deposit` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.pay` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.command.withdraw` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.ah.user` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.ah.interact.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.ah.limit.[amount]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.command.create` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.editor` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.edit.inventory.location` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.locations.new` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.stock.max.[max-stock]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.rows.max.[max-rows]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.pages.max.[max-pages]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.locations.max.[max-locations]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.shops.max.[max-shops]` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.force.physical.currency.true` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.interact.view` | **<span style="color: #33cc33">TRUE</span>** |
| `exaltedeconomy.playershop.break` | **<span style="color: #33cc33">TRUE</span>** |
