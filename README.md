# 30 Days of Laravel API

A practical Laravel API learning project designed to build two skills at the same time:

1. Become confident building production-style REST APIs.
2. Prepare for API-focused backend interviews.

I have experience working with Laravel MVC, but this repository is focused on strengthening API design, API architecture, authentication, authorization, testing, documentation, security, and performance.

The goal is not only to complete 30 days of practice. The goal is to build enough hands-on experience and interview knowledge to explain, design, and implement real-world REST APIs with confidence.

---

## Main Outcomes

By the end of this project, I should be able to:

- Design clean RESTful APIs using correct routes, methods, status codes, and response formats.
- Build Laravel APIs using Form Requests, API Resources, controllers, services, policies, and tests.
- Implement authentication with Laravel Sanctum and understand Passport, OAuth2, JWT, access tokens, and refresh tokens.
- Add authorization with roles, permissions, policies, and gates.
- Handle validation, exceptions, and error responses professionally.
- Implement pagination, filtering, sorting, searching, caching, rate limiting, file uploads, queues, webhooks, and external API integrations.
- Write automated API tests and document endpoints clearly.
- Explain API concepts clearly in interviews with examples from this project.

---

## Repository Structure

```txt
30-days-of-laravel-api/
|
|-- src/                     # Laravel application workspace
|   |-- app/
|   |-- routes/api.php
|   |-- config/
|   |-- tests/
|   `-- ...
|
|-- exercises/               # Day-wise practice, tasks, notes, and logs
|   |-- Day01/
|   |-- Day02/
|   |-- ...
|   `-- Day30/
|
|-- docs/                    # Learning plan and API knowledge base
|   |-- API_MASTERY_PLAN.md
|   `-- learning/
|       |-- README.md
|       `-- REST_API_INTERVIEW_RECAP.md
|
|-- README.md
`-- LICENSE
```

---

## Learning Method

Each day has two tracks:

```txt
Track A: Build API skill through Laravel implementation.
Track B: Build interview skill through written Q&A and explanation.
```

Daily workflow:

1. Learn the topic.
2. Implement it inside the Laravel app.
3. Test it with Postman, Insomnia, or automated tests.
4. Document the endpoint behavior and mistakes.
5. Add interview questions and answers.
6. Commit the progress.

---

## Documentation

Start here:

- [API mastery plan](docs/API_MASTERY_PLAN.md)
- [Learning docs index](docs/learning/README.md)
- [REST API interview recap](docs/learning/REST_API_INTERVIEW_RECAP.md)

The `docs/learning/` folder is the long-term revision area. Before interviews, I should be able to review those files and quickly recap the most important API concepts.

---

## 30-Day Roadmap

### Week 1: REST API Foundations

1. API basics, REST, JSON, HTTP
2. Laravel API project setup
3. API routing, controllers, and request lifecycle
4. CRUD API design
5. Form Requests and validation
6. API Resources and response transformation
7. Pagination, sorting, filtering, and searching

### Week 2: Authentication and Authorization

8. Token basics and hashing
9. Laravel Sanctum
10. Passport and OAuth2 concepts
11. Role-based access control
12. Policies and gates
13. JWT authentication concepts
14. Refresh tokens and token rotation

### Week 3: Advanced API Features

15. API versioning
16. Rate limiting and throttling
17. Caching and performance optimization
18. Eloquent optimization and N+1 query prevention
19. File upload API and secure storage
20. Events, listeners, and queues
21. Domain-driven API structure

### Week 4: Professional API Development

22. Automated API testing
23. API documentation with OpenAPI, Swagger, Scribe, or Postman
24. Custom error handling and exception formatting
25. Logging and monitoring
26. Microservice-ready API architecture
27. Webhooks and callback URLs
28. Consuming external APIs
29. Deployment and production readiness
30. Final project cleanup and interview review

---

## Final Project Direction

The recommended final project is a Mini ERP API because it matches real business software experience.

Possible modules:

- users
- roles
- permissions
- customers
- products
- orders
- order items
- invoices
- payments
- attachments
- activity logs

This gives enough real-world depth to practice API design, authentication, authorization, validation, testing, performance, and documentation.

---

## Success Standard

At the end of this practice, I should be able to say:

> I built a Laravel REST API project with authentication, authorization, resource responses, validation, pagination, filtering, versioning, rate limiting, caching, file uploads, queues, webhooks, external API integration, feature tests, documentation, and production-oriented error handling. I can explain the design decisions behind each part.

That is the level this repository is designed to reach.
