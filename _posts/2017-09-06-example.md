---
title: Biofísica
date: 2017-09-06 17:07:00 Z
categories:
- Posgrados
layout: post
author: PosgradosFisicaUdeA
---

Esta es una publicación de ejemplo para ilustrar las características del sitio [Postgrados Física](https://fisica.udea.edu.co).  

<!-- more -->

**Markdown Basico**  

El siguiente texto,  

```
Neque porro *quisquam* est, qui **dolorem** ipsum, quia ***dolor*** sit, amet,
[consectetur](http://cjdns.info/), adipisci velit.

 * lorem
 * ipsum

1. dolor
2. sit

```

Se renderiza como,  

Neque porro *quisquam* est, qui **dolorem** ipsum, quia ***dolor*** sit, amet, [consectetur](http://cjdns.info/), adipisci velit.  

 * lorem  
 * ipsum  

1. dolor  
2. sit  

**Citación o _Blockquote_**

Como dijo Benjamin Franklin, 

> "They who can give up essential liberty to obtain a little temporary safety, deserve neither liberty nor safety."
> 
> _Benjamin Franklin_

**Codigo fuente**

Ahora un método en `C++`

{% highlight c %}

static void asyncEnabled(Dict* args, void* vAdmin, String* txid, struct Allocator* requestAlloc)
{
    struct Admin* admin = Identity_check((struct Admin*) vAdmin);
    int64_t enabled = admin->asyncEnabled;
    Dict d = Dict_CONST(String_CONST("asyncEnabled"), Int_OBJ(enabled), NULL);
    Admin_sendMessage(&d, txid, admin);
}

{% endhighlight %}

**Tables**
Tables are very easy to write in markdown. Please check the following example (the extra : are for alignment of the columns)

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Check the result is the web page: https://institutodefisica.github.io/admision

**Imagen**

Mediante el texto `![ThisIsADemoPhoto](http://media.vector4free.com/normal/flat-banner-vectors.jpg)`
se introduce la imagen,  

![ThisIsADemoPhoto](http://media.vector4free.com/normal/flat-banner-vectors.jpg)
