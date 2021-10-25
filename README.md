# Rest Client and curl
The other alternatives to request testing with Postman are REST Client Extension and curl command. If you are the person that get boring of open Postman while testing REST API, I recommend REST Client Extension in vscode.

## Rest Client Extension
After downloading this extension, you can start creating request file with .http extension.
```
// rest.http
https://swapi.dev/api/people/3
```
You can use either .http or .txt, but the REST Client extension can detect .http and pop up the "Send Request" message. Therefore, it is more convenient to use .http than .txt.

For .txt, you need to run command palette (Ctrl + Shift + P) and use "REST Client: Send Request".

### Basic Syntax
- use `###` to separate requests
- both lowercase and uppercase are allowed for request type (POST or post)

### GET request
```
https://swapi.dev/api/people/3

### separate between request

GET https://swapi.dev/api/planets/3/

### or

get https://swapi.dev/api/planets/3/
```

### Post request
```
POST https://example.com/comments HTTP/1.1
Content-Type: application/xml
Authorization: token xxx

<request>
    <name>sample</name>
    <time>Wed, 21 Oct 2015 18:27:50 GMT</time>
</request>

### send json body

POST https://example.com/comments HTTP/1.1
Content-Type: application/json

{
    "userId": "123",
    "name": "Chitsaunpong"
}

```
### Variables
```
@hostname = https://swapi.dev/api

{{hostname}}/people/3

###

GET {{hostname}}/planets/3/
```

## Fake API resources
- [JSON Placeholder](https://jsonplaceholder.typicode.com/)
- [The Star Wars API](https://swapi.dev/)