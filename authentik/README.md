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