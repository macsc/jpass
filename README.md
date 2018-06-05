# jpass
Workflow for randomizing the JAMF Pro management account's password per computer. 

Comprised of:
1. A scoped policy to execute a script on each client, randomizing the management account's password per computer and uploading a salt to the JSS server 
2. A commandline tool for use by remote support to reveal the password to someone with JSS admin access based upon the computer's serial number or the AD username of the employee it is assigned to. 
3. A Self Service policy for local admins with JSS admin access to issue a per session simple password that eases local work on the computer, then resets to randomized after closure or 5 minutes, whichever comes first.
