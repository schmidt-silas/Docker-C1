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

### make relay use rels istead of rel
```
nano management.json
```
change `"Addresses": ["rel://<NETBIRD_DOMAIN>:443/relay"],` (in the relay portion of the json file)
to `"Addresses": ["rels://<NETBIRD_DOMAIN>:443/relay"],`

### Start Container
```
docker compose up -d
docker compose logs
```

DNS Record setzen [sub_domain].[domain]


---------------------------------
### For Authentik (can probably be  skiped since it's explained in the new doku form Netbird)
1. authentik admin interface
2. left menu --> System --> Brands
3. edit authentik-default (or custom)
4. navigate to Default flows
5. set Device code flow to default-authenticator-static-setup
6. hit update