# Installation (Docker)

## login.json pre-requisites for Linux Install

### AnkerMake Slicer installed on another Machine

1. Install the [AnkerMake slicer](https://www.ankermake.com/software) on a supported Operating System.  Make sure you open it and login via the “Account” dropdown in the top toolbar.

2. Retreive the ```login.json``` file from the supported operating system:

  Windows Default Location:
  ```sh
  %APPDATA%\AnkerMake\AnkerMake_64bit_fp\login.json
  ```
   
  MacOS Default Location:
  ```sh
  $HOME/Library/Application\ Support/AnkerMake/AnkerMake_64bit_fp/login.json
   ```

3. Take said ```login.json``` file and store it in a location your docker instance will be able to access it from.

4. Now follow the Docker Compose Instructions below.

### Native Linux

1. Install the [AnkerMake slicer](https://www.ankermake.com/software) on Linux via emulation such as Wine.  Make sure you open it and login via the “Account” dropdown in the top toolbar.
   
2. Retreive the ```login.json``` file ```~/.wine/drive_c/users/$USER/AppData/Local/AnkerMake/AnkerMake_64bit_fp/login.json```

3. Take said ```login.json``` file and store it in a location your docker instance will be able to access it from.

4. Now follow the Docker Compose Instructions below.

## Docker Compose Instructions

To start `ankerctl` using docker compose on your local machine, run:

```sh
curl -O https://raw.githubusercontent.com/anselor/ankermake-m5-protocol/exiles/docker-compose.yaml
curl -O https://raw.githubusercontent.com/anselor/ankermake-m5-protocol/exiles/compose.sh
curl -O https://raw.githubusercontent.com/anselor/ankermake-m5-protocol/exiles/.env
docker-compose pull
./compose.sh up
```


To start `ankerctl` usinge docker compose as a daemon service running on another system:

```sh
curl -O https://raw.githubusercontent.com/anselor/ankermake-m5-protocol/exiles/docker-compose.yaml
curl -O https://raw.githubusercontent.com/anselor/ankermake-m5-protocol/exiles/compose.sh
curl -O https://raw.githubusercontent.com/anselor/ankermake-m5-protocol/exiles/.env
docker-compose pull
./compose.sh -o up -d
```
