## JAX-WS lib

### Annotations

There are some core annotations that stays in the package: *javax.jws*

-  @Webservice

```java
@WebService
public class OrderService {
    //code here
}
```

it says that this class is a service that can receive requests.

- @WebMethod
```java
@WebMethod
@WebResult(name="order")
public Order_getOrder(@WebParam("orderId") Long orderId) {
    //code here
}
```
