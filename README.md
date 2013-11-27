# Pusher Zapier Integration

This library provides integration with Pusher to Zapier. Right now it exposes the ability to trigger and event on a channel.

## How?

### Using existing libraries

It does this by combining a number of libraries and providing a `require` polyfill that doesn't exist in the Zapier runtime.

It combines:

* [pusher-node-server](https://github.com/pusher/pusher-node-server)
* [crypto-js](https://code.google.com/p/crypto-js/) (using MD5 and HMAC)

### A Zap

A zap needs to be creating so that anybody who wants to use Pusher with Zapier can provide details such as:

* bundle.auth_fields.app_id,
* bundle.auth_fields.app_key,
* bundle.auth_fields.app_secret
* bundle.action_fields[ 'event' ]
* bundle.action_fields[ 'channel' ]

The data that is triggered is the data created by the even in Zapier.

## TODO

* Automate the build of `pusher-zapier.js` by combining the required libraries
* Expose the Zap publicly in Zapier