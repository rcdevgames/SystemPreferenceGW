
Follow these steps:

1.  Locate the app folder in Finder that contains the app for which you need to assign permissions.
    
2.  Open Terminal, type the command  `codesign -dr -`  and drag the app file from Finder into the Terminal window.
    
3.  Press Enter. Terminal will display the path to the app along with other details, including its identifier.enter code here
    

Example:  `codesign -dr - /Applications/Microsoft\ Teams.app`  Take note of the app's identifier (e.g.,  `com.microsoft.teams`).

4.  In Terminal, enter the following commands:
    
    ```
     cd ~/Downloads/
     chmod +x tccplus
     ./tccplus add Microphone [identifier]
    
    ```
    

Replace "[identifier]" with the app's identifier you noted earlier. Example:  `./tccplus add Microphone com.microsoft.teams`

5.  Press Enter. Terminal will confirm the successful addition of permissions.

To grant camera access as well, repeat the previous command, replacing "Microphone" with "Camera".
