# Section 2: Angular componentes, core directives and pipes

## Built-in Pipes

- converting date using pipe
```typescript
  //Start date: Jan 1, 2020
  <div> Start date: {{startDate | date}}
   
   //Start date: 01/01/2020
  <div> Start date: {{startDate | date: 'MM/dd/yyyy'}}
  
``` 

 - using uppercase in strings
  ```typescript
  //DENIS CAMINHA
  <div> {{user.name | uppercase}} </div>
  ```
  
 - setting numbers as floating using pipes
```typescript
  //10.99
  <div> {{ product.price | number: '3.1-2' }} </div>
```

 - percentage of a value
```typescript
  //67%
  <div> {{ percentValue = 0.67 | percent }} </div>
```
