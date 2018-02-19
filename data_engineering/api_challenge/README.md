# Data Engineering API Code Challenge

Implement a basic system responsible for consumption, storage, and retrieval of vehicle sale records. This system should have some interface so that it is convenient to interact with records; either an API or a system with accompanying client library is recommended.

## Vehicle Sale Records

There should be a persistent storage for vehicle sale records. Such records consist of a minimum of:

- VIN (17-digit vehicle identification number)
- Make
- Model
- Year
- Price
- Buyer
- Seller


For any single sale record, either the Buyer or Seller is an individual customer (with first name and last name, e.g. 'Bob Smith') and the other is a car dealership (with name and location, e.g. 'Rusnak BMW of Thousand Oaks'). That is, all sales are either from individual customer to car dealership OR from car dealership to individual customer.

### Inserting Records

* Records may be ingested in bulk or individually. Recommended means of bulk input include API POSTs or file uploads.

* Records should be persisted with consideration towards efficiency of storage and searching.

### Retrieving Records

**Records may be searched by filtering on parameters. For searching of records, consider the following use cases for the data:**

* Latest sales price of a specific vehicle (i.e. sales price by VIN)
* Historical sales price of a class of vehicles (i.e. sales price by Make/Model/Year)
* Transaction history for a specific dealership

The system should have an interface available to search persisted records and respond with the matching results. In the case of invalid searches, there should be proper error handling and/or error responses.

### Additional Considerations

**In the interests of time, it is not necessary to implement the following, but please answer how you may adjust your solution to accommodate the following issues:**

1. Security - How would you protect against outsiders from inserting/querying records?
1. Scalability - Would anything change if your system had 100 million vehicle sale records? What if the API had to handle 10 searches per second?
1. Data Integrity - How would you handle erroneous sale records data (e.g. malformed VINs, invalid field values)?
1. Auditability - How would you track the source of any incoming data as well as the source of any searches?

