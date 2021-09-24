Write-Host  -ForegroundColor Green "Starting OSD for Bruker - ZTI"
Start-Sleep -Seconds 5

#Change Display Resolution for Virtual Machine
if ((Get-MyComputerModel) -match 'Virtual') {
    Write-Host  -ForegroundColor Green "Setting Display Resolution to 1600x"
    Set-DisRes 1600
}

#Make sure I have the latest OSD Content
Write-Host  -ForegroundColor Green "Updating OSD Configuration Files"
Install-Module OSD -Force

Write-Host  -ForegroundColor Green "Importing OSD Configuration Files"
Import-Module OSD -Force

#Start OSDCloud ZTI the RIGHT way
Write-Host  -ForegroundColor Green "Start OSDCloud"
Start-OSDCloudGUI -Brand "Bruker OSD"

#Restart from WinPE
Write-Host  -ForegroundColor Green "Restarting in 10 seconds!"
Start-Sleep -Seconds 10
wpeutil reboot
