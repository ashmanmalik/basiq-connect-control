Basiq Connect is a javascript library written in React, which allows applicants to securely connect to their bank so lenders can generate an Affordability Report.

##Requirements

Basiq Connect requires installing of react and react-dom, starting from version 16.9.0:

$ npm install react
$ npm install react-dom

## Installation

$ npm install basiq-connect

##Configuration

Basiq Connect is a function which receives configuration as an input object with following parameters:

1. containerId
  - ID of the DOM element in which Basiq Connect will be rendered
  Type: String
2. token 
  - authentication token
  Type: String
3. userID
  - ID of the user
  Type: String
4. connectLinkID
  - ID part of Basiq Connect link
  Type: String
5. upload
  - True if uploading statements should be enabled
  Type: Boolean 
6. connect
  - True if connecting to bank with credentials should be enabled
  Type: Boolean 
7. companyName
  - Name of the company(bank)
  Type: String

## How to use it

Basiq Connect requires authentication. Authentication can be done through providing connect link or access token and user id.

- Calling Basiq Connect with provided token and userID
  Add the following code to your .js file:

```
import BasiqConnect from 'basiq-connect';

BasiqConnect({
    containerId: DOM_CONTAINER_ID,
    token: YOU_TOKEN,
    userID: YOUR_USER_ID,
    upload: TRUE/FALSE,
    connect: TRUE\FALSE,
    companyName: YOUR_COMPANY_NAME
});
```

- Calling Basiq Connect with provided connect link:
Add the following code to your .js file:

```
import BasiqConnect from 'basiq-connect';

BasiqConnect({
    containerId: DOM_CONTAINER_ID,
    connectLink: YOUR_CONNECT_LINK,
    upload: TRUE/FALSE,
    connect: TRUE\FALSE,
    companyName: YOUR_COMPANY_NAME
});

```

* If connect link is https://connect.basiq.io/0272b5c7-b19a-4d93-908d-18c44ferffwd7a ID part of connect link is 0272b5c7-b19a-4d93-908d-18c44ferffwd7a



