# IPRoyal Pawns

## Requirements

Install docker and docker-compose.

## Setup

1. Change to `RDP_SERVER: "yes"` in `docker-compose.yml`
2. Uncomments `ports`
3. `docker-compose up`
4. Connect via RDP to `localhost:3389`, login: `wineuser`, password: `wineuser`
5. Run program from.

    ```bash
    wine /home/wineuser/.wine/drive_c/Program\ Files\ \(x86\)/IPRoyalPawns/iproyal_pawns.exe
    ```

6. Login to IPRoyal Pawns
7. `docker-compose down`
8. Change to `RDP_SERVER: "no"`
9. Comment `ports` in `docker-compose.yml`

After these instructions, the session files in the `session` directory should change. Each new startup should result in an automatic login.

## Start pawn

1. `docker-compose up -d`

Now pawn should already be working in the container. To check the logs, you can call the `docker-compose logs` command and view the status of the application.

## Update

Download new installer.

```bash
cd Downloads && rm IPRoyalPawnsSetup.exe && wget https://download.iproyal.com/pawns/0.40.1/win64/IPRoyalPawnsSetup.exe
```

