# Hubot Redmine

Light mapping of the Redmine REST API that allows hubot access to some basic redmine tasks. Once you have a redmine
user (preferably one with enough access to modify tickets), add the following to your heroku/etc. config:

    heroku config:add HUBOT_REDMINE_BASE_URL="http://redmine.your-server.com"
    heroku config:add HUBOT_REDMINE_TOKEN="your api token here"

If using over SSL, add the following to your heroku config:

    heroku config:add HUBOT_REDMINE_SSL=1

If redmine use self-signed certification, or not-well-known CA such as cacert.org,
place certification pem file and add the following:

   heroku config:add HUBOT_REDMINE_SSL_CA=/etc/ssl/certs/cacert.org-class3.pem

If not spefified, it use well-known authority certificates, such as verisign, to check the remote host.

![screenshot](https://github.com/robhurring/hubot-redmine/blob/master/ss.png?raw=true)

## Showing issue details

* Hubot show me [issue id]
* Hubot redmine me [issue id]

## Showing my issue (or another user's)

* Hubot show my issues
* Hubot show [user]'s issues
** [user] will attempt to match on redmine firstname or login

## Re-Assigning tickets

* Hubot assign [issue id] to [user]

## Leaving notes on tickets

* Hubot update [issue id] with "[comments]"

## Create tickets

* Hubot add issue to "[project]" [traker id] with "[subject]"
** [tracker id] is optional and represent the number matching literal value Bug/Feature/...

## Get a link to an issue

* Hubot link me [issue id]

## Set the percent done of an issue

* Hubot set [issue id] to 100% "[comments]"
* Hubot add [hours] hours to [issue id] "[comments]"

## More coming!
