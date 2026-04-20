# Get Flights

## Endpoint
 GET /flights
---
## Description
 Fetch available flights between two cities.
---

## Headers
| Header | Type | Required | Description |
|--------|------|----------|------------ |
| Authorization | string | Yes | Bearer token |
---

## Query Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| from      |string|    Yes      | Departure city code |
| to        |string|    Yes      | Destination city code|
---
## Example Request
GET /flights?from=DEL&to=BLR
---

## Example Response
```json
{
  "status": "success",
  "data": [
    {
      "flightId": "AI101",
      "departure": "DEL",
      "arrival": "BLR",
      "price": 5000
    }
  ]
}
```
---

## Error response
### 400 Bad Request
```json
{
"status": "error",
"message": "Invalid query parameter"
}
```
---
### 401 Unauthorized
```json
{
 "status": "error",
"message": "Missing or invalid tokenn"
}
```
---
### 404 Not found
```json
{
 "status": "error",
 "message": "Flight not found"
 }
```
---


 
