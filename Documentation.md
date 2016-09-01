#PerseusAPI

How to connect to the Perseus API.<br>
Every text, edition, verse and paragraph has a URN for identification.

##Menu
[Searching](#searching)<br>
[References](#references)<br>
[Passages](#passages) (Get texts)<br>

##Searching

###Search Suggestions

Search suggestions when typing a query.

####URL:
http://catalog.perseus.org/catalog/opensearch.json?q={query}

####Parameters:
| Parameter | Value | Info
|-----------|-----------|-----------
| q | <i>query</i> | Optional

####Examples:
|Type|URL
|----|------------------------------
| Suggestions: | http://catalog.perseus.org/catalog/opensearch.json?q=Homer

###Search Records

Supported returned formats:
 - HTML
 - Atom
 - RSS

The format of the returned file while searching can be set as followed:

As parameter:
 - ?format=html
 - ?format=atom
 - ?format=rss

As extension:
 - /catalog.html
 - /catalog.atom
 - /catalog.rss

###Search Records (Atom XML)

Search texts by title, author or URN.

####URL:
http://catalog.perseus.org/catalog.atom?q={query}&search_field={field}<br>
http://catalog.perseus.org/catalog?q={query}&format=atom&search_field={field}

####Parameters:
| Parameter | Value | Info
|-----------|-----------|-----------
| per_page | <i>number</i> | Optional
| q | <i>query</i> | Optional
| search_field | title<br>author<br>urn | Optional
| sort | <i>...</i> | Optional

####Examples:
|Type|URL
|----|------------------------------
| Keyword search (All Fields): | http://catalog.perseus.org/catalog.atom?q=Homer
| URN search (URN Field): | http://catalog.perseus.org/catalog.atom?&q=tlg0012&search_field=urn
| Author search (Author Field): | http://catalog.perseus.org/catalog.atom?&q=Homer&search_field=author
| Title search (Title Field): |http://catalog.perseus.org/catalog.atom?&q=Iliad&search_field=title

###Search Record (RSS XML)

Soon

##References

Get URNs of all verses of a book by a book URN or a brother-verse URN. (More INFO about this coming soon...)

###URL:
http://www.perseus.tufts.edu/hopper/CTS?request=GetValidReff&urn={urn}

###Parameters:
| Parameter | Value
|-----------|-----------
| request | GetValidReff
| urn | <i>urn</i>

###Examples:
|Type|URL
|----|------------------------------
| Get sub verses of the book | http://www.perseus.tufts.edu/hopper/CTS?request=GetValidReff&urn=urn:cts:greekLit:tlg0012.tlg001
| Get brother verses of the verse | http://www.perseus.tufts.edu/hopper/CTS?request=GetValidReff&urn=urn:cts:greekLit:tlg0012.tlg001.perseus-grc1:1.1

##Passages

###URL:
http://www.perseus.tufts.edu/hopper/CTS?request=GetPassage&urn={urn}

###Parameters:
| Parameter | Value
|-----------|-----------
| request | GetPassage
| urn | <i>urn</i>

###Examples:
|Type|URL
|----|------------------------------
| Get a text paragraph | http://www.perseus.tufts.edu/hopper/CTS?request=GetPassage&urn=urn:cts:greekLit:tlg0012.tlg001
| Get a sentence | http://www.perseus.tufts.edu/hopper/CTS?request=GetPassage&urn=urn:cts:greekLit:tlg0012.tlg001.perseus-grc1:1.1
