# PN5_60900

<PageHeader />

## Description

Add extensions to Dynamic Objects per RFC 7159.

### Previous Release Behavior

The jBASE JSON parser worked strictly to the standard set by the ECMA-404 standard. See [https://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf](https://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf)

Since that standard was published, JSON has moved on, albeit very slightly and jBASE does not accept some incompatibilities caused by this latest revision. The definition of this standard can be found at [http://www.faqs.org/rfcs/rfc7159.html](http://www.faqs.org/rfcs/rfc7159.html)

The jBASE JSON parser insisted that the source text was an object or an array. The extension allows for the four primitive types to be represented as well as objects or arrays. The new revision notes this by saying:

## Note

>Certain previous specifications of JSON constrained a JSON text to be an object or an array.

### Current Release Behavior

A JSON source text can now accept the 4 primitive types of JSON as text, as well as objects and arrays as previously. For example:

```
   source = '"Hello World"'
 obj = source->$fromjson()
if obj->$isobject() then
   crt "We returned an object like this"
   crt obj->$tojson(1)
end else
   crt "We didn't return an object, we returned this"
   crt obj
end

[Screen output]

We didn't return an object, we returned this
Hello World
```

In the above example, the source for $fromjson() was neither an object nor array, so we don't return an object as such, hence $isobject() returns false. However, the source to $fromjson() is a recognised JSON primitive of "Hello World" and so we return the string "Hello World".

Back to [5.7.4 Release Notes](./../README.md)
