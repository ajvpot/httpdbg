# httpdbg
A Golang library for logging and visualizing HTTP requests. 

### Features
* Provides a simple wrapper for an http.RoundTripper, making it easy to integrate with existing applications.
* Presentation of a Chrome Dev Tools server for viewing the requests in a familiar tool.

### Installation

### Usage

### Contributing
If you find a bug or have a feature request, please open an issue or a pull request on the GitHub repository.

### License
`httpdbg` is released under the Apache 2 license. See [LICENSE](https://github.com/ajvpot/httpdbg/blob/main/LICENSE).

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
