Ecommerce API Documentation

This APIS documentation provides details on the endpoints and operations of the Ecommerce Service. Below are the available API endpoints with their corresponding methods, parameters, and responses.

## Order APIS

### Create Order

###  /Order  Create Order

- **Method:** POST
- **Summary:** Create Order
- **Operation ID:** createOrder
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation

```bash
const myHeaders = new Headers();
myHeaders.append("", "");
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "products": [
    {
      "name": "Product 1",
      "price": 10.99
    },
    {
      "name": "Product 2",
      "price": 20.49
    }
  ],
  "totalPrice": "31.48",
  "createdAt": "2024-02-07T10:00:00Z"
});

const requestOptions = {
  method: "POST",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:3000/dev/order", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));

```
### Create CancelOrder

###  /Order/{Id}    Create CancelOrder

- **Method:** POST
- **Summary:** Create CancelOrder
- **Operation ID:** create CancelOrder
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation

```bash
const myHeaders = new Headers();
myHeaders.append("", "");

const raw = "";

const requestOptions = {
  method: "POST",
  headers: myHeaders,
  body: JSON.stringify({
    "Status": "Cancell Order")
  }
  redirect: "follow"
};

fetch("baseUrl/dev/order/{Id}", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));

```
### Create CloseOrder

###  /Order/{Id}    Create CloseOrder

- **Method:** POST
- **Summary:** Create CloseOrder
- **Operation ID:** create CloseOrder
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation

```bash
const myHeaders = new Headers();
myHeaders.append("", "");

const raw = "";

const requestOptions = {
  method: "POST",
  headers: myHeaders,
  body: JSON.stringify({
    "Status": "Close Order")
  }
  redirect: "follow"
};

fetch("baseUrl/dev/order/{Id}", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));

```
## Get Order

### /Order - Get Order

- **Method:** GET
- **Summary:** Get Order
- **Operation ID:** getOrder
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation

  ### Example:

``` bash

const myHeaders = new Headers();
myHeaders.append("", "");

const raw = "";

const requestOptions = {
  method: "GET",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("baseUrl/dev/order", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));

  ```

## Get Order By ID

### /Order{Id} - Get Order By ID

- **Method:** GET
- **Summary:** Get Order By ID
- **Operation ID:** getOrderByID
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
  - **400:** Order ID is missing or invalid
  - **404:** Order not found

  ### Example:
```bash
const myHeaders = new Headers();
myHeaders.append("", "");

const raw = "";

const requestOptions = {
  method: "GET",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("baseUrl/dev/order/{id}", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));

  ```

  ## Update Order 

### /Order{Id} - Update Order

- **Method:** PUT
- **Summary:** Update Order 
- **Operation ID:** updateOrder
- **Tags:** Request
- **Responses:**
  - **200:** Update successful
  - **400:** Invalid OrderId or request body
  - **500:** Internal Server Error

  ### Example:
```bash
const myHeaders = new Headers();
myHeaders.append("", "");
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "products": [
    {
      "name": "Product 1",
      "price": 10.99
    },
    {
      "name": "Product 2",
      "price": 20.49
    }
  ],
  "totalPrice": "31.48",
  "createdAt": "2024-02-07T10:00:00Z"
});

const requestOptions = {
  method: "PUT",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:3000/dev/order/12", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```

## Delete Order

### /Order/{Id} - Delete Order

- **Method:** Delete
- **Summary:** Delete Order
- **Operation ID:** deleteOrder
- **Tags:** Request
- **Responses:**
  - **200:** Deletion successful
  - **400:** Invalid Order Id
  - **500:** Internal Server Error

   ### Example:
```bash
const myHeaders = new Headers();
myHeaders.append("", "");

const raw = "";

const requestOptions = {
  method: "DELETE",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("baseUrl/dev/order/{id}", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));

  ```