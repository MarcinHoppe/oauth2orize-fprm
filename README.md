# oauth2orize-fprm

[OAuth2orize](https://github.com/jaredhanson/oauth2orize) response mode plugin
providing support for [Form Post Response Mode](https://openid.net/specs/oauth-v2-form-post-response-mode-1_0.html).

This response mode uses the HTTP POST method instead of a redirect URI to return
authorization responses from the authorization server.

## Install

    $ npm install oauth2orize-fprm

## Usage

#### Add Response Mode

For each grant in which form post response mode is desired, add support by
passing a `modes` option containing form post response mode.  For example,
using the token grant:

```js
server.grant({ 
  modes: {
    form_post: require('oauth2orize-fprm')
  } }, 
  oauth2orize.grant.token(function(client, user, ares, done) {
    // TODO: issue token
  })
);
```

## Contributing

#### Tests

The test suite is located in the `test/` directory.  All new features are
expected to have corresponding test cases.  Ensure that the complete test suite
passes by executing:

```bash
$ make test
```

#### Coverage

All new feature development is expected to have test coverage.  Patches that
increse test coverage are happily accepted.  Coverage reports can be viewed by
executing:

```bash
$ make test-cov
$ make view-cov
```

## Support

#### Funding

This software is provided to you as open source, free of charge.  The time and
effort to develop and maintain this project is volunteered by [@jaredhanson](https://github.com/jaredhanson).
If you (or your employer) benefit from this project, please consider a financial
contribution.  Your contribution helps continue the efforts that produce this
and other open source software.

Funds are accepted via [PayPal](https://paypal.me/jaredhanson), [Venmo](https://venmo.com/jaredhanson),
and [other](http://jaredhanson.net/pay) methods.  Any amount is appreciated.

## License

[The MIT License](http://opensource.org/licenses/MIT)

Copyright (c) 2015-2017 Jared Hanson <[http://jaredhanson.net/](http://jaredhanson.net/)>
