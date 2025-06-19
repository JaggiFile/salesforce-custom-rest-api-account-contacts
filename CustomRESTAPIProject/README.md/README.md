# Salesforce Custom REST API Project - Account with Contacts

This project demonstrates how to create and test a Custom REST API in Salesforce using Apex that returns an Account along with all its related Contacts in JSON format.

## Features

- Custom REST API built using `@RestResource`
- Supports HTTP GET method
- Fetches a single Account and all related Contacts
- Uses wrapper classes to structure the JSON response
- Tested using Salesforce Workbench
- Achieves 100% code coverage with Apex Test Class

## Files Included

| File                          | Description                                |
|------------------------------|--------------------------------------------|
| `CustomRESTAPIClass.cls`     | Main Apex class with REST API logic        |
| `CustomRESTAPIClass.cls-meta.xml` | Metadata file for deployment         |
| `CustomRESTAPIClassTest.cls` | Apex test class to simulate REST request   |
| `README.md`                  | Project overview and documentation         |

## How It Works

The REST API is exposed at the following endpoint:


In this example:
- `001d200000XuVFtAAN` is a real Account record ID from the Salesforce Developer Org used in testing.
- When the endpoint is called using GET method, the response returns the Account's ID and Name, along with all its related Contacts in JSON format.

### Example JSON Response

```json
{
  "accountId": "001d200000XuVFtAAN",
  "accountName": "Dickenson plc",
  "contacts": [
    {
      "contactId": "003d200000YtYbCAAX",
      "firstName": "John",
      "lastName": "Doe"
    },
    {
      "contactId": "003d200000YtYbDAAX",
      "firstName": "Andy",
      "lastName": "Young"
    }
  ]
}
