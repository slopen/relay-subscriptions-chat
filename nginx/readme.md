# setup nginx for local development / production

* add this line with proper path to /usr/local/etc/nginx/nginx.conf

	`include "%absolute-path-to-cloned-repo%/relay-subscriptions-chat/nginx/nginx.conf";`

* change the paths for ssl_certificate & ssl_certificate_key

	`ssl_certificate %absolute-path-to-cloned-repo%/relay-subscriptions-chat/nginx/ssl.crt;`

	`ssl_certificate_key %absolute-path-to-cloned-repo%/relay-subscriptions-chat/nginx/ssl.key;`

* restart nginx

	```
	$ sudo nginx -s stop
	$ sudo nginx
	```

* add this line to /etc/hosts

	`127.0.0.1 relay-subscriptions-chat`


NOTE: to change `mode` comment / uncomment `PRODUCTION` / `DEVELOPMENT` blocks
