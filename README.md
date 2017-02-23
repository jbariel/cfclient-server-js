# CF Client API Service
Create a simple web service to abstract the [CF API](https://apidocs.cloudfoundry.org)

## Getting started
It's very simple to get this project up and running:

* Clone the repo
* Install dependencies `npm install`
* Configure your `props.json`
* Run the project `node index.js`

### What it does
The app currently starts up on 
```
process.env.PORT || 8888
```
and then listens for a request.  You can visit a URL such as `http://localhost:8888/apps` and it will parse the context as `apps` and run the appropriate CF API call.  You can also do complex queries such as
```
http://localhost:8888/apps?q=name IN <appname>
```
to do things like search for an app with `<appname>`.  For this specific example, please look at the [API Reference](https://apidocs.cloudfoundry.org/241/apps/list_all_apps.html).

### JS CFClient
This project is based on the [js-cfclient](https://github.com/jbariel/js-cfclient) NPM.  See more information there.

### props.json
There is an example `props.json.example` file that you can copy/paste/update.  The parameters are:

* `protocol` => `http` or `https`
* `host` => FQDN or IP address of the PCF or CF host (e.g. `api.mydomain.com`)
* `username` => Username to access the api
* `password` => Password for the given username
* `skipSslValidation` => Set to `true` when using self-signed certs

# Issues
Please use the [Issues tab](../../issues) to report any problems or feature requests.
