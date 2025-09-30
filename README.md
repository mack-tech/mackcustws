# Mack Customers API Services
<p align="center">
    <img src="https://www.macktech.com/wp-content/uploads/2019/05/macktech-logo-blue-web.png" alt="Mack Technologies">
</p>

### Documentation Holley API Service

### Endpoint Overview

This endpoint retrieves information about a specific box identified by its unique `boxId`.

### Request

- **Method**: GET
    
- **URL**: `https://jrzcusws.macktech.com:10443/api/Holley/boxes/{boxId}`
    
- **Path Parameter**:
    
    - `boxId` (integer): The unique identifier for the box whose details are being requested.
        

### Response

- **Status Code**: 200 OK
    
- **Content-Type**: application/json
    
- **Response Body**:
    
    - `boxId` (integer): The ID of the box.
        
    - `units` (array): An array of unit objects associated with the box, where each unit contains:
        
        - `serialNumber` (string): The serial number of the unit.
            
        - `jobOrder` (string): The job order associated with the unit.
            
        - `createdAt` (string): The timestamp of when the unit was created.
            

This endpoint is useful for obtaining detailed information about a box and its associated units based on the provided `boxId`.

### Purpose

This endpoint retrieves detailed information about a specific box identified by its unique `boxId`. It is useful for obtaining the metadata and associated units of a box in the system.

### Request Format

- **Method**: GET
    
- **URL**: `https://jrzcusws.macktech.com:10443/api/Holley/boxes/{boxId}`
    
- **Path Parameter**:
    
    - `boxId` (integer): The unique identifier for the box you want to retrieve information about.
        

### Response Structure

On a successful request (HTTP Status 200), the response will be in JSON format and will contain the following structure:

``` json
{
  "boxId": 0,
  "units": [
    {
      "serialNumber": "",
      "jobOrder": "",
      "createdAt": ""
    }
  ]
}

 ```

- **Response Fields**:
    
    - `boxId` (integer): The ID of the box.
        
    - `units` (array): A list of units associated with the box. Each unit contains:
        
        - `serialNumber` (string): The serial number of the unit.
            
        - `jobOrder` (string): The job order associated with the unit.
            
        - `createdAt` (string): The timestamp indicating when the unit was created.
            

### Authentication

Ensure that you are authenticated to access this endpoint. Include the necessary authentication tokens or credentials in your request headers as required by your API security policy.

### Error Handling

In case of an error, the API may return different HTTP status codes along with a message detailing the issue. Common status codes include:

- **404 Not Found**: If the specified `boxId` does not exist.
    
- **401 Unauthorized**: If authentication fails.
    
- **500 Internal Server Error**: For unexpected server issues.
    

Make sure to handle these responses appropriately in your application.

### Support
Feel free to reach out to us at https://www.macktech.com/juarez-mexico/

