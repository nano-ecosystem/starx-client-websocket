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
