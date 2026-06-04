# API Mastery Plan

This plan is built around two outcomes:

1. Build strong hands-on REST API development skill.
2. Crack API-related backend interviews with clear explanations and practical examples.

The target is not only to know Laravel API features. The target is to understand API design deeply enough to build, debug, secure, test, document, and explain real APIs.

---

## Core Strategy

Every topic must be practiced in four ways:

1. Concept: understand the idea.
2. Implementation: build it in Laravel.
3. Verification: test it through Postman, Insomnia, or automated tests.
4. Interview explanation: write and speak the answer clearly.

If a topic cannot be explained simply, it is not mastered yet.

---

## Daily Work Template

For each day, create or update:

```txt
exercises/DayXX/README.md
docs/learning/REST_API_INTERVIEW_RECAP.md
```

Use this format in each day folder:

```md
# Day XX - Topic Name

## Goal

## Concepts Learned

## Laravel Implementation

## Endpoints Built

## Request Examples

## Response Examples

## Problems Faced

## Tests

## Interview Questions

## Summary
```

---

## Phase 1: REST API Foundations

Goal: think in API contracts instead of Blade pages or MVC screens.

Topics to master:

- What an API is
- REST principles
- HTTP methods
- HTTP status codes
- JSON request and response structure
- route parameters, query parameters, and request body
- resource naming
- CRUD endpoint design
- idempotency

Hands-on targets:

- Build a health check endpoint.
- Build customer CRUD endpoints.
- Use correct status codes for create, update, delete, validation, and not found responses.
- Add pagination, filtering, sorting, and searching.

Interview targets:

- Explain REST.
- Explain `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`.
- Explain `200`, `201`, `204`, `400`, `401`, `403`, `404`, `422`, `429`, and `500`.
- Explain `PUT` vs `PATCH`.
- Explain API route naming best practices.

---

## Phase 2: Laravel API Structure

Goal: write clean Laravel APIs with thin controllers and predictable responses.

Topics to master:

- API routes
- controller structure
- Form Requests
- API Resources
- Resource Collections
- service classes
- action classes
- response consistency

Hands-on targets:

- Use `app/Http/Controllers/Api/V1`.
- Use Form Requests for all create and update endpoints.
- Use API Resources for all successful responses.
- Create a reusable response pattern.
- Keep controllers small.

Interview targets:

- Why should we use Form Requests?
- Why should we use API Resources?
- Why should controllers stay thin?
- Why is returning raw models risky?

---

## Phase 3: Authentication and Authorization

Goal: secure APIs correctly.

Topics to master:

- bearer tokens
- Laravel Sanctum
- Passport and OAuth2 concepts
- JWT concepts
- access tokens
- refresh tokens
- token rotation
- authentication vs authorization
- policies and gates
- roles and permissions

Hands-on targets:

- Register user.
- Login user.
- Logout user.
- Return authenticated profile.
- Protect private routes.
- Add admin, manager, and staff roles.
- Add policies for customer/order access.

Interview targets:

- Authentication vs authorization.
- Session auth vs token auth.
- Sanctum vs Passport.
- JWT advantages and risks.
- Access token vs refresh token.
- How to secure login APIs.

---

## Phase 4: Professional API Features

Goal: handle real-world API requirements.

Topics to master:

- versioning
- rate limiting
- caching
- N+1 query prevention
- file uploads
- queues
- events
- webhooks
- external API consumption
- logging
- monitoring

Hands-on targets:

- Add `/api/v1` route structure.
- Add rate limiting to login and public APIs.
- Cache read-heavy endpoints.
- Optimize order listing with eager loading.
- Build secure file upload.
- Queue notification after order creation.
- Build webhook receiver.
- Consume one external API.

Interview targets:

- Why version APIs?
- What is rate limiting?
- How do you optimize slow APIs?
- What is the N+1 problem?
- What is a webhook?
- How do you handle failed external API calls?

---

## Phase 5: Testing, Documentation, and Production Readiness

Goal: make APIs maintainable and interview-ready.

Topics to master:

- feature tests
- validation tests
- authorization tests
- JSON assertions
- API documentation
- OpenAPI/Swagger/Scribe/Postman
- error formatting
- deployment checklist

Hands-on targets:

- Write tests for auth.
- Write tests for CRUD.
- Write tests for validation.
- Write tests for authorization.
- Document every important endpoint.
- Create production readiness notes.

Interview targets:

- How do you test APIs?
- What should API documentation include?
- How should APIs handle errors?
- How do you prepare APIs for production?

---

## Weekly Checkpoints

### End of Week 1

You can design and build basic REST CRUD APIs with validation, resources, pagination, filtering, and correct status codes.

### End of Week 2

You can build authenticated and authorized APIs using Laravel Sanctum, roles, permissions, policies, and token concepts.

### End of Week 3

You can add real-world API features such as versioning, rate limiting, caching, performance optimization, file upload, queues, and webhooks.

### End of Week 4

You can test, document, explain, and present the API project as interview-ready work.

---

## Interview Practice Rule

For every implemented feature, prepare answers for:

1. What problem does it solve?
2. How did you implement it in Laravel?
3. What mistakes should developers avoid?
4. How would you explain it in an interview?

This turns coding practice into interview confidence.
