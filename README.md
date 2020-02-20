# base64
Provides full cross browser (and legacy browser) support for Base64 Encoding and Decoding true (not just merican) UTF-8 charset strings in Javascript. Will work with Base64 encoding and the UTF-8 charset on the .NET platform.

It's a complete wonder that we in 2020 still don't have a decent international charset support for a standard nearly 30 years old, used by the majority of the world.

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
var encodedString = Convert.ToBase64String(Encoding.UTF8.GetBytes(HttpUtility.UrlEncode(decodedString)))
```
## decode in C#
```csharp
var decodedString = HttpUtility.UrlDecode(Encoding.UTF8.GetString(Convert.FromBase64String(encodedString)))
```
## C# Extension for string
```csharp
public static class StringExtensions
{
    public static string Base64Encode(this string str) =>
        Convert.ToBase64String(Encoding.UTF8.GetBytes(HttpUtility.UrlEncode(str ?? string.Empty)));

    public static string Base64Decode(this string str) =>
        HttpUtility.UrlDecode(Encoding.UTF8.GetString(Convert.FromBase64String(str)));
}
```
#### Usage
```csharp
var encodedString = "Decoded string".Base64Encode()
```csharp
var decodedString = "RW5jb2RlZCUyMHN0cmluZw==".Base64Decode()
```
