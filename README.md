# Tamper

**Important:** This extensions stopped working a while ago 😕 I'm working on a fix, should be available soon!

Tamper is a [Mitmproxy](http://www.mitmproxy.org) based devtools extension that lets you edit remote files locally and serve them directly to Chrome.

![Demo](https://github.com/dutzi/tamper/blob/master/assets/demo.gif)
### Using Tamper

Once installed, Tamper will add a new panel to your devtools, the "Tamper" panel. Similar to the Network panel, the Tamper panel shows you a list of all requests made by this page. Click on one of these network requests and the response Chrome got will open in your default editor. Make the changes you need and save the file. Once you hit refresh, Tamper will serve Chrome the file you just saved.

Tamper is based on the awesome Mitmproxy (man-in-the-middle proxy), or more precisely, libmproxy, its companion library that allows implementing powerful interception proxies.

### Installing

* Install Tamper's python script
```
sudo pip install tamper
```
* Install [Tamper's devtools extension](https://chrome.google.com/webstore/detail/tamper/mabhojhgigkmnkppkncbkblecnnanfmd)

### Developing

#### Chrome Extension

```bash
$ cd chrome-extension
$ npm install
$ bower install
```

Add an unpacked extension to Chrome:

1. Browse to about:extensions
2. Check the "Developer mode" checkbox
3. Click the "Load unpacked extension..." button
4. Choose the "app" folder

A new extension has been added to Chrome, copy the new extension's id.

Open ~/Library/Application Support/Google/Chrome/NativeMessagingHosts/com.dutzi.tamper.json and add the extension's id to the allowed_origins list. Now restart Chrome.

### Troubleshooting

Having issues installing Tamper? Check out the [troubleshooting page](https://github.com/dutzi/tamper/wiki/Troubleshooting).
