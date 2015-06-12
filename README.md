#PerseusAPI

How to connect the Perseus API and receive ancient texts...
Every text, edition and verse has a URN for identification.

##Menu
[Searching](#searching)
[References](#references)

##Searching

Search texts by title, author or URN.

###URL:
http://catalog.perseus.org/catalog.atom?q={query}&search_field={field}

###Parameters:
| Parameter | Value
|-----------|-----------
| q | <i>query</i>
| search_field | title<br>author<br>urn

###Examples:
|Type|URL
|----|------------------------------
| Keyword search (All Fields): | http://catalog.perseus.org/catalog.atom?q=Homer
| URN search (URN Field): | http://catalog.perseus.org/catalog.atom?&q=tlg0012&search_field=urn
| Author search (Author Field): | http://catalog.perseus.org/catalog.atom?&q=Homer&search_field=author
| Title search (Title Field): |http://catalog.perseus.org/catalog.atom?&q=Iliad&search_field=title

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
| Get brother verses of a verse | http://www.perseus.tufts.edu/hopper/CTS?request=GetValidReff&urn=urn:cts:greekLit:tlg0012.tlg001.perseus-grc1:1.1
