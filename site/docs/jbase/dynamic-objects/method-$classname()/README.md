# Method: $classname()

**Created At:** 2/15/2018 2:07:35 PM  
**Updated At:** 9/15/2019 8:31:37 AM  
**Original Doc:** [method-classname](https://docs.jbase.com/42948-dynamic-objects/method-classname)  
**Original ID:** 299325  
**Internal:** No  

## Description

The **$classname()** method returns the name of the class as a text string.

## Syntax

```
var->$classname()
```

## Arguments

None

## Return values

The name of the class as a text string

A null return value indicates that either **var** is not an object or the object was created with no classname, e.g.

```
var = new object
crt dquote(var->$classname()) ;* displays ""
```

## Example

This mainline code creates a **book** object from a **Library** class, passing 2 arguments, book title and author, to the class's constructor method, then displays the JSON representation of the object:

```
$option jabba
book = new object("Library", "Phaedrus", "Plato")
crt "The class name is ":dquote(book->$classname()):"."
crt book->$tojson()
```

Here's the constructor for the **Library** class:

```
$option jabba
method Library::Library(title, author)
    this->title = title
    this->author = author
end method
```

Running the mainline code displays:

```
The class name is "Library".
{"title":"Phaedrus","author":"Plato"}
```

## Notes
