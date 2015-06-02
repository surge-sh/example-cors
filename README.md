# CORS example

An example using [Cross-Origin Resource Sharing](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS) via [a CORS file on Surge](https://surge.sh/help).

**Note** `CORS` support will be a paid feature on Surge in the near future. When you publish, you’ll be prompted to upgrade your project if you haven’t already. If you have any questions, just mention [@surge_sh](https://twitter.com/surge_sh) on Twitter.

## Getting started

Cross-Origin Resource Sharing, or CORS, allows you to serve static resources from a project you have on Surge, to sites and applications you have on other domains. This is done by adding a `CORS` file (no extension) in the root of the directory you want to publish.

First, install Surge globally using your terminal:

```sh
npm install --global surge
```

### Adding a `CORS` file

Next, create a `CORS` file using your favourite text editor, or the command line:

```sh
touch CORS
```

Allow your fonts, SVG files, and other resources to be accessed client-side from __any__ other domain, by adding `*` into the `CORS` file:

```
*
```

You can also create this file and add `*` into it, all with one command:

```
echo '*' > CORS
```

### Adding CORS for specific domains only

If you want your resources to be setup for CORS, but only with a specific, other domain, you may list it in the `CORS` file instead. For example:

```
https://blog.example.com
```

You may also list multiple domains in the file:

```
https://blog.example.com
https://example.com
https://surge.sh
```

### Publishing your project

Your project should now have a `CORS` file inside the root of the directory you are going to deploy. [Publish it by running `surge ./path/to/my-project`](https://surge.sh/help/getting-started-with-surge):

```
surge ./src
```

**Note** This will be a paid feature on Surge in the near future. When you publish, you’ll be prompted to upgrade your project if you haven’t already. Questions? Just mention [@surge_sh](https://twitter.com/surge_sh) on Twitter!

[Here are the results](http://client.cors-api.appspot.com/client#?client_method=GET&client_credentials=false&server_url=http%3A%2F%2Fexample-cors.surge.sh%2Fsourcesanspro-black.woff2&server_enable=true&server_status=200&server_credentials=false&server_tabs=remote) of requesting the `.woff2` file on in this project using [test-cors.org](http://test-cors.org).

Now, your project is live on the web with CORS support.

## License

Source Code Pro is included with this project, and is Copyright © 2010, 2012, 2014 [Adobe Systems Incorporated](http://www.adobe.com/) and available under [the SIL License](https://github.com/adobe-fonts/source-sans-pro/blob/master/LICENSE.txt).

[The MIT License (MIT)](LICENSE.md)

Copyright © 2015 [Chloi Inc.](http://chloi.io)
