# Installation Process

1. Download and unzip the following file (preferably to your Downloads folder)
Note: After unzipping you should be left with a VSCodeSetup folder, and the following files:
- extensions.txt
- Global Snippets.code-snippets
- settings.json
- sql.json
- sql-field-list-formatter-0.5.0.vsix
- trailing-spaces-0.0.2.vsix
- uninstall_extensions.txt
- VSCodeSetup.ps1

2. Open up the 'Windows PowerShell ISE' application (because security may block access to actual PowerShell)

3. Within the command-line interface, change to the VSCodeSetup directory that you previously unzipped.
Since it was in my Downloads folder already, I just needed to change to \Downloads\VSCodeSetup
cd .\Downloads\VSCodeSetup

4. Run the Install-VSCodeProfile.ps1 PowerShell script
.\VSCodeSetup.ps1

5. Once the PowerShell script starts, it will do the following:
	1. Check to see if VS Code, Node.js / npm, and Git are installed
		a. If they are, it tries to update them
		b. If they are not, it tries to install them
	2. Re-reads PATH variables (to ensure we can call the correct shortcuts)
	3. Disables PowerShell and Node.js / npm warnings
	4. Sets up the required directory and file paths and checks to see if all the required files are present
	5. Backs up the user's current VS Code extension list and settings file
	6. Adjusts the SSL and Certificate settings

6. When prompted, enter in the required information.
- If all went well, the Snippets files and Settings file should have been modified with the user's given information

7. When prompted, enter Y to copy the files to the correct VS Code directory

8. Any unneeded extensions (like deprecated ones or ones that are no longer supported by VS Code) will be uninstalled

9. When prompted, enter Y to install the recommended VS Code extensions

10. Then a bit of clean up should take place (mainly to reset warnings) 

11. If everything went well, you should see a message, then be prompted to hit the Enter key to start a new VS Code instance

12. Profit.
