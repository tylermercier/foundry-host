Guide steps copied from https://theelous3.net/how_to_set_up_foundryvtt_server

Copy file to server
`rsync ~/Downloads/plutonium-foundry10.zip root@vtt.vidja.ca:/home`

Move upload into foundry
`mv plutonium-foundry10.zip /home/foundry/foundry_data/Data/modules/plut.zip`
`chmod 777 plutonium-foundry10.zip /home/foundry/foundry_data/Data/modules/plut.zip`
`su foundry`
`unzip plutonium-foundry10.zip /home/foundry/foundry_data/Data/modules/plut.zip`

Foundry folders

Install module location
`/home/foundry/foundry_data/Data/modules`

Common asset folder
`/home/foundry/foundry_data/Data/shared`
