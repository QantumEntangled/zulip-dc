# Zulip Docker

## env_file.env

Edit the contents of env_file.env to reflect your email and domain configuration.

```Bash
SECRETS_secret_key=REPLACE_WITH_SECURE_SECRET_KEY
SECRETS_email_password=123456789
```

## Create Realm

After spinning up the containers, run the following command to create the organization in Zulip.

```Bash
docker-compose exec app sudo -H -u zulip -g zulip /home/zulip/deployments/current/manage.py generate_realm_creation_link
```
