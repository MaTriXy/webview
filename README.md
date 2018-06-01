This is a template project for Android Studio that allows you to create an android webview application in minutes. You can use it to create a simple app for your website or as a starting point for your HTML5 based android app.

### Getting started

[Download](https://github.com/slymax/webview/archive/master.zip) or clone this repository and import it into Android Studio.

### Using a remote source

If you want to create an app that displays the contents of a remote website

1. uncomment lines **31** and **32** in `MainActivity.java` and change `http://example.com` to match your remote source

	```
	mWebView.loadUrl("http://example.com");
    mWebView.setWebViewClient(new MyAppWebViewClient());
	```

2. open the `MyAppWebViewClient.java` file and replace `example.com` on line **12** with your custom url

	```
	if (Uri.parse(url).getHost().endsWith("example.com")) {
	```

### Using a local source

If you want to create a local HTML5 android app

1. uncomment line **35** in `MainActivity.java`

	```
	mWebView.loadUrl("file:///android_asset/demo/index.html");
	```

2. replace the demo project in `src/main/assets/demo/` with your own HTML, CSS and JavaScript files