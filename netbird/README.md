### like official doku
```
https://docs.netbird.io/selfhosted/selfhosted-guide
```
### replace docker.tmpl and setup.env
### Edit SETUP File
```
nano setup.env
```
### start script
```
./configure
```
### copy artefacts to netbird folder
### Start Container
```
docker compose up -d
docker compose logs
```

DNS Record setzen [sub_domain].[domain]


---------------------------------
### For Authentik
1. authentik admin interface
2. left menu --> System --> Brands
3. edit authentik-default (or custom)
4. navigate to Default flows
5. set Device code flow to default-authenticator-static-setup
6. hit update