# Use Case Model

**Author**: **Team44**

## 1 Use Case Diagram

*This section should contain a use case diagram with all the actors and use cases for the system, suitably connected.*

## 2 Use Case Descriptions

**UC1 - User Login**<br />
**R1:**  The user should be allowed to login as a player or an administrator.<br />
**Pre-condition:** none.<br />
**Post-condition:** Player menu or Administrator menu will appear.<br />
**Scenario:**<br />
1. User opens Cryptogram application.<br />
2. User selects Player or Administrator.<br />
3. User inputs userName.<br />
4. If user clicks " login as a player", and userName is right,  a player main menu with View/Play cryptogram, view player rating list will appear if the user is a player.<br />
5. If user clicks " login as an administrator", and userName is authentic as the administrator, an Administrator menu with “Add User” and “Add Cryptogram” will appear if user login as an Administrator.<br />
6. If userName is not correct, system prompts " Wrong userName, please try again."<br />

**UC2 - Administrator Add a player**<br />
**R2:** The administrator shall be able to add a new player.<br />
**Pre-condition:** The user is logged in as an administrator. Added player userName shall be unique. <br />
**Post-condition:** Player will be created and saved.<br />
**Scenario:**<br />
1. Administrator selects “ Add a Player”.<br />
2. Administrator inputs player's firstName, lastName and userName.<br />
4.1  Administrator input is valid, player information will be saved, back to Administrator menu.<br />
4.2 Administrator input is invalid, prompt Administrator to try again. <br />

**UC3 - Administrator Add a cryptogram**<br />
**R3:** The administrator shall be able to add a new cryptogram.<br />
**Pre-condition:** The user is logged in as an administrator. Cryptogram must be unique and contains at least one alphabetic letter. Encoding phrase must match solution phrase. <br />
**Post-condition:** Cryptogram will be saved and assigned an UIUD.<br />
**Scenario: **<br />
1. Administrator selects “ Add a Cryptogram”.<br />
2. Administrator enters solution phrase.<br />
3.1 If solution phrase does not contain any alphabetic letter, Administrator will be prompted to input a valid solution phrase.<br />
3.2 If solution phrase contains one or more alphabetic letters, Administrator enters a matching encoding phrase.<br />
4 Administrator clicks “modifyCryptogram’ to edit solution phrase and its matching encoding phrase.<br />
5 Administrator clicks “saveCryptogram” to save entered cryptogram. <br />
6 Once save, Administrator receives the UIUD number.<br />

**UC4 - Player views cryptogram and plays a cryptogram**<br />
**R4:** The player shall be able to play a cryptogram.<br />
**Pre-condition:** Player is in player main menu. <br />
**Post-condition:** Player’s solution and number of attempts will be updated.<br />
**Scenario:** <br />
1. Player clicks “View/Play Cryptogram”.<br />
2. A list with cryptogram identifier, whether the player has solved it, and the number of incorrect solution submissions will be displayed.<br />
3.1 If there is no current available cryptogram, system prompts player to come back later.<br />
3.2 User selects a cryptogram from the available cryptogram list by clicking the UIUD.<br />
4. A cryptogram will be shown with UIUD, its encoded phrase appears and an empty solution editor. <br />
5 Player inputs and edits a solution in the solution editor.<br />
6. Player submits solution when he/she is ready.<br />
7. System prompts the player whether the solution is correct or not.<br />
7.1 If solution is correct, the players is prompted to “try another one” or “back to main menu”.<br /> 
7.2 If solution is not correct, the players is prompted to either “try again” or “try another one” or “back to main menu”.<br />
8.1 If “try again” clicked, the same cryptogram will display.<br />
8.2: If “try another one” clicked, available cryptogram list will be shown.<br />
8.3 If “back to main menu” clicked, player main menu will be displayed.<br />

**UC5 - Player views player rating list**<br />
**R5:** The player shall be able to view player rating list.<br />
**Pre-condition:** Players are in player main menu. <br />
**Post-condition:** none<br />
**Scenario:** <br />
1. Player clicks “view player rating list”.<br />
2. A list of player ratings shall display, for each player, his or her name, the number of cryptograms solved, the number of cryptograms started, and the total number of incorrect solutions submitted. The list shall be sorted in descending order by the number of cryptograms solved.<br />
3. System prompts the player with the option to “back to main menu”.<br />
4. If “back to main menu” clicked, player main menu will be displayed.<br />

**UC6 - Player views history**<br />
**R6:** The player shall be able to view history.<br />
**Pre-condition:** Players are in player main menu. <br />
**Post-condition:** None<br />
**Scenario:** <br />
1. In the player main menu, player clicks “view player history”.<br />
2. A list of previously solved or attempted cryptogram shall display.<br />
3. System prompts the player with the option to “back to main menu”.<br />
4. If “back to main menu” clicked, player main menu will be displayed.<br />

