IP: 10.10.31.195
```bash
ssh Administrator@10.10.31.195

cd Downloads
powershell -ep bypass
. .\PowerView.ps1
Get-NetComputer -fulldata | select operatingsystem
Get-NetUser | select cn
Get-NetGroup -GroupName *
Get-NetUser -SPN | ?{$_.memberof -match 'Domain Admins'}