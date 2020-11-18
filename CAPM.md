#CDS

##CDS Types:

1. Predefined Types:
`UUID, Boolean, Integer, Decimal, Date, Time`
1. Structured Types:
`type Amount {
   value : Decimal(10,3);
   currency : Currency;
 }
 entity Books {
   price : Amount;
 }`

