# User Management Context for AI

## User Domain Overview
- **Purpose:** Manage user accounts, authentication, and authorization
- **Scope:** Registration, login, profile management, permissions, preferences
- **Security Focus:** Authentication, session management, data protection

## User Lifecycle
- **Registration:** Account creation, email verification, initial setup
- **Authentication:** Login/logout, password management, 2FA support
- **Profile Management:** Personal information, preferences, settings
- **Account States:** Active, suspended, pending verification, deleted

## Key Models and Services
- **User Model:** Core user data, authentication credentials
- **Profile Service:** User preferences, personal information management
- **Authentication Service:** Login/logout, session management
- **Authorization Service:** Role-based access control, permissions

## Business Rules
- **Password Policy:** Minimum requirements, expiration, history
- **Session Management:** Timeout rules, concurrent sessions, security
- **Data Privacy:** GDPR compliance, data retention, user consent
- **Account Security:** Failed login attempts, account lockout, recovery

## Common Patterns
```javascript
// User authentication workflow
async function authenticateUser(credentials) {
  // 1. Validate credentials format
  // 2. Check against stored data
  // 3. Verify account status
  // 4. Create session
  // 5. Log security event
}
```

## AI Applications
- User behavior analysis
- Anomaly detection in login patterns
- Automated user support
- Personalization recommendations
- Security threat detection
- Profile completion suggestions
