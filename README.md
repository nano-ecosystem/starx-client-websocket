# Starx websocket client

# Usage

```
<!DOCTYPE html/>
<html>
<head>
	<title>ws test</title>
</head>
<body>
<script src="./protocol.js"></script>
<script src="./starx-wsclient.js"></script>
<script type="text/javascript">

var starx = window.starx

starx.init({host: "127.0.0.1", port: 3250, log: true}, function(){
	starx.request("gate.Handler.Login", {"name":"chrislonng", "age":10000}, function(data){
		console.log(data);
	});

	starx.request("gate.Handler.Signup", {"name":"Signup chrislonng", "age":10000}, function(data){
		console.log(data);
	});

	starx.on("notify", function(data){
		console.log(data);
	});
});

</script>
</body>
</html>

```

## Reference
[pomelo-jsclient-websocket](https://github.com/pomelonode/pomelo-jsclient-websocket)

##License
(The MIT License)

Copyright (c) 2012-2013 NetEase, Inc. and other contributors

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the 'Software'),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
