These are standalone versions of the password generators from ss64.com.

There are two password generators:

*   The [standard one][standard]
*   The [strong one][strong]

Here there are three versions of each of these generators:

*   Bash
*   Powershell
*   Standalone HTML + Javascript

Using the bash version
----------------------

*   copy `passwdgen.bash` from the `bash` subdirectory into your home directory
*   add the following line to your `.bashrc`:

        source passwdgen.bash

Next time you start bash, you can use the following commands:

    strongpw site1 [site2...]
    stdpw    site1 [site2...]

You will be prompted for the master key. Then, if there is only one site
specified, you will get the password into the clipboard, else passwords will be
echoed in your terminal.

An additional verification code will appear, that will be always the same
(depends only on the typed-in master key). It can help you detect whether you
mistyped your key.

Using the Powershell version
----------------------------

*   Make a `Documents\WindowsPowerShell\Modules\PasswdGen` subfolder in your
    user profile folder
*   Copy the `.psd1` and `.psm1` files into that folder
*   In your user profile, create the file `Microsoft.PowerShell_profile.ps1`
    in the subfolder `Documents\WindowsPowerShell` if it does not exist, and
    then add the following line:

        Import-Module PasswdGen

Next time you start Powershell, you can use the following commands:

    Get-StrongPw site1 [site2...]
    Get-StdPw    site1 [site2...]

They work exactly like the bash counterparts.

[standard]: http://ss64.com/passwords/ "Standard SS64.com password generator"
[strong]: http://ss64.com/pass/ "Strong SS64.com password generator"
