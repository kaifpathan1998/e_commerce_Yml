This API documentation provides details on the endpoints and operations of the ecommerce Service. Below are the available API endpoints with their corresponding methods, parameters, and responses.
 
## Product APIS
 
### insert Product
 
### /Product - insert Product
 
- **Method:** POST
- **Summary:** insert Product
- **Operation ID:** insert Product
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
```bash
  const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");
 
const raw = JSON.stringify({
  "name": {
    "S": "washine machine"
  },
  "description": {
    "S": "Updated Product Description"
  },
  "price": {
    "N": 50
  },
  "quantity": {
    "N": 50
  },
  "unit": {
    "M": {
      "kg": {
        "N": 50
      }
    }
  },
  "category": {
    "S": "electronics"
  },
  "image": {
    "S": "C:\\Users\\Hi\\Pictures\\Screenshots\\Screenshot 2024-01-16 161402.png"
  }
});
 
const requestOptions = {
  method: "POST",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};
 
fetch("http://localhost:3000/dev/product", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
 
 
### get Product
 
### /Product - get Product
 
- **Method:** GET
- **Summary:** get Product
- **Operation ID:** get Product
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
```bash
  const requestOptions = {
  method: "GET",
  headers: myHeaders,
  redirect: "follow"
};
 
fetch("http://localhost:3000/dev/product", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
 
  ### product get by id
 
  ### /Product - Product get by id
 
- **Method:** GET
- **Summary:** Product get by id
- **Operation ID:** Product get by id
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
```bash
  const requestOptions = {
  method: "GET",
  redirect: "follow"
};
 
fetch("http://localhost:3000/dev/product/04ee1f11-09e8-488e-91c9-f64aede3eee1", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
 ```
### update Product
 
### /Product - update Product
 
- **Method:** PUT
- **Summary:** update Product
- **Operation ID:** update Product
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
```bash
  const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");
 
const raw = JSON.stringify({
  "name": {
    "S": "apple"
  },
  "description": {
    "S": "Updated Product Description"
  },
  "price": {
    "N": 300
  },
  "quantity": {
    "N": 100
  },
  "unit": {
    "M": {
      "kg": {
        "N": 100
      }
    }
  },
  "category": {
    "S": "fruits"
  },
  "image": {
    "S": "https://example.com/image.jpg"
  }
});
 
const requestOptions = {
  method: "PUT",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};
 
fetch("http://localhost:3000/dev/product/04ee1f11-09e8-488e-91c9-f64aede3eee1", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
 
 ### delete Product
 
### /Product - delete Product
 
- **Method:** DELETE
- **Summary:** delete Product
- **Operation ID:** delete Product
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
```bash
  const requestOptions = {
  method: "DELETE",
  redirect: "follow"
};
 
fetch("http://localhost:3000/dev/product/04ee1f11-09e8-488e-91c9-f64aede3eee1", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
has context menu