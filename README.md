#PerseusAPI

How to connect the Perseus API

##Menu
[Searching](#searching)

##Searching

###URL:
http://catalog.perseus.org/catalog.atom?q={query}&search_field={field}

###Parameters:
| Parameter | Value
|-----------|-----------
| q | <i>text</i>
| search_field | title<br>author<br>urn

###Examples:
|Type|URL
|----|------------------------------
| Keyword search (All Fields): | http://catalog.perseus.org/catalog.atom?q=Homer
| URN search (URN Field): | http://catalog.perseus.org/catalog.atom?&q=tlg0012&search_field=urn
| Author search (Author Field): | http://catalog.perseus.org/catalog.atom?&q=Homer&search_field=author
| Title search (Title Field): |http://catalog.perseus.org/catalog.atom?&q=Iliad&search_field=title
