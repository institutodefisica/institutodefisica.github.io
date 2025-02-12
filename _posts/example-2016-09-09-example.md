---
title: Profesores
date: 2016-09-09 17:07:00 Z
categories:
- Personal
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

**Imagen**

Mediante el texto `![ThisIsADemoPhoto](http://media.vector4free.com/normal/flat-banner-vectors.jpg)`
se introduce la imagen,  

![ThisIsADemoPhoto](http://media.vector4free.com/normal/flat-banner-vectors.jpg)
