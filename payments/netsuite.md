# NetSuite Engineer Take Home Exercise

## Scenario:
 
We have customer invoices being generated via webservice and some important information is stored in a field.
Let’s assume NetSuite Script ID for the field is simply `memo`.
 
Accounting team has reached out and asked us to extract information from the memo field and store them in separate fields.
 
Let’s assume the information stored in memo field was the following string.
`"Order ID: 9108 Subscription ID: 5223"`
 
We want to parse out Order ID and Subscription ID from the memo field and store them into custom field labeled “Order ID” (Script ID: `custbody_ff_order_id` ) and another custom field labeled “Subscription ID” (Script ID: `custbody_ff_subscription_id`)
 
## Test:
Please read the scenario above and write your solution 
  - Use SuiteScript 2.0 
  - Don't be shy about your design pattern
  - What happens if User Event on another record type was submitting this record?

## One extra step
Everything went well and your script was deployed successfully!
It turns out that `custbody_ff_order_id` ("Order ID") was a List/Record type field.
We'd like to be able to link the custom record.
  - Order Record has Script ID `customrecord_fair_order`
  - We store the Order ID in a field which has Script ID `custrecord_fair_order_id` and is unique per Order ID
