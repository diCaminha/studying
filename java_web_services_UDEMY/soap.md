## SOAP - Simple Object Access Protocol

![](images/soap.png?raw=true)


It's used to exchange information in the implementation of **web services**. It used **XML** as the format of documents and stays on application layer, most often **HTTP** as the path of information.

### Its Parts:
1. An envelope: which describes the structure of the content (skeleton)
2. Encoding rules
3. Convention for representing procedure calls and response

### WS Security

Is a extension to SOAP to apply security when exchanging information between applications. 

The current mechanism of security provided by the web (HTTPS) might be not enough to garantee all the requisites. So that's the security in the message layer.

It defines how to **attach a signature, to use crypt and also using tokens in messages SOAP**

The performance is affected by the WS Security, since there's a overhead to SOAP Processing due to the increased size of the message on the wire.


|  Security mechanism | Messages/second  |
|---|---|
| WS-Security (X.509) XML Signature & Encryption | 352  |
| WS-SecureConversation XML Signature & Encryption | 798 |
| Transport Layer Security  |  2918 |

------------------------

### WSDL

Suppose you are hired to develop a project for your company that will integrate with another system via Web Service from another Company. 

Aparently the first thing to do is to call them and ask for a pdf or something showing examples of calls for their web service. Or even you already have a document but just need to check if the document is not outdated.

All this process above would be skipped with the company works with a wsdl URL for their web service (Web Services Description Language).




references:

https://medium.com/@gabrielpolo/conhecendo-o-ws-security-c6c775b461fd

https://www.devmedia.com.br/wsdl-simplifique-a-integracao-de-dados-via-web-service/30066

