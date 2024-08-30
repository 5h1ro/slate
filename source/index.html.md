---
title: Kasirpintar WA v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers:
  - <a href="https://kasirpintar.co.id">Find out our organic company.</a>
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="kasirpintar-wa">Kasirpintar WA v1.0.0</h1>
Welcome to the Woowa API V3.0! You can use our API to access Woowa API endpoints, which can send message,image also file and get information of your account at my.woo-wa.com.
We have language bindings in PHP! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.
This is Demo account to try our API
license : 5c286f20169dd key : db63f52c1a00d33cf143524083dd3ffd025d672e255cc688
You can get new data account (token) at https://woo-wa.com

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

# Introduction
Welcome to the Woowa API V3.0! You can use our API to access Woowa API endpoints, which can send message,image also file and get information of your account at my.woo-wa.com.
We have language bindings in PHP! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.
This is Demo account to try our API
license : 5c286f20169dd key : db63f52c1a00d33cf143524083dd3ffd025d672e255cc688
You can get new data account (token) at https://woo-wa.com

Base URLs:

* <a href="https://wa.kpntr.com/backend/">https://wa.kpntr.com/backend/</a>

* <a href="https://kpwa.kpntr.com/backend/">https://kpwa.kpntr.com/backend/</a>

# Authentication

* API Key (Token)
    - Parameter Name: **X-API-KEY**, in: header. You can get API key from dashboard

<h1 id="kasirpintar-wa-api">API</h1>

All of open api endpoint

## Restart Service

<a id="opIdrestart"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://wa.kpntr.com/backend/openapi/wa/restart \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
GET https://wa.kpntr.com/backend/openapi/wa/restart HTTP/1.1
Host: wa.kpntr.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/restart',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.get 'https://wa.kpntr.com/backend/openapi/wa/restart',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.get('https://wa.kpntr.com/backend/openapi/wa/restart', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://wa.kpntr.com/backend/openapi/wa/restart', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/restart");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://wa.kpntr.com/backend/openapi/wa/restart", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /openapi/wa/restart`

*Restart service*

Restart specified service with license

> Example responses

> 200 Response

```json
{
  "message": "string",
  "status": "qr",
  "code": null
}
```

<h3 id="restart-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="restart-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» status|string|true|none|none|
|» code|any|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|qr|
|status|ready|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Token
</aside>

## Check Service Status

<a id="opIdcheckStatus"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://wa.kpntr.com/backend/openapi/wa/status \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
POST https://wa.kpntr.com/backend/openapi/wa/status HTTP/1.1
Host: wa.kpntr.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/status',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.post 'https://wa.kpntr.com/backend/openapi/wa/status',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.post('https://wa.kpntr.com/backend/openapi/wa/status', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://wa.kpntr.com/backend/openapi/wa/status', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/status");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://wa.kpntr.com/backend/openapi/wa/status", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /openapi/wa/status`

*Check status*

Check status service by license.

> Example responses

> 200 Response

```json
{
  "message": "string",
  "status": "qr",
  "code": null
}
```

<h3 id="checkstatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="checkstatus-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» status|string|true|none|none|
|» code|any|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|qr|
|status|connected|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Token
</aside>

## Scan QR

<a id="opIdscanQR"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://wa.kpntr.com/backend/openapi/wa/login-qr \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
POST https://wa.kpntr.com/backend/openapi/wa/login-qr HTTP/1.1
Host: wa.kpntr.com
Content-Type: application/x-www-form-urlencoded
Accept: application/json

```

```javascript
const inputBody = '{
  "responseAs": "image"
}';
const headers = {
  'Content-Type':'application/x-www-form-urlencoded',
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/login-qr',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded',
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.post 'https://wa.kpntr.com/backend/openapi/wa/login-qr',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/x-www-form-urlencoded',
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.post('https://wa.kpntr.com/backend/openapi/wa/login-qr', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/x-www-form-urlencoded',
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://wa.kpntr.com/backend/openapi/wa/login-qr', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/login-qr");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/x-www-form-urlencoded"},
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://wa.kpntr.com/backend/openapi/wa/login-qr", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /openapi/wa/login-qr`

*Scan QR*

Scan QR code to login whatsapp

> Body parameter

```yaml
responseAs: image

```

<h3 id="scanqr-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» responseAs|body|string|false|You can specify choice return as image or string base64|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» responseAs|image|
|» responseAs|string|

> Example responses

> 200 Response

```json
{
  "message": "string",
  "qr_string": "string",
  "code": null
}
```

<h3 id="scanqr-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="scanqr-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» qr_string|string|true|none|none|
|» code|any|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Token
</aside>

## Check Phone Number

<a id="opIdcheckNumber"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber} \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
GET https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber} HTTP/1.1
Host: wa.kpntr.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.get 'https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.get('https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://wa.kpntr.com/backend/openapi/wa/check-number/{phoneNumber}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /openapi/wa/check-number/{phoneNumber}`

*Check number*

Check number whatsapp is available to send message

<h3 id="checknumber-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|phoneNumber|path|string|true|Menghapus semua karakter selain angka. Lalu, jika diawali 0, maka angka 0 tersebut diganti dengan 62|

#### Detailed descriptions

**phoneNumber**: Menghapus semua karakter selain angka. Lalu, jika diawali 0, maka angka 0 tersebut diganti dengan 62

<br>
Examples :
<br>
| Input | Read as |
<br>
| --- | --- |
<br>
| `081234567890`, `0812 3456 7890`, `0812-3456-7890`, `6281234567890`, `62812 3456 7890` | `6281234567890` |
<br>
| `81234567890`, `812 3456 7890`, `812-3456-7890` | `81234567890` |

> Example responses

> 200 Response

```json
{
  "message": "string",
  "is_registered": true,
  "code": null
}
```

<h3 id="checknumber-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="checknumber-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» is_registered|boolean|true|none|none|
|» code|any|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Token
</aside>

## Send Message

<a id="opIdsendMessage"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://wa.kpntr.com/backend/openapi/wa/message \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
POST https://wa.kpntr.com/backend/openapi/wa/message HTTP/1.1
Host: wa.kpntr.com
Content-Type: application/x-www-form-urlencoded
Accept: application/json

