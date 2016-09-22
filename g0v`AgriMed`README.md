backend_template
================


Usage
-----
project name/directory is recommended to fit python style (using underscore as project name/directory):

* good: backendTemp

git clone https://github.com/chhsiao1981/frontend_template.git .; ./scripts/init_dev.sh; . __/bin/activate; ./scripts/init_starter.sh; cp config.js.tmpl config.js; npm install; npm start

* start: ./scripts/init_starter.sh
* create a module: ./scripts/dev_module.sh


Introduction
-----
This template intends to efficiently develop with the following libraries:

* pcreate (scaffolding, from pylons pyramid)
* type / str / unicode
* timestamp (by millisecond) / sec_timestamp / datetime / arrow
* sniffer / nosetests (autotest)
* pymongo (db)
* grequests (http post/get)
* ujson (json)
* argparse
* pandas
* lock
* send email
* oauth2
* django
* django-rest-framework

All are welcome to improve this template


Django
-----
1. settings is set in [{{package}}:django] in .ini (with key lowercased)


python-social-auth
-----
1. For now, social-auth is for authentication only.
2. need to change data-clientid to the corresponding clientid in /static/login.html
3. need to change social\_auth\_google\_plus\_key and social\_auth\_google\_plus\_secret in .ini
4. The token on client-side should be revoked immediately once the ajax to login complete (success or error).
5. Once the ajax to login successfully complete, the response return \{id, username, first\_name, last\_time, url\}
6. tested /auth/complete/google-plus (/static/login.html)
