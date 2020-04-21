## Notes about Java Web Services course in Udemy
### link: https://www.udemy.com/course/java-web-services/?deal_code=&utm_source=aff-campaign&utm_medium=udemyads&utm_term=Homepage&utm_content=Textlink&utm_campaign=Admitad-default&admitad_uid=ffc0be993b2a2efb4a3364860685f26e

**What are XML services?**

The format xml is used to exchange information throught the internet for direct application-to-application communication;

**The difference XML and HTML**

XML was designed to hold data, instead HTML focus on display data. Also, the tags in xml file are not predefined as in HTML.

**Note:** 

The XML file must have a root element that is the parent of all others elements;
example:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<note>
  <to>Tove</to>
  <from>Jani</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
</note>
```

the <note> is the root element.


Note: the XML prolog
<?xml version="1.0" encoding="UTF-8"?>
it is optional.
UTF-8 is the default for XML files.


Note: XML tags are case sensitive.


What's the difference between element and attribute?
r: the attributes is information related to the element. The value of the attribute goes inside the tag. The elements inside an element are like
a more complex attributes for the element parent. Take a look at the example below:

info gender as attribute:
<person gender="female">
  <firstname>Anna</firstname>
  <lastname>Smith</lastname>
</person>

info gender as element:
```xml
<person>
  <gender>female</gender>
  <firstname>Anna</firstname>
  <lastname>Smith</lastname>
</person>
```