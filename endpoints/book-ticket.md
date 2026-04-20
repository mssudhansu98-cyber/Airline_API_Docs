# Book Ticket

## Endpoint
POST /book

## Description
Book a flight ticket for a passenger.

## Headers
| Header | Type | Required | Description |
|---------|-----|----------|-------------|
| Authorization | string | Yes | Bearer token |
| Content-Type | string | Yes | application/json |

## Request body 
```json
{
 "flightId": "AI101",
 "passengerName": "Sudhansu Sekhar",
"age": 28,
"seatClass": "Economy"
}
```

## Request Body Parameters
| Field | Type | Required | Decsription |
|-------|------|----------|-------------|
| FlightId | string | Yes | Flight ID to be booked |
| passengerName | string | Yes | Name of the passenger |
| age | number | Yes | Passenger age |
| seatClass | sringe | No | Economy / buisness |

## Example Request
POST /book
Authorization: Bearer YOUR_API_TOKEN
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
"bookingId": "BK12345"
}
```
## Error Responses

### 400 Bad Request
```json
{
"status": "error",
"message": "Invalid input data"
}
```
### 401 Unauthorized
```json
{
"status": "error",
"message": "Missing or Invalid token"
}
```

### 500 Internal Server Error
```json
{
"status": "error",
"message": "Server error"
}
```

## Notes
- Ensure valid flightID before booking
- Seat availablity is subject to change 


