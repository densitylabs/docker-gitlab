This is a docker image that allows you to setup gitlab using environment variables.

for instance you can setup smtp like this:

```
GITLAB_SMTP_ENABLE=true
GITLAB_SMTP_ADDRESS="smtp.server"
GITLAB_SMTP_PORT=456
GITLAB_SMTP_USER_NAME="smtp user"
GITLAB_SMTP_PASSWORD="smtp password"
GITLAB_SMTP_DOMAIN="example.com"
```
