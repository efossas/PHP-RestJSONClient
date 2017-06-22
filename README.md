# PHP-RestJSONClient
A Restful PHP Class For Sending REST + JSON requests

### Usage

This class can send REST requests. The following arguments have setters & getters:

```
$method				- The HTTP method type
$url				- The endpoint.
$headers			- Any optonal HTTP headers to include.
#bodyjson			- Any variables to include. (not included in DELETE request)
$files				- A file to uplood. (Only used in PUT request)

$timeout			- number of seconds to try for a connection
$protocol_version	- HTTP/1.0 or HTTP/1.1
```

Example usage:

```
$myclient = new RestClient($method,$url,$headers,$bodyjson,files);

$myclient->set_all($method,$url,$headers,$bodyjson,$file); // or set individually with setter functions: set_PARAMETER($PARAMETER)

$response = $myclient->send();
```

### Notes

The client supports Basic Auth. It can handle all typical HTTP headers except for CONNECTION.