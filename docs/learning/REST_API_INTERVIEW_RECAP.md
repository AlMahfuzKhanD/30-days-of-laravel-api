# REST API Interview Recap

This document is for quick review before API-related interviews. Keep improving it during the 30-day practice.

---

## What Is an API?

An API, or Application Programming Interface, is a contract that allows one software system to communicate with another.

In web development, an API usually receives HTTP requests and returns structured responses, commonly JSON.

Example:

```txt
GET /api/v1/customers/10
```

The client asks for customer `10`, and the server returns customer data.

---

## What Is REST?

REST means Representational State Transfer. It is an architectural style for designing network APIs around resources.

In REST, resources are represented by URLs, and actions are represented by HTTP methods.

Example:

```txt
GET    /api/v1/customers
POST   /api/v1/customers
GET    /api/v1/customers/10
PUT    /api/v1/customers/10
PATCH  /api/v1/customers/10
DELETE /api/v1/customers/10
```

---

## Common HTTP Methods

| Method | Purpose | Example |
| --- | --- | --- |
| GET | Read data | `GET /customers` |
| POST | Create data | `POST /customers` |
| PUT | Replace a resource | `PUT /customers/10` |
| PATCH | Partially update a resource | `PATCH /customers/10` |
| DELETE | Delete a resource | `DELETE /customers/10` |

---

## Important Status Codes

| Code | Meaning | Usage |
| --- | --- | --- |
| 200 | OK | Successful read or update |
| 201 | Created | Resource created successfully |
| 204 | No Content | Delete successful with no response body |
| 400 | Bad Request | Invalid request format |
| 401 | Unauthorized | User is not authenticated |
| 403 | Forbidden | User is authenticated but not allowed |
| 404 | Not Found | Resource does not exist |
| 422 | Unprocessable Entity | Validation failed |
| 429 | Too Many Requests | Rate limit exceeded |
| 500 | Server Error | Unexpected server failure |

---

## PUT vs PATCH

`PUT` usually replaces the full resource.

`PATCH` updates only selected fields.

Example:

```txt
PUT /api/v1/customers/10
```

Expected to send the full customer payload.

```txt
PATCH /api/v1/customers/10
```

Can send only one field, such as customer status.

---

## Authentication vs Authorization

Authentication answers:

```txt
Who are you?
```

Authorization answers:

```txt
What are you allowed to do?
```

Example:

- Login with token: authentication
- Only admin can delete user: authorization

---

## 401 vs 403

Use `401 Unauthorized` when the user is not logged in or the token is missing/invalid.

Use `403 Forbidden` when the user is logged in but does not have permission.

---

## Good API Response Shape

Success response:

```json
{
  "data": {
    "id": 1,
    "name": "Customer Name"
  },
  "message": "Customer retrieved successfully"
}
```

Validation error:

```json
{
  "message": "Validation failed",
  "errors": {
    "email": [
      "The email field is required."
    ]
  }
}
```

---

## Laravel API Best Practices

- Use `routes/api.php` for API routes.
- Use route prefixes like `/api/v1`.
- Use Form Requests for validation.
- Use API Resources for response transformation.
- Use policies for authorization.
- Use feature tests for important endpoints.
- Avoid returning raw Eloquent models directly.
- Avoid business logic-heavy controllers.
- Use pagination for list endpoints.
- Use eager loading to prevent N+1 queries.

---

## Common Interview Questions

### What is REST?

REST is an architectural style where APIs expose resources through URLs and use HTTP methods to perform actions on those resources.

### What is the difference between API and REST API?

An API is any interface that allows systems to communicate. A REST API is a specific type of API that follows REST principles using resources, HTTP methods, stateless communication, and standard status codes.

### Why use API Resources in Laravel?

API Resources control how models are converted to JSON. They help avoid exposing unnecessary database fields and keep response formats consistent.

### Why use Form Requests?

Form Requests move validation logic out of controllers. They make controllers cleaner and validation reusable.

### What is stateless API design?

Stateless means each request contains all information needed to process it. The server does not depend on session state from previous requests.

### What is rate limiting?

Rate limiting controls how many requests a client can make in a period of time. It protects APIs from abuse, brute-force attacks, and accidental overload.

### What is the N+1 query problem?

The N+1 problem happens when an API loads a list of records and then runs an extra query for each record's relationship. In Laravel, eager loading with `with()` helps prevent it.

---

## Quick Revision Checklist

Before an interview, review:

- REST principles
- HTTP methods
- status codes
- request vs response
- validation errors
- authentication vs authorization
- Sanctum basics
- JWT and OAuth2 basics
- API Resources
- Form Requests
- policies and gates
- pagination and filtering
- rate limiting
- caching
- API testing
- API documentation
- security best practices
