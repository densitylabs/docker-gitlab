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


Read gitlab documentation:

* http://doc.gitlab.com/omnibus/docker/
* https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/settings/smtp.md


If you are using an existing docker image `gitlab.rb` is inside of the config volume.
You need to copy it inside the volume. You can do it like this:

```
docker run -ti framallo/gitlab cp /gitlab.rb /etc/gitlab/gitlab.rb
```


Last, remember to run `gitlab-ctl reconfigure` every time you change the config file
