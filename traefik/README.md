### create acme.json
```
touch acme.json
chmod 600 acme.json
```
### ACME E-Mail manuel anpassen
```
cp example.traefik.yml traefik.yml
nano traefik.yml
```

### Befeht password hash für .env & rest anpassen
```
sudo apt install apache2-utils
```
```
echo $(htpasswd -nb "user" "pw") | sed -e s/\\$/\\$\\$/g
```

### Edit ENV File
```
cp example.env .env
nano .env
```
### Start Container

```
docker compose up -d
docker compose logs
```

DNS Record setzen [sub_domain].[domain]