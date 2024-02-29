This API documentation provides details on the endpoints and operations of the ecommerce Service. Below are the available API endpoints with their corresponding methods, parameters, and responses.

## customer APIS

### insert customer

### /customer - insert customer

- **Method:** POST
- **Summary:** insert customer
- **Operation ID:** insert customer
- **Tags:** Request
- **Responses:**

  - **200:** Successful operation

  ### Example:

```bash
const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "customer_details": {
    "name": "mddsa",
    "email": "ssdd",
    "phno": "2",
    "address": "ddsfdsddsdffadddm",
    "city": "hydewfdsdd",
    "country": "india"
  }
});

const requestOptions = {
  method: "POST",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:3000/customer", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```

### /customer - get all customer

- **Method:** POST
- **Summary:** get all customer
- **Operation ID:** get all customer
- **Tags:** Request
- **Responses:**

  - **200:** Successful operation

  ### Example:

```bash
const requestOptions = {
  method: "GET",
  redirect: "follow"
};

fetch("http://localhost:3000/customer", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```

### customer get by id

### /customer - customer get by id

- **Method:** GET
- **Summary:** customer get by id
- **Operation ID:** customer get by id
- **Tags:** Request
- **Responses:**

  - **200:** Successful operation

  ### Example:

```bash
const requestOptions = {
  method: "GET",
  redirect: "follow"
};

fetch("http://localhost:3000/customer/9af5cc9e-38d7-4075-b0dc-840e5bcbfc1d", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```

### update customer

### /customer - update Product

- **Method:** PUT
- **Summary:** update customer
- **Operation ID:** update customer
- **Tags:** Request
- **Responses:**

  - **200:** Successful operation

  ### Example:

```bash
const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "customer_details": {
    "name": "ahbvasdk",
    "email": "examplsdfsde.com",
    "phone": "732535"
  }
});

const requestOptions = {
  method: "PUT",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:3000/customer/9af5cc9e-38d7-4075-b0dc-840e5bcbfc1d", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```

### delete customer

### /customer - delete customer

- **Method:** DELETE
- **Summary:** delete customer
- **Operation ID:** delete customer
- **Tags:** Request
- **Responses:**

  - **200:** Successful operation

  ### Example:

```bash
const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

const requestOptions = {
  method: "DELETE",
  headers: myHeaders,
  redirect: "follow"
};

fetch("http://localhost:3000/customer/a35acb7c-92af-452e-add8-6619511b3fe9", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```
