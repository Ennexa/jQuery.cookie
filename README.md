# jQuery.cookie

Simple jQuery plugin for handling cookies. This is not a full fledged dependency management solution.


## Usage

### Set Cookie
```js
var value = 'Sample Cookie';
$.cookie('my-cookie-name', value);
```

By default the cookie created by `$.cookie` method will be a session cookie and will be automatically deleted at the end of the current browser session. If you want the cookie to persist beyond current session, you can specify a TTL in seconds using the expires option.

```js
var value = 'Sample Cookie';
// This cookie will persist for 1 hour (3600 seconds) and will not
// be deleted if the browser session is ended before the specified TTL
$.cookie('my-cookie-name', value, {expires: 3600});
```

### Read Cookie
```js
var value = $.cookie('my-cookie-name');
alert('Value of "my-cookie-name" is ' + value);
```

### Delete Cookie
A cookie can be deleted by passing null as its value. It can also be deleted by setting a negative value for `expires` option.

```js
var value = $.cookie('my-cookie-name');
alert('Value of "my-cookie-name" is ' + value);
```

## Options

Available options are

Parameter  | Description
-----------|----------
expires    | The cookie TTL in seconds
domain     | The domains from which the cookie is accessible. By default the cookie is accessible only from the same domain from which it is set. If you wish to allow access to the cookie from subdomains, use `'.yourdomain.com'`
path       | By default, the cookie is available only from the path where it was set. If you wish to access the cookie from location outside the path, set the path accordingly. Setting `path` to `/` will make the cookie available from the entire site.
secure     | Determines whether the cookie is available from `http` urls. 

## Credits

This plugin was created for [Prokerala.com](http://www.prokerala.com).