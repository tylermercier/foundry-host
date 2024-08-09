Create directories for foundry

`cd ~`
`mkdir foundryvtt`
`mkdir foundrydata`
`cd foundryvtt`

Download foundry. You will need to get a download url from https://foundryvtt.com/community/nohandle/licenses

`curl 'PASTE_IN_HERE' -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8' -H 'Accept-Language: en-US,en;q=0.5' --compressed -H 'Connection: keep-alive' -H 'Upgrade-Insecure-Requests: 1' -o foundryvtt.zip`

Extract foundry
`unzip foundryvtt.zip`

Check foundry is running
`node resources/app/main.js --dataPath=/home/foundry/foundrydata`

Check/restart service

```
systemctl list-units --type=service
...
foundryvtt.service
...
sudo systemctl restart foundryvtt.service
```
