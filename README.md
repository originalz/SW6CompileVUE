## Compile Storefront VueJS components in Shopware 6
```bash
docker machine > bin/console plugin:refresh
docker machine > bin/console plugin:install PLUGINNAME
docker machine > bin/console plugin:activate PLUGINNAME

docker machine > copy changed VueJS component files to machine

docker machine > npm run build
location       > plugindir/src/Resources/app/storefront/src/plugins/COMPONENT-NAME

docker machine > ./bin/build-storefront.sh

remote server  > copy compiled minified VueJS to server
location       > plugindir/src/Resources/app/storefront/src/plugins/COMPONENT-NAME/dist/COMPONENT-NAME.js
remote server  > copy compiled minified StorefrontJS to server
location       > plugindir/src/Resources/app/storefront/dist/storefront/js/full-plugin-name.js

remote server  > bin/console theme:compile
remote server  > bin/console cache:clear
```
