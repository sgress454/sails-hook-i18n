# sails-hook-wide-i18n

This is a fork of the [sails-hook-i18n](https://github.com/sgress454/sails-hook-i18n) hook from Scott Gress @sgress454

[Sails JS](http://sailsjs.org) hook to allow internationalization using the [i18n module](http://npmjs.org/packages/i18n).

This is essentially a port of the Sails v0.12.x core i18n hook.  Sails 1.0 uses the more lightweight [i18n-2 module](http://npmjs.org/packages/i18n-2), so if you're missing some of the features from `i18n`, this hook's for you!

### Installation

`npm install --save sails-hook-wide-i18n`

### Usage

See the [Sails internationalization docs](http://sailsjs.com/documentation/concepts/internationalization) for the basics of using i18n with Sails.

### Configuration

See the [i18n module README](http://npmjs.org/packages/i18n) for full documentation -- any property set on `sails.config.i18n` (in the `config/i18n.js` file) will be passed directly in to the `i18n` module.  Below are some common config properties.


| Property           | Type        | Default               | Details |
|--------------------|:-----------:|-----------------------|---------|
| `locales`          | ((array))   | ['en','es','fr','de'] | List of supported [locale codes](http://en.wikipedia.org/wiki/BCP_47)
| `localesDirectory` | ((string))  | '/config/locales'     | The project-relative path to the folder containing your locale translations (i.e. stringfiles)
| `defaultLocale`    | ((string))  | 'en'                  | The default locale for the site. Note that this setting will be overridden for any request that sends an "Accept-Language" header (i.e. most browsers), but it's still useful if you need to localize the response for requests made by non-browser clients (e.g. cURL).
| `updateFiles`      | ((boolean)) | false                 | Whether to automatically add new keys to locale (translation) files when they are encountered during a request.
