# Get Flights

## Endpoint
GET/flights

## Description
Fetch available flights between two cities.

## Query Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| from      |stringe|    Yes      | Departure city code |
| to        |stringe|    Yes      | Destination City code|

## Example Request
GET / flights?from=DEL&to=BLR

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

## Error response
### 400 Bad Request
```json
{
"status": "error",
"message": "invalid query parameter"
}
```
