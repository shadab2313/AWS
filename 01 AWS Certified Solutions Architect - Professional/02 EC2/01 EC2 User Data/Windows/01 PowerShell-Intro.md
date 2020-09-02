# 01 PowerShell-Intro

## Doc
* [user-data-powershell](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-windows-user-data.html#user-data-powershell)

## Syntax
* Create a text file with the instance user data. To execute user data scripts every time you reboot
  or start the instance, add **\<persist\>true\</persist\>**, as shown in the following example

## User data
### Demo-01
````PowerShell
<powershell>
$file = $env:SystemRoot + "\Temp\" + (Get-Date).ToString("MM-dd-yy-hh-mm")
New-Item $file -ItemType file
</powershell>
````

### Demo-02