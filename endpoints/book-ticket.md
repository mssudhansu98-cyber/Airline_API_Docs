# Book Ticket

## End point
POST /book

## Description
Book a flight ticket for a passanger.

## Headers
| Header | Type | Required | Description |
|---------|-----|----------|-------------|
| Authorization | string | Yes | Bearer token |
| Content- type | string | Yes | application/json |

## Request body 
```json
{
 "FlightId": "AI101",
 "passengerName": "Sudhansu Sekhar",
"age": 28,
"seatclass": "Economy"
}
```

## Request Body Parameters
| Field | Type | Required | Decsription |
|-------|------|----------|-------------|
| FlightId | string | Yes | Flight ID to be booked |
| passengername | string | Yes | Name of the passenger |
| age | number | Yes | Passenger age |
| seatClass | sringe | No | Economy / buisness |

## Example Request
POST /book
Authorization: Bearer Token
Content-type: application/json

```json
{
"flightId": "AI101",
"passengerName": "Sudhansu Sekhar",
"age": 28,
"seatclass": "Economy"
}
```
## Example Response
```json
{
"status": "success",
"message": "Ticket booked successfully",
"bookingid": "BK12345"
}
```
## Error Responses

### 404 Bad Request
```json
{
"status": "error",
"message": "Invalid input data"
}
```
### 401 Unauthorized
```json
{
"status": "error"
"message": "Missing or Invalid token"
}
```

### 500 Internal Server Error
```json
{
"ststus": "error",
"messege": "Server error"
}
```

## Notes
- Ensure valid flightID before booking
- Seat availablity is subject to change 


