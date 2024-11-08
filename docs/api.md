# API Documentation

## Endpoints

### Health Check

```http
GET /health
```

Returns the health status of the service.

**Response**
```json
{
  "status": "healthy",
  "version": "0.1.0"
}
```

### Echo Service

```http
POST /echo
```

Returns the provided message.

**Request Body**
```json
{
  "content": "Hello, World!"
}
```

**Response**
```json
{
  "content": "Hello, World!"
}
```

## Error Responses

All endpoints may return the following error responses:

- `400 Bad Request` - Invalid request format
- `500 Internal Server Error` - Server-side error

## Content Types

- All requests must use `Content-Type: application/json`
- All responses will be in JSON format

## Rate Limiting

Currently, no rate limiting is implemented.

## Authentication

Currently, no authentication is required.