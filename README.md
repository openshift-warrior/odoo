# OpenShift OpenERP quickstart

[![DEPLOY ON OpenShift](http://launch-shifter.rhcloud.com/launch/DEPLOY ON.svg)](https://openshift.redhat.com/app/console/application_type/custom?&cartridges[]=python-2.7&cartridges[]=postgresql-8.4&initial_git_url=https://github.com/openshift-warrior/odoo.git&name=Odoo)

This quickstart contains an OpenERP installation ready to run on OpenShift.

## Create your app

First, create an application with PostgreSQL:

```
$ rhc app create openerp python-2.7 postgresql-9
```

Then, merge and push this repo into your new app. Please be patient, this operation may last for a long time.

```
$ cd openerp/
$ git remote add upstream https://github.com/amon-ra/openshift-odoo-quickstart.git
$ git pull -s recursive -X theirs upstream 8.0
$ git push
```

That's it!

Now put your own modules in addons dir and do another 
```
git push
```

Now put your own modules in addons dir and do another 
```
git push
```

Point your browser to [https://openerp-$namespace.rhcloud.com](https://openerp-$namespace.rhcloud.com) and login.
Default credentials are:

```
Username: admin
Password: admin
```

## Upgrade

To use master version pull master on previus commands.
