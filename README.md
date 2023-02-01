# httpdbg
`httpdbg` is a wrapper for an `http.RoundTripper` that logs requests and presents a Chrome Dev Tools server for viewing them.

### Notes
* http.Client middleware (RoundTripper?) for chromedp logging of network requests
	* https://www.gmarik.info/blog/2019/cdp-proxy-chrome-devtools-proxy-middleware-golang/
	* attach callsites in metadata somehow?
	* https://pkg.go.dev/github.com/mafredri/cdp#section-readme
	* https://github.com/chromedp/chromedp
	* https://chromedevtools.github.io/devtools-protocol/tot/Network/#event-webSocketFrameReceived:~:text=setRequestInterception%20EXPERIMENTALDEPRECATED-,Events,-Network.dataReceived
	* requests (http.Client)
		* instrument roundtripper, defaultclient
		* https://pkg.go.dev/net/http#RoundTripper
	* websockets?
		* could hijack dialer and reroute it directly to a gorilla handler
		* https://github.com/koding/websocketproxy/blob/master/websocketproxy.go