```

```javascript
const inputBody = '{
  "phoneNumber": "string",
  "message": "string",
  "imageUrl": "string"
}';
const headers = {
  'Content-Type':'application/x-www-form-urlencoded',
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/message',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded',
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.post 'https://wa.kpntr.com/backend/openapi/wa/message',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/x-www-form-urlencoded',
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.post('https://wa.kpntr.com/backend/openapi/wa/message', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/x-www-form-urlencoded',
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://wa.kpntr.com/backend/openapi/wa/message', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/message");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/x-www-form-urlencoded"},
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://wa.kpntr.com/backend/openapi/wa/message", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /openapi/wa/message`

*Send message*

Send message to some number

> Body parameter

```yaml
phoneNumber: string
message: string
imageUrl: string

```

<h3 id="sendmessage-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» phoneNumber|body|string|true|Menghapus semua karakter selain angka. Lalu, jika diawali 0, maka angka 0 tersebut diganti dengan 62|
|» message|body|string|false|none|
|» imageUrl|body|string|false|You can add an image URL and make sure your image is not transparent|

#### Detailed descriptions

**» phoneNumber**: Menghapus semua karakter selain angka. Lalu, jika diawali 0, maka angka 0 tersebut diganti dengan 62

<br>
Examples :
<br>
| Input | Read as |
<br>
| --- | --- |
<br>
| `081234567890`, `0812 3456 7890`, `0812-3456-7890`, `6281234567890`, `62812 3456 7890` | `6281234567890` |
<br>
| `81234567890`, `812 3456 7890`, `812-3456-7890` | `81234567890` |

> Example responses

> 200 Response

```json
{
  "message": "string",
  "result": {
    "id": "string",
    "body": "string",
    "from": "string",
    "to": "string",
    "media_url": "string",
    "created_at": "string"
  },
  "code": null
}
```

<h3 id="sendmessage-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|code possible value:
- 20001|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="sendmessage-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» result|object|true|none|none|
|»» id|string|true|none|none|
|»» body|string|true|none|none|
|»» from|string|true|none|none|
|»» to|string|true|none|none|
|»» media_url|string¦null|true|none|none|
|»» created_at|string|true|none|format "YYYY-MM-DD HH:mm:ss"|
|» code|any|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
Token
</aside>

## Send Message to Group

> Code samples

```shell
# You can also use wget
curl -X POST https://wa.kpntr.com/backend/openapi/wa/message-group \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
POST https://wa.kpntr.com/backend/openapi/wa/message-group HTTP/1.1
Host: wa.kpntr.com
Content-Type: application/x-www-form-urlencoded
Accept: application/json

```

```javascript
const inputBody = '{
  "groupName": "string",
  "message": "string",
  "imageUrl": "string"
}';
const headers = {
  'Content-Type':'application/x-www-form-urlencoded',
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/message-group',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded',
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.post 'https://wa.kpntr.com/backend/openapi/wa/message-group',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/x-www-form-urlencoded',
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.post('https://wa.kpntr.com/backend/openapi/wa/message-group', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/x-www-form-urlencoded',
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://wa.kpntr.com/backend/openapi/wa/message-group', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/message-group");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/x-www-form-urlencoded"},
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://wa.kpntr.com/backend/openapi/wa/message-group", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /openapi/wa/message-group`

> Body parameter

```yaml
groupName: string
message: string
imageUrl: string

```

<h3 id="post__openapi_wa_message-group-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» groupName|body|string|true|must exist|
|» message|body|string|false|must exist if imageUrl doesnt exist|
|» imageUrl|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "message": "string",
  "result": {
    "id": "string",
    "body": "string",
    "from": "string",
    "to": "string",
    "media_url": "string",
    "created_at": "string"
  },
  "code": 0
}
```

<h3 id="post__openapi_wa_message-group-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|code possible value:
- 20001|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="post__openapi_wa_message-group-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» result|object|true|none|none|
|»» id|string|true|none|none|
|»» body|string|true|none|none|
|»» from|string|true|none|none|
|»» to|string|true|none|none|
|»» media_url|string¦null|true|none|none|
|»» created_at|string|true|none|format "YYYY-MM-DD HH:mm:ss"|
|» code|any|true|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|

Status Code **504**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
APIKey
</aside>

## Webhook

> Code samples

```shell
# You can also use wget
curl -X POST https://wa.kpntr.com/backend/openapi/wa/webhook \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
POST https://wa.kpntr.com/backend/openapi/wa/webhook HTTP/1.1
Host: wa.kpntr.com
Content-Type: application/x-www-form-urlencoded
Accept: application/json

```

```javascript
const inputBody = '{
  "webhook": "string"
}';
const headers = {
  'Content-Type':'application/x-www-form-urlencoded',
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/webhook',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded',
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.post 'https://wa.kpntr.com/backend/openapi/wa/webhook',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/x-www-form-urlencoded',
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.post('https://wa.kpntr.com/backend/openapi/wa/webhook', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/x-www-form-urlencoded',
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://wa.kpntr.com/backend/openapi/wa/webhook', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/webhook");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/x-www-form-urlencoded"},
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://wa.kpntr.com/backend/openapi/wa/webhook", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /openapi/wa/webhook`

Menambahkan link webhook pada table license

> Body parameter

```yaml
webhook: string

```

<h3 id="post__openapi_webhook-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» webhook|body|string|true|url webhook|

> Example responses

> 200 Response

```json
{
  "message": "string",
  "code": 0
}
```

<h3 id="post__openapi_webhook-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|code possible value:
- 20001|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="post__openapi_webhook-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» code|integer|true|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
APIKey
</aside>

## Reset Webhook

> Code samples

```shell
# You can also use wget
curl -X GET https://wa.kpntr.com/backend/openapi/wa/webhook/reset \
  -H 'Accept: application/json' \
  -H 'X-API-KEY: API_KEY'

```

```http
GET https://wa.kpntr.com/backend/openapi/wa/webhook/reset HTTP/1.1
Host: wa.kpntr.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'X-API-KEY':'API_KEY'
};

fetch('https://wa.kpntr.com/backend/openapi/wa/webhook/reset',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-KEY' => 'API_KEY'
}

result = RestClient.get 'https://wa.kpntr.com/backend/openapi/wa/webhook/reset',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'X-API-KEY': 'API_KEY'
}

r = requests.get('https://wa.kpntr.com/backend/openapi/wa/webhook/reset', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'X-API-KEY' => 'API_KEY',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://wa.kpntr.com/backend/openapi/wa/webhook/reset', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://wa.kpntr.com/backend/openapi/wa/webhook/reset");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "X-API-KEY": []string{"API_KEY"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://wa.kpntr.com/backend/openapi/wa/webhook/reset", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /openapi/wa/webhook/reset`

> Example responses

> 200 Response

```json
{
  "message": "string",
  "status": "qr",
  "code": 0
}
```

<h3 id="get__openapi_webhook_reset-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Error|[default-400-schema](#schemadefault-400-schema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|[default-401-schema](#schemadefault-401-schema)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|[default-500-schema](#schemadefault-500-schema)|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Timeout|[default-504-schema](#schemadefault-504-schema)|

<h3 id="get__openapi_webhook_reset-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|
|» status|string|true|none|none|
|» code|[code-schema](#schemacode-schema)|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|qr|
|status|connected|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|

Status Code **504**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
APIKey
</aside>

# Schemas

<h2 id="tocS_default-400-schema">default-400-schema</h2>
<!-- backwards compatibility -->
<a id="schemadefault-400-schema"></a>
<a id="schema_default-400-schema"></a>
<a id="tocSdefault-400-schema"></a>
<a id="tocsdefault-400-schema"></a>

```json
{
  "message": "string",
  "errors": [
    "string"
  ],
  "code": null
}

```

### Properties

oneOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» message|string|true|none|none|
|» errors|[string]|true|none|none|
|» code|[code-schema](#schemacode-schema)|true|none|none|

xor

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» message|string|true|none|none|
|» code|[code-schema](#schemacode-schema)|true|none|none|

<h2 id="tocS_default-401-schema">default-401-schema</h2>
<!-- backwards compatibility -->
<a id="schemadefault-401-schema"></a>
<a id="schema_default-401-schema"></a>
<a id="tocSdefault-401-schema"></a>
<a id="tocsdefault-401-schema"></a>

```json
{
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|message|string|true|none|none|

<h2 id="tocS_default-500-schema">default-500-schema</h2>
<!-- backwards compatibility -->
<a id="schemadefault-500-schema"></a>
<a id="schema_default-500-schema"></a>
<a id="tocSdefault-500-schema"></a>
<a id="tocsdefault-500-schema"></a>

```json
{
  "message": "string",
  "error": "string",
  "code": null
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|message|string|true|none|none|
|error|string|true|none|none|
|code|[code-schema](#schemacode-schema)|true|none|none|

<h2 id="tocS_default-504-schema">default-504-schema</h2>
<!-- backwards compatibility -->
<a id="schemadefault-504-schema"></a>
<a id="schema_default-504-schema"></a>
<a id="tocSdefault-504-schema"></a>
<a id="tocsdefault-504-schema"></a>

```json
{
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|message|string|true|none|none|

