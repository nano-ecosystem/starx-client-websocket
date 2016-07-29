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

## License

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
