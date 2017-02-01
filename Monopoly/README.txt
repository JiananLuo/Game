1.	Introduction
A game of BB7K is a Monpoly game, consists of a board with the board being based on the University of Waterloo campus which has 40 squares. When a player moves, an action specific to the square they land on occurs. The goal of the game is to be the only player to not drop out of university (declare bankruptcy). Play proceeds as follows: players take turns moving around the board, buying and improving on-campus buildings (properties), and paying tuition (rent).

2.	Gameplay
A typical turn should be played as follows:
	• When not in the middle of another action, the player can offer a trade, buy/sell improvements, and mortgage/unmortgage buildings they own.
	• If the player is in the DC Tims Line, they follow the procedure to leave.
	• Otherwise, the player rolls two six sided dice. Their token moves the sum of dice. They take the action of the square they landed on. If they rolled doubles, they roll again. If they roll three sets of doubles in a row, they do not move the number shown on the last set and move to DC Tims Line5 instead and cannot roll again.
	• When the player cannot roll, they can finish their turn.
	• At any time when a player must pay more money than they currently have, they have the option to drop out (declare bankruptcy) or attempt to trade, mortgage buildings and sell improvements to gather the required money.

3 Command Interpreter
Initially, the game will demand the player enter the number of players, followed by the name of each player and the character that will represent the player on the board. Each player starts with 1500 money. Play will then continue in the way described below or until one player remains.
	The following commands can be supplied to your command interpreter:
	• roll: if the player can roll, the player rolls two dice, moves the sum of the two dice and takes action on the square they landed on.
	• next: if the player cannot roll, gives control to the next player.
	• trade <name> <give> <receive>: offers a trade to name with the current player offering give and requesting receive, where give and receive are either amounts of money or a property name. Responses are accept and reject. For example,
		– trade Nomair 500 DC indicates that the current player is willing to give Nomair $500 in exchange for the DC building
		– trade Kirsten DC MC indicates that the current player is willing to give Kirsten DC in exchange for MC
		– trade Sean MC 500 indicates that the current player is willing to give Sean MC in exchange for $500
		Note: it does not make sense for a player to offer to give money in return for money.
		Note: A player can only offer to trade a property if all properties in the monopoly (including the property being offered for trade) do not have improvements. In the case that a player incorrectly offers for trade a property that has improvements (or for which a property in the monopoly has improvements), the game must automatically reject the trade offer.
	• improve <property> buy/sell: attempts to buy or sell an improvement for property.
	• mortgage <property>: attempts to mortgage property.
	• unmortgage <property>: attempts to unmortgage property.
	• bankrupt: player declares bankruptcy. This command is only available when a player must pay more money then they currently have.
	• assets: displays the assets of the current player. Does not work if the player is deciding how to pay Tuition.
	• save <filename>: saves the current state of the game (as per the description below) to the given file.



5.	Map
____________________________________________________________________________________________________
|Goose   |        |NEEDLES |        |        |V1      |        |        |CIF     |        |GO TO   |
|Nesting |--------|HALL    |--------|--------|        |--------|--------|        |--------|TIMS    |
|        |EV1     |        |EV2     |EV3     |        |PHYS    |B1      |        |B2      |        |
|        |        |        |        |        |        |        |        |        |        |        |
|________|________|________|________|________|________|________|________|________|________|________|
|        |                                                                                |        |
|--------|                                                                                |--------|
|OPT     |                                                                                |EIT     |
|        |                                                                                |        |
|________|                                                                                |________|
|        |                                                                                |        |
|--------|                                                                                |--------|
|BMH     |                                                                                |ESC     |
|        |                                                                                |        |
|________|                                                                                |________|
|SLC     |                                                                                |SLC     |
|        |                                                                                |        |
|        |                                                                                |        |
|        |                                                                                |        |
|________|                                                                                |________|
|        |                                                                                |        |
|--------|                                                                                |--------|
|LHI     |                                                                                |C2      |
|        |                                                                                |        |
|________|                                                                                |________|
|UWP     |                                                                                |REV     |
|        |                                                                                |        |
|        |                                                                                |        |
|        |                                                                                |        |
|________|                                                                                |________|
|        |                                                                                |NEEDLES |
|--------|                                                                                |HALL    |
|CPH     |                                                                                |        |
|        |                                                                                |        |
|________|                                                                                |________|
|        |                                                                                |        |
|--------|                                                                                |--------|
|DWE     |                                                                                |MC      |
|        |                                                                                |        |
|________|                                                                                |________|
|PAC     |                                                                                |COOP    |
|        |                                                                                |FEE     |
|        |                                                                                |        |
|        |                                                                                |        |
|________|                                                                                |________|
|        |                                                                                |        |
|--------|                                                                                |--------|
|RCH     |                                                                                |DC      |
|        |                                                                                |        |
|________|________________________________________________________________________________|________|
|DC Tims |        |        |NEEDLES |        |MKV     |TUITION |        |SLC     |        |COLLECT |
|Line    |--------|--------|HALL    |--------|        |        |--------|        |--------|OSAP    |
|        |HH      |PAS     |        |ECH     |        |        |ML      |        |AL      |        |
|        |        |        |        |        |        |        |        |        |        |        |
|________|________|________|________|________|________|________|________|________|________|________|
