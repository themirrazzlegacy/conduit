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
We're using `127.0.0.1` in the examples, but feel free to choose whichever one you prefer.

> Free tip: you can give yourself a custom domain if you edit the `/etc/hosts` file. On Linux and MacOS, it's in... `/etc/hosts`. On Windows, its prob in some folder under `system32`

To access the **Conduit Dashboard**, you can visit `127.0.0.1/dashboard/`. The dashboard lets you manage all of your quizzes and your account. Note to use Conduit, it doesn't require an account to host a session!

To join a **Conduit Live** session, you can visit `127.0.0.1/live/` to join a Conduit Live session.

To access the **Conduit Quiz Editor**, you can either go to the dashboard and click the `New Quiz` button, or you can visit `127.0.0.1/editor/` - remember you don't need an account to edit, host or play. You only need an account to share your quizzes and save them to the server you're hosting Conduit on.

To host a game via the **Conduit Live Console**, click the `Conduit Live` button
