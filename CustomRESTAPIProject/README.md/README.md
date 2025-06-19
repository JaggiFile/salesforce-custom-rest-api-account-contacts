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


Replace `{AccountId}` with a valid 15- or 18-character Account record ID.

### Example JSON Response

```json
{
  "accountId": "001XXXXXXXXXXXX",
  "accountName": "Test Account",
  "contacts": [
    {
      "contactId": "003XXXXXXXXXXXX",
      "firstName": "John",
      "lastName": "Doe"
    },
    {
      "contactId": "003XXXXXXXXXXXY",
      "firstName": "Jane",
      "lastName": "Smith"
    }
  ]
}
