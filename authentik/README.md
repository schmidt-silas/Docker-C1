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
```
```
echo "PG_PASS=$(openssl rand -base64 36 | tr -d '\n')" >> .env
echo "AUTHENTIK_SECRET_KEY=$(openssl rand -base64 60 | tr -d '\n')" >> .env
echo "AUTHENTIK_ERROR_REPORTING__ENABLED=true" >> .env
```
```
nano .env
```
### Start Container

```
docker compose up -d
docker compose logs
```

DNS Record setzen [sub_domain].[domain]

### INITIAL SETUP !!
```
https://<FQDN>/if/flow/initial-setup/
```