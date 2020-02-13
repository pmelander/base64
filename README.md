# base64
Provides full cross browser (and legacy browser) support for Base64 Encoding and Decoding true UTF-8 charset strings in Javascript. Will work with Base64 encoding and the UTF-8 charset on the .NET platform
## base64.encode in javascript
```javascript
var encodedString = base64.encode(decodedString)
```
_OR_
```javascript
var encodedString = btoa(decodedString)
```
## base64.decode in javascript
```javascript
var decodedString = base64.decode(encodedString)
```
_OR_
```javascript
var decodedString = atob(encodedString)
```
## encode in C#
```csharp
var encodedString = Convert.ToBase64String(Encoding.UTF8.GetBytes(decodedString))
```
## decode in C#
```csharp
var decodedString = Encoding.UTF8.GetString(Convert.FromBase64String(encodedString))
```
