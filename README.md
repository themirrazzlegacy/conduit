# Conduit
An open-source Kahoot! clone

## How to set up
You'll need either `git` or a program to extract ZIPs. You'll also need [Nodejs](https://nodejs.org/) and [NPM](https://npmjs.com/) installed.
You'll need to either `git clone` this repository or download as a ZIP and extract the files.
Once in the folder with the source, run `npm install`.
Then, just run `npm init` to start the system.

## The `.conduit.json` file
This is a configuration file used to configure Conduit. The default file looks like this:
```json
{
   "secure_port": 443,
   "http_port": 80,
   "secure_response": "none",
   "http_response": "index",
   "ssl_private_key": null,
   "ssl_public_key": null
}
```
The possible values for "secure_response" and "http_response" are:
* `index` - aka the client/editor/manager
* `redirect_to_secure` - redirect to secure version
* `none` - does not listen at all

Change `ssl_private_key` and `ssl_public_key` to a file path if you want to use the secure version.

## Accessing Conduit
For testing, you'll visit `127.0.0.1` or `localhost`. In some cases, you can visit `localho.st` (depending on your /etc/hosts file and DNS server).
We're using `127.0.0.1` in the examples.
