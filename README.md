ecommerce API Documentation
 
This API documentation provides details on the endpoints and operations of the ecommerce Service. Below are the available API endpoints with their corresponding methods, parameters, and responses.
      
## Inventory APIS
 
### insert inventory details
 
### /inventory - insert inventory details
 
- **Method:** POST
- **Summary:** insert inventory
- **Operation ID:** insert inventory
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
 
```bash
const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "product_id": 28,
  "availableQuantity": 24
});

const requestOptions = {
  method: "POST",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:4002/dev/inventory", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
 
## Get all inventory details
 
### /Node - Get all inventories
 
- **Method:** GET
- **Summary:** Get all inventories
- **Operation ID:** Get all inventories
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation
 
  ### Example:
```bash
const raw = "";

const requestOptions = {
  method: "GET",
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:4002/dev/inventory", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
 
 
## Get inventory By ID
 
### /inventory/{inventory_id} - Get inventory By ID
 
- **Method:** GET
- **Summary:** Get inventory By ID
- **Operation ID:** getInventoryByID
- **Tags:** Request
- **Responses:**
  - **200:** Successful operation

 
  ### Example:
```bash
const requestOptions = {
  method: "GET",
  redirect: "follow"
};

fetch("http://localhost:4002/dev/inventory/95792b6b-5a86-4caf-8900-92d46ce1062b", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
 
## Update inventory details
 
### /inventory/{inventory_id} - Update inventory details
 
- **Method:** PUT
- **Summary:** Update inventory details
- **Operation ID:** updateInventoryDetails
- **Tags:** Request
- **Responses:**
  - **200:** Update successful

 
  ### Example:
```bash
const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "updatedQuantity": 54
});

const requestOptions = {
  method: "PUT",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:4002/dev/inventory/95792b6b-5a86-4caf-8900-92d46ce1062b", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
   ```
 
 
## Delete inventory
 
### /inventory/{inventory_id} - Delete Node
 
- **Method:** DELETE
- **Summary:** Delete inventory
- **Operation ID:** deleteinventory
- **Tags:** Request
- **Responses:**
  - **200:** Deletion successful
 
 
   ### Example:
```bash
  const myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

const raw = JSON.stringify({
  "updatedQuantity": 54
});

const requestOptions = {
  method: "DELETE",
  headers: myHeaders,
  body: raw,
  redirect: "follow"
};

fetch("http://localhost:4002/dev/inventory/95792b6b-5a86-4caf-8900-92d46ce1062b", requestOptions)
  .then((response) => response.text())
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
  ```
