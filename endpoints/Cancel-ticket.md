# Cancel Ticket

## Endpoint
DELET /cancel/{bookingId}

---

## Description
Cancel an existing flight booking using the booking ID.

---

## Headers
| Header | Type | Required | Description |
|--------|------|----------|-------------|
| Authorization | string | Yes | bearer token |

---

## Path Parameters
| Parameter | Type | Required | Description |
|----------|---------|--------|-------------|
|booking Id | string | yes | Unique booking identifier |

---

## Exxample Request 
DELET /cancel/BK12345
Authorization: Bearer YOUR_API_TOKEN

---

## example Response 
```json
{
"status": "success",
"message": "Booking canceled successfully"
}
```
---

## Error Responses
400 bad request
```json
{
"status": "error",
"message": "Invalid booking ID"
}
```
---

## 401 Unauthorized
```json
{
"status": "error",
"message": "Missing or invalid token"
}
```
---

## 404 Not found
```json
{
"status": "error",
"message": "Booking not found"
}
```
---

## 500 Internal Server Error
```json
{
"status": "error",
"message": "Servver error"
}
```
---

## Notes
- ensure the booking ID exists before attempting cancellation.
- Cancellation may be subject to airline polices


