# Use Case Model

**Author**: **Team44**

## 1 Use Case Diagram

*This section should contain a use case diagram with all the actors and use cases for the system, suitably connected.*

## 2 Use Case Descriptions

**UC1 - User Login**
**R1:**  The user should be allowed to login as a player or an administrator.
**Pre-condition:** none
**Post-condition:** Player menu or Administrator menu will appear.

**Scenario:**
1. User opens Cryptogram application.
2. User selects Player or Administrator.
3. User inputs userName.
4. If user clicks " login as a player", and userName is right,  a player main menu with View/Play cryptogram, view player rating list will appear if the user is a player.
5. If user clicks " login as an administrator", and userName is authentic as the administrator, an Administrator menu with “Add User” and “Add Cryptogram” will appear if user login as an Administrator.
6. If userName is not correct, system prompts " Wrong userName, please try again."

**UC2 - Administrator Add a player**
**R2:** The administrator shall be able to add a new player.
**Pre-condition:** The user is logged in as an administrator. Added player userName shall be unique. 
**Post-condition:** Player will be created and saved.
**Scenario:**
1. Administrator selects “ Add a Player”.
2. Administrator inputs player's firstName, lastName and userName.
4.1  Administrator input is valid, player information will be saved, back to Administrator menu.
4.2 Administrator input is invalid, prompt Administrator to try again. 

**UC3 - Administrator Add a cryptogram**
**R3:** The administrator shall be able to add a new cryptogram.
**Pre-condition:** The user is logged in as an administrator. Cryptogram must be unique and contains at least one alphabetic letter. Encoding phrase must match solution phrase. 
**Post-condition:** Cryptogram will be saved and assigned an UIUD.
**Scenario: **
1. Administrator selects “ Add a Cryptogram”.
2. Administrator enters solution phrase.
3.1 If solution phrase does not contain any alphabetic letter, Administrator will be prompted to input a valid solution phrase.
3.2 If solution phrase contains one or more alphabetic letters, Administrator enters a matching encoding phrase.
4 Administrator clicks “modifyCryptogram’ to edit solution phrase and its matching encoding phrase.
5 Administrator clicks “saveCryptogram” to save entered cryptogram. 
6 Once save, Administrator receives the UIUD number.

**UC4 - Player views cryptogram and plays a cryptogram**
**R4:** The player shall be able to play a cryptogram.
**Pre-condition:** Player is in player main menu. 
**Post-condition:** Player’s solution and number of attempts will be updated.
**Scenario:** 
1. Player clicks “View/Play Cryptogram”.
2. A list with cryptogram identifier, whether the player has solved it, and the number of incorrect solution submissions will be displayed.
3.1 If there is no current available cryptogram, system prompts player to come back later.
3.2 User selects a cryptogram from the available cryptogram list by clicking the UIUD.
4. A cryptogram will be shown with UIUD, its encoded phrase appears and an empty solution editor. 
5 Player inputs and edits a solution in the solution editor.
6. Player submits solution when he/she is ready.
7. System prompts the player whether the solution is correct or not.
7.1 If solution is correct, the players is prompted to “try another one” or “back to main menu”. 
7.2 If solution is not correct, the players is prompted to either “try again” or “try another one” or “back to main menu”.
8.1 If “try again” clicked, the same cryptogram will display.
8.2: If “try another one” clicked, available cryptogram list will be shown.
8.3 If “back to main menu” clicked, player main menu will be displayed.

**UC5 - Player views player rating list**
**R6:** The player shall be able to view player rating list.
**Pre-condition:** Players are in player main menu. 
**Post-condition:** none
**Scenario:** 
1. Player clicks “view player rating list”.
2. A list of player ratings shall display, for each player, his or her name, the number of cryptograms solved, the number of cryptograms started, and the total number of incorrect solutions submitted. The list shall be sorted in descending order by the number of cryptograms solved.
3. System prompts the player with the option to “back to main menu”.
4. If “back to main menu” clicked, player main menu will be displayed.

**UC6 - Player views history**
**R6:** The player shall be able to view history.
**Pre-condition:** Players are in player main menu. 
**Post-condition:** None
**Scenario:** 
1. In the player main menu, player clicks “view player history”.
2. A list of previously solved or attempted cryptogram shall display.
3. System prompts the player with the option to “back to main menu”.
4. If “back to main menu” clicked, player main menu will be displayed.

