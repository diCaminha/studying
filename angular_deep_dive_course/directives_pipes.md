# Section 2: Angular componentes, core directives and pipes

## Built-in Pipes

- converting date using pipe
```typescript
  //Start date: Jan 1, 2020
  <div> Start date: {{startDate | date}}
   
   //Start date: 01/01/2020
  <div> Start date: {{startDate | date: 'MM/dd/yyyy'}}
  

``` 

