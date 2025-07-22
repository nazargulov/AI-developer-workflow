# API Context for AI

## API Architecture Overview

- **Type:** RESTful API with JSON responses
- **Authentication:** JWT tokens, API keys for external integrations
- **Rate Limiting:** Per-user and per-endpoint limits
- **Versioning:** URL-based versioning (/api/v1/, /api/v2/)

## Core Endpoints

- **Authentication:** `/auth/login`, `/auth/refresh`, `/auth/logout`
- **Users:** `/users`, `/users/{id}`, `/users/{id}/profile`
- **Health:** `/health`, `/metrics`, `/status`

## Request/Response Patterns

```javascript
// Standard API response format
{
  "success": true,
  "data": { /* response data */ },
  "message": "Operation completed successfully",
  "timestamp": "2025-07-19T10:30:00Z",
  "requestId": "req_123456"
}

// Error response format
{
  "success": false,
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input data",
    "details": { /* field-specific errors */ }
  },
  "timestamp": "2025-07-19T10:30:00Z",
  "requestId": "req_123456"
}
```

## Security Considerations

- **Input Validation:** Strict validation for all inputs
- **Output Sanitization:** XSS prevention, data leakage protection
- **CORS Configuration:** Secure cross-origin resource sharing
- **SSL/TLS:** Enforce HTTPS for all communications

## Performance Guidelines

- **Caching:** Redis for session data, response caching
- **Pagination:** Limit large result sets, cursor-based pagination
- **Async Processing:** Background jobs for heavy operations

## Common AI Applications

- API usage pattern analysis
- Automated API testing
- Performance optimization suggestions
- Security vulnerability detection
- Documentation generation
- Error handling improvements

## Integration Examples

- Third-party payment processors
- External authentication providers
- Monitoring and logging services
- Analytics and reporting tools
