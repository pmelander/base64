# base64
Provides full cross browser (and legacy browser) support for Base64 Encoding and Decoding true (not just merican) UTF-8 charset strings in Javascript. Will work with Base64 encoding and the UTF-8 charset on the .NET platform.

It's a complete wonder that we in 2020 still don't have a decent international charset support.

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
