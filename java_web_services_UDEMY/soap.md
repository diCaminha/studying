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

references:

https://medium.com/@gabrielpolo/conhecendo-o-ws-security-c6c775b461fd

