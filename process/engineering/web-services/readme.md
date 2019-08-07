# Readme

* This is square one of a project
* Be clear about first installation vs. upgrade \(deploy vs. redeploy\)

## deploy

* List down / capture all dependencies
* `make && make install`
* Not in git
  * config
    * DB user/pass
    * 3rd party libs
    * i18n
  * migrations
    * schema \(migration 0\)
    * migrations
    * seed data

## redeploy

* `./upgrade`
  * stop service
  * migrate data
  * install new software
  * restart service

## deployment models

* **Proprietary**: an admin \(you?\) deploys an instance of a web service from git to a single location/server \(perhaps local cloud\) -- all users
* **Open Source**: admins deploy instances of a web service from git to different locations/servers, different users
* **Clustered**: admins \(perhaps you\) deploy load-balanced or separate instances of the service to multiple locations
* **Federated**: SendMail, XMPP, etc.
* **P2P**: Serverless \(not WS-lambda\) leaf node architecture with a seamless user-only deployment

## destinations \(all of which are distributed computing nodes\)

* servers
* phones
* desktops
* specialized hardware \(raspberry pi in the forest, bicycle sharing kiosks, etc.\)

