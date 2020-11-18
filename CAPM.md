# CDS

## CDS Types:

- Predefined Types:
`UUID, Boolean, Integer, Decimal, Date, Time`
g
- Structured Types:
```
type Amount {
   value : Decimal(10,3);
   currency : Currency;
 }
 entity Books {
   price : Amount;
 }
```

- Arrayed Types:
```entity Foo { emails: many String; }
   entity Bar { emails: many { kind:String; address:String; }; }
   entity Car { emails: many EmailAddress; }
   entity Car { emails: EmailAddresses; }
   type EmailAddresses : many { kind:String; address:String; }
   type EmailAddress : { kind:String; address:String; }
```

- Default Values:
```
entity Foo {
     bar : String default 'bar';
     boo : Integer default 1;
   }
```

- Type References:
```
entity Author {
  firstname : String(100);
   lastname : type of firstname; // has type "String(100)"
}
```

- Constraints: 
```
entity Employees {
  name : String(111) not null;
}
```

- Enums: 
```
type Gender : String enum { male; female; }
entity Order {
  status : Integer enum {
    submitted =  1;
    fulfilled =  2;
    shipped   =  3;
    canceled  = -1;
  };
}
```




