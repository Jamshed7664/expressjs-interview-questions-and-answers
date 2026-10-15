<div align="center">

# 🚀 Top 100 Express.js Interview Questions & Answers (2026)

### From Beginner to Advanced | Easy Indian English | Practical JavaScript Examples

**Made with ❤️ by Code with Jamshed**

![Express](https://img.shields.io/badge/Express.js-5.x-000000?logo=express&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=nodedotjs&logoColor=white) ![Questions](https://img.shields.io/badge/Interview_Questions-100-2563eb) ![Level](https://img.shields.io/badge/Level-Beginner_to_Advanced-9333ea) ![License](https://img.shields.io/badge/License-MIT-yellow)

**A friendly Express.js interview guide for freshers and experienced backend developers.**

</div>

---

> ⭐ If this guide helps you prepare, please star the repository and share it with other developers.

## 📚 What You Will Learn

- 100 carefully organised interview questions with clear answers and code examples.
- Express 5 fundamentals, middleware, routers, REST APIs, authentication, security, testing and deployment.
- Practical interview tips, common mistakes and simple examples.
- Examples mostly use **CommonJS** (`require`) and **Express 5**.

> **Important:** Some examples are focused snippets, not standalone runnable programs. Assume `app` is an Express application, required modules are imported, and sample project-specific handlers/services exist unless shown. Never paste placeholder secrets into production.

## ⚡ Quick Start

**Requirements:** Node.js 18+ and npm.

```bash
mkdir expressjs-interview-prep
cd expressjs-interview-prep
npm init -y
npm install express@5
```

Create `app.js`:

```js
const express = require("express");
const app = express();

app.use(express.json());

app.get("/", (req, res) => {
  res.json({ message: "Hello from Code with Jamshed!" });
});

app.listen(3000, () => console.log("Server running: http://localhost:3000"));
```

```bash
node app.js
```

Visit `http://localhost:3000`.

## 🧭 Table of Contents

- [Express.js Fundamentals (Q1–Q10)](#expressjs-fundamentals)
- [Middleware & Request Lifecycle (Q11–Q20)](#middleware--request-lifecycle)
- [Routing & URL Handling (Q21–Q30)](#routing--url-handling)
- [Requests & Responses (Q31–Q40)](#requests--responses)
- [REST API Design (Q41–Q50)](#rest-api-design)
- [Error Handling (Q51–Q60)](#error-handling)
- [Authentication & Security (Q61–Q75)](#authentication--security)
- [Database & Architecture (Q76–Q85)](#database--architecture)
- [Testing & Real-Time APIs (Q86–Q90)](#testing--real-time-apis)
- [Performance, Deployment & Advanced (Q91–Q100)](#performance-deployment--advanced)

<details>
<summary><strong>🔎 Expand all 100 question links</strong></summary>

1. [Q1. What is Express.js?](#q1-what-is-expressjs)
2. [Q2. Why do developers use Express.js?](#q2-why-do-developers-use-expressjs)
3. [Q3. How do you install Express 5?](#q3-how-do-you-install-express-5)
4. [Q4. How do you start a basic Express server?](#q4-how-do-you-start-a-basic-express-server)
5. [Q5. What is the Express application object?](#q5-what-is-the-express-application-object)
6. [Q6. What are req and res?](#q6-what-are-req-and-res)
7. [Q7. What is a route in Express?](#q7-what-is-a-route-in-express)
8. [Q8. How does Express differ from Node.js?](#q8-how-does-express-differ-from-nodejs)
9. [Q9. What is an HTTP request-response cycle?](#q9-what-is-an-http-request-response-cycle)
10. [Q10. How do you configure a port?](#q10-how-do-you-configure-a-port)
11. [Q11. What is middleware?](#q11-what-is-middleware)
12. [Q12. What does next() do?](#q12-what-does-next-do)
13. [Q13. What is application-level middleware?](#q13-what-is-application-level-middleware)
14. [Q14. What is router-level middleware?](#q14-what-is-router-level-middleware)
15. [Q15. What is built-in middleware?](#q15-what-is-built-in-middleware)
16. [Q16. How does express.json() work?](#q16-how-does-expressjson-work)
17. [Q17. What does express.urlencoded() do?](#q17-what-does-expressurlencoded-do)
18. [Q18. Why is middleware order important?](#q18-why-is-middleware-order-important)
19. [Q19. What is third-party middleware?](#q19-what-is-third-party-middleware)
20. [Q20. What is a middleware chain?](#q20-what-is-a-middleware-chain)
21. [Q21. What is express.Router()?](#q21-what-is-expressrouter)
22. [Q22. What is the difference between GET and POST?](#q22-what-is-the-difference-between-get-and-post)
23. [Q23. How do PUT and PATCH differ?](#q23-how-do-put-and-patch-differ)
24. [Q24. How do you handle DELETE requests?](#q24-how-do-you-handle-delete-requests)
25. [Q25. What are route parameters?](#q25-what-are-route-parameters)
26. [Q26. What are query parameters?](#q26-what-are-query-parameters)
27. [Q27. How can you get request headers?](#q27-how-can-you-get-request-headers)
28. [Q28. What is app.all()?](#q28-what-is-appall)
29. [Q29. How do you implement a 404 handler?](#q29-how-do-you-implement-a-404-handler)
30. [Q30. What changed in wildcard routing in Express 5?](#q30-what-changed-in-wildcard-routing-in-express-5)
31. [Q31. What is res.send()?](#q31-what-is-ressend)
32. [Q32. What is res.json()?](#q32-what-is-resjson)
33. [Q33. What is res.status()?](#q33-what-is-resstatus)
34. [Q34. What does res.sendStatus() do?](#q34-what-does-ressendstatus-do)
35. [Q35. How do you send custom response headers?](#q35-how-do-you-send-custom-response-headers)
36. [Q36. How do you redirect a client?](#q36-how-do-you-redirect-a-client)
37. [Q37. How do you send a file?](#q37-how-do-you-send-a-file)
38. [Q38. How do you serve static assets?](#q38-how-do-you-serve-static-assets)
39. [Q39. How do you set cookies?](#q39-how-do-you-set-cookies)
40. [Q40. How do you read a request body?](#q40-how-do-you-read-a-request-body)
41. [Q41. What is REST in an Express API?](#q41-what-is-rest-in-an-express-api)
42. [Q42. What is CRUD?](#q42-what-is-crud)
43. [Q43. What is the right status for creating a resource?](#q43-what-is-the-right-status-for-creating-a-resource)
44. [Q44. How do you implement pagination?](#q44-how-do-you-implement-pagination)
45. [Q45. What is API versioning?](#q45-what-is-api-versioning)
46. [Q46. How do you validate API input?](#q46-how-do-you-validate-api-input)
47. [Q47. What is idempotency?](#q47-what-is-idempotency)
48. [Q48. How do you design consistent API errors?](#q48-how-do-you-design-consistent-api-errors)
49. [Q49. How do you create a health-check endpoint?](#q49-how-do-you-create-a-health-check-endpoint)
50. [Q50. What is content negotiation?](#q50-what-is-content-negotiation)
51. [Q51. What is Express error-handling middleware?](#q51-what-is-express-error-handling-middleware)
52. [Q52. What does next(err) do?](#q52-what-does-nexterr-do)
53. [Q53. How does Express 5 handle async errors?](#q53-how-does-express-5-handle-async-errors)
54. [Q54. How do you create a custom 404 error?](#q54-how-do-you-create-a-custom-404-error)
55. [Q55. What is a custom error class?](#q55-what-is-a-custom-error-class)
56. [Q56. Why check res.headersSent?](#q56-why-check-resheaderssent)
57. [Q57. How do you deal with unhandled async callback errors?](#q57-how-do-you-deal-with-unhandled-async-callback-errors)
58. [Q58. What is the difference between 400 and 422?](#q58-what-is-the-difference-between-400-and-422)
59. [Q59. How do you log errors safely?](#q59-how-do-you-log-errors-safely)
60. [Q60. What is error-handling order?](#q60-what-is-error-handling-order)
61. [Q61. What is a global error response strategy?](#q61-what-is-a-global-error-response-strategy)
62. [Q62. What is authentication?](#q62-what-is-authentication)
63. [Q63. What is authorization?](#q63-what-is-authorization)
64. [Q64. How can JWT authentication work in Express?](#q64-how-can-jwt-authentication-work-in-express)
65. [Q65. What is session authentication?](#q65-what-is-session-authentication)
66. [Q66. How should passwords be stored?](#q66-how-should-passwords-be-stored)
67. [Q67. What is CORS?](#q67-what-is-cors)
68. [Q68. How do you handle a CORS preflight?](#q68-how-do-you-handle-a-cors-preflight)
69. [Q69. What is Helmet middleware?](#q69-what-is-helmet-middleware)
70. [Q70. How do you apply rate limiting?](#q70-how-do-you-apply-rate-limiting)
71. [Q71. What is CSRF and when does it matter?](#q71-what-is-csrf-and-when-does-it-matter)
72. [Q72. How do you prevent injection attacks?](#q72-how-do-you-prevent-injection-attacks)
73. [Q73. What is the safest way to manage secrets?](#q73-what-is-the-safest-way-to-manage-secrets)
74. [Q74. How do you control request body size?](#q74-how-do-you-control-request-body-size)
75. [Q75. What is the role of HTTPS and trust proxy?](#q75-what-is-the-role-of-https-and-trust-proxy)
76. [Q76. How do you connect Express with MongoDB?](#q76-how-do-you-connect-express-with-mongodb)
77. [Q77. How do you connect Express with PostgreSQL?](#q77-how-do-you-connect-express-with-postgresql)
78. [Q78. What is an Express controller?](#q78-what-is-an-express-controller)
79. [Q79. What is a service layer?](#q79-what-is-a-service-layer)
80. [Q80. What is dependency injection in Express?](#q80-what-is-dependency-injection-in-express)
81. [Q81. How do you implement file uploads?](#q81-how-do-you-implement-file-uploads)
82. [Q82. How does Express support WebSockets?](#q82-how-does-express-support-websockets)
83. [Q83. What are Server-Sent Events (SSE)?](#q83-what-are-server-sent-events-sse)
84. [Q84. What is a background job queue?](#q84-what-is-a-background-job-queue)
85. [Q85. How do you test an Express endpoint?](#q85-how-do-you-test-an-express-endpoint)
86. [Q86. What is unit testing versus integration testing?](#q86-what-is-unit-testing-versus-integration-testing)
87. [Q87. How do you mock a service in route tests?](#q87-how-do-you-mock-a-service-in-route-tests)
88. [Q88. How do you enable response compression?](#q88-how-do-you-enable-response-compression)
89. [Q89. How do you cache responses?](#q89-how-do-you-cache-responses)
90. [Q90. What is graceful shutdown?](#q90-what-is-graceful-shutdown)
91. [Q91. How do you deploy Express behind a reverse proxy?](#q91-how-do-you-deploy-express-behind-a-reverse-proxy)
92. [Q92. How do you avoid blocking the event loop?](#q92-how-do-you-avoid-blocking-the-event-loop)
93. [Q93. How do you organise a production Express project?](#q93-how-do-you-organise-a-production-express-project)
94. [Q94. What is observability in Express?](#q94-what-is-observability-in-express)
95. [Q95. What is API documentation using OpenAPI?](#q95-what-is-api-documentation-using-openapi)
96. [Q96. What changed from Express 4 to Express 5?](#q96-what-changed-from-express-4-to-express-5)
97. [Q97. How do you add request timeouts?](#q97-how-do-you-add-request-timeouts)
98. [Q98. How do you implement feature flags?](#q98-how-do-you-implement-feature-flags)
99. [Q99. How do you protect Express from duplicate writes?](#q99-how-do-you-protect-express-from-duplicate-writes)
100. [Q100. How can you profile slow Express endpoints?](#q100-how-can-you-profile-slow-express-endpoints)

</details>

---

## Express.js Fundamentals

---

### Q1. What is Express.js?

**Easy Answer:**

Express.js is a small and flexible web framework for Node.js. It helps us create APIs, routes and middleware without writing the same HTTP boilerplate again.

**Code Example:**

```js
const express = require('express');
const app = express();
app.get('/', (req, res) => res.send('Hello Express'));
app.listen(3000);
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q2. Why do developers use Express.js?

**Easy Answer:**

Express makes HTTP routing, JSON responses, middleware, and error handling easy. It is a good choice when we want to build a REST API quickly.

**Code Example:**

```js
app.get('/health', (req, res) => res.json({ status: 'ok' }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q3. How do you install Express 5?

**Easy Answer:**

Use npm in a Node.js project. Express 5 requires Node.js 18 or later. A package-lock file helps keep installs reproducible.

**Code Example:**

```js
npm init -y
npm install express@5
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q4. How do you start a basic Express server?

**Easy Answer:**

Create an app, define a route and call listen. The port identifies where the server accepts incoming requests.

**Code Example:**

```js
const express = require('express');
const app = express();
app.get('/', (req, res) => res.send('Welcome'));
app.listen(3000, () => console.log('Running on 3000'));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q5. What is the Express application object?

**Easy Answer:**

The value returned by express() is the main app. We add global middleware, routes and settings to this object.

**Code Example:**

```js
const app = require('express')();
app.set('trust proxy', false);
app.get('/ping', (req, res) => res.send('pong'));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q6. What are req and res?

**Easy Answer:**

req represents incoming HTTP request details. res is used to send an HTTP response back to the client.

**Code Example:**

```js
app.get('/hello', (req, res) => {
  res.json({ method: req.method, path: req.path });
});
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q7. What is a route in Express?

**Easy Answer:**

A route matches an HTTP method and URL path, then executes one or more handlers. For example GET /users handles a request to read users.

**Code Example:**

```js
app.get('/users', (req, res) => res.json([{ id: 1, name: 'Asha' }]));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q8. How does Express differ from Node.js?

**Easy Answer:**

Node.js is the JavaScript runtime and provides low-level HTTP APIs. Express runs on Node.js and adds convenient routing and middleware abstractions.

**Code Example:**

```js
const http = require('node:http');
// Node: http.createServer(handler)
// Express: app.get('/path', handler)
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q9. What is an HTTP request-response cycle?

**Easy Answer:**

Client sends a request, middleware and route handlers process it, and the server sends one response. Each handler should respond or pass control onwards.

**Code Example:**

```js
app.get('/time', (req, res) => res.json({ now: new Date().toISOString() }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q10. How do you configure a port?

**Easy Answer:**

Read PORT from environment, with a local default. This allows hosting platforms to choose their own port.

**Code Example:**

```js
const port = Number(process.env.PORT || 3000);
app.listen(port, () => console.log(`Listening on ${port}`));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Middleware & Request Lifecycle

---

### Q11. What is middleware?

**Easy Answer:**

Middleware is a function running between request and response. It can log, authenticate, modify the request or finish the response.

**Code Example:**

```js
app.use((req, res, next) => {
  console.log(req.method, req.path);
  next();
});
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q12. What does next() do?

**Easy Answer:**

next() passes control to the next matching middleware or route handler. If you neither respond nor call next, the request can hang.

**Code Example:**

```js
app.use((req, res, next) => {
  req.receivedAt = Date.now();
  next();
});
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q13. What is application-level middleware?

**Easy Answer:**

It is registered with app.use() or app.METHOD() and can run for all or selected paths. Order matters.

**Code Example:**

```js
app.use('/api', (req, res, next) => {
  console.log('API request');
  next();
});
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q14. What is router-level middleware?

**Easy Answer:**

A Router groups routes and middleware for a feature. This helps organise medium and large projects.

**Code Example:**

```js
const router = express.Router();
router.use((req, res, next) => { next(); });
router.get('/', (req, res) => res.send('Users'));
app.use('/users', router);
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q15. What is built-in middleware?

**Easy Answer:**

Express already provides helpful middleware such as express.json(), express.urlencoded() and express.static().

**Code Example:**

```js
app.use(express.json());
app.use(express.urlencoded({ extended: false }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q16. How does express.json() work?

**Easy Answer:**

It parses matching JSON request bodies and assigns the parsed value to req.body. Always validate that value because it comes from the client.

**Code Example:**

```js
app.use(express.json({ limit: '100kb' }));
app.post('/items', (req, res) => res.json(req.body));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q17. What does express.urlencoded() do?

**Easy Answer:**

It parses URL-encoded form submissions, like name=Asha. The extended option controls nested-form parsing behaviour.

**Code Example:**

```js
app.use(express.urlencoded({ extended: false }));
app.post('/form', (req, res) => res.json(req.body));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q18. Why is middleware order important?

**Easy Answer:**

Express runs matching middleware in registration order. Place JSON parsing before routes that need req.body and error handling after routes.

**Code Example:**

```js
app.use(express.json());
app.post('/save', (req, res) => res.json(req.body));
app.use((err, req, res, next) => res.status(500).json({ error: 'Server error' }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q19. What is third-party middleware?

**Easy Answer:**

These are packages created outside Express, for example helmet for security headers and cors for browser cross-origin access.

**Code Example:**

```js
const helmet = require('helmet'); // npm i helmet
app.use(helmet());
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q20. What is a middleware chain?

**Easy Answer:**

Multiple handlers can be attached to the same route. Each calls next() so Express can continue to the following handler.

**Code Example:**

```js
const validate = (req, res, next) => { next(); };
app.get('/profile', validate, (req, res) => res.send('Profile'));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Routing & URL Handling

---

### Q21. What is express.Router()?

**Easy Answer:**

It is a mini routing object. Mount it under a path prefix so feature routes remain separate from the main app.

**Code Example:**

```js
const users = express.Router();
users.get('/:id', (req, res) => res.json({ id: req.params.id }));
app.use('/api/users', users);
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q22. What is the difference between GET and POST?

**Easy Answer:**

GET usually reads data and POST usually creates data or triggers an operation. HTTP semantics matter for caching and clients.

**Code Example:**

```js
app.get('/tasks', (req, res) => res.json([]));
app.post('/tasks', (req, res) => res.status(201).json({ created: true }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q23. How do PUT and PATCH differ?

**Easy Answer:**

PUT commonly replaces a resource representation; PATCH makes a partial update. Your API should clearly document its exact behaviour.

**Code Example:**

```js
app.put('/users/:id', (req, res) => res.json({ replaced: req.params.id }));
app.patch('/users/:id', (req, res) => res.json({ updated: req.params.id }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q24. How do you handle DELETE requests?

**Easy Answer:**

Use app.delete() to define a deletion endpoint. A successful delete may return status 204 with no body.

**Code Example:**

```js
app.delete('/users/:id', (req, res) => res.sendStatus(204));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q25. What are route parameters?

**Easy Answer:**

They are dynamic values inside URL paths, like :id. Express exposes them through req.params, which must be validated.

**Code Example:**

```js
app.get('/users/:id', (req, res) => res.json({ id: req.params.id }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q26. What are query parameters?

**Easy Answer:**

Query parameters appear after ? in the URL. Express provides them through req.query. They are untrusted input.

**Code Example:**

```js
app.get('/search', (req, res) => res.json({ term: req.query.q ?? '' }));
// GET /search?q=node
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q27. How can you get request headers?

**Easy Answer:**

Use req.get('Header-Name') or req.headers. A header may be missing, so handle undefined values.

**Code Example:**

```js
app.get('/client', (req, res) => {
  res.json({ agent: req.get('User-Agent') ?? 'unknown' });
});
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q28. What is app.all()?

**Easy Answer:**

It matches all HTTP methods for a specified path. It is useful for shared route-specific checks.

**Code Example:**

```js
app.all('/private', (req, res, next) => {
  console.log('Checking private route'); next();
});
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q29. How do you implement a 404 handler?

**Easy Answer:**

Place a normal middleware after all routes. If nothing matched before it, respond with 404.

**Code Example:**

```js
app.use((req, res) => res.status(404).json({ message: 'Not found' }));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q30. What changed in wildcard routing in Express 5?

**Easy Answer:**

In Express 5, wildcards need names. Use /{*splat} to also include the root route, instead of the old unnamed * patterns.

**Code Example:**

```js
app.get('/{*splat}', (req, res) => res.send('Fallback'));
```

**Interview Tip:** Remember to explain the request flow, what Express does, and why this matters in a real API.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Requests & Responses

---

### Q31. What is res.send()?

**Easy Answer:**

res.send() sends text, HTML, Buffer or other supported response bodies. Express sets suitable content headers.

**Code Example:**

```js
app.get('/welcome', (req, res) => res.send('Hello from API'));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q32. What is res.json()?

**Easy Answer:**

res.json() serialises a JavaScript value as JSON and sends it to the client. It is a common API response method.

**Code Example:**

```js
app.get('/status', (req, res) => res.json({ ready: true }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q33. What is res.status()?

**Easy Answer:**

It sets the HTTP status code for a response. Return a meaningful code with the message body.

**Code Example:**

```js
app.post('/orders', (req, res) => res.status(201).json({ id: 42 }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q34. What does res.sendStatus() do?

**Easy Answer:**

It sets an HTTP status and sends its standard short status message, except codes such as 204 that do not allow a response body.

**Code Example:**

```js
app.get('/no-content', (req, res) => res.sendStatus(204));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q35. How do you send custom response headers?

**Easy Answer:**

Use res.set() to send headers such as Cache-Control or custom tracing identifiers.

**Code Example:**

```js
app.get('/data', (req, res) => {
  res.set('Cache-Control', 'no-store');
  res.json({ private: true });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q36. How do you redirect a client?

**Easy Answer:**

res.redirect() sends a redirect response so the browser or HTTP client can request another URL.

**Code Example:**

```js
app.get('/old', (req, res) => res.redirect(301, '/new'));
app.get('/new', (req, res) => res.send('New page'));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q37. How do you send a file?

**Easy Answer:**

res.sendFile() sends a file using an absolute path. Never pass unchecked user-controlled paths.

**Code Example:**

```js
const path = require('node:path');
app.get('/report', (req, res) => {
  res.sendFile(path.join(__dirname, 'public', 'report.pdf'));
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q38. How do you serve static assets?

**Easy Answer:**

express.static() serves files such as CSS, JavaScript or images from a folder. Keep private files outside that folder.

**Code Example:**

```js
const path = require('node:path');
app.use('/assets', express.static(path.join(__dirname, 'public')));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q39. How do you set cookies?

**Easy Answer:**

Use res.cookie() with secure options. Cookies containing sensitive session identifiers should be httpOnly, secure over HTTPS and have suitable sameSite settings.

**Code Example:**

```js
app.get('/set-cookie', (req, res) => {
  res.cookie('theme', 'dark', { httpOnly: true, sameSite: 'lax' });
  res.send('Saved');
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q40. How do you read a request body?

**Easy Answer:**

First register a parser, then read req.body. In Express 5, req.body can be undefined when no body was parsed.

**Code Example:**

```js
app.use(express.json());
app.post('/echo', (req, res) => res.json({ data: req.body ?? null }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## REST API Design

---

### Q41. What is REST in an Express API?

**Easy Answer:**

REST uses resource-oriented URLs and HTTP methods. Express does not enforce REST, but makes it easy to build these endpoints.

**Code Example:**

```js
app.get('/books', (req, res) => res.json([]));
app.get('/books/:id', (req, res) => res.json({ id: req.params.id }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q42. What is CRUD?

**Easy Answer:**

CRUD means Create, Read, Update and Delete. It maps naturally to POST, GET, PUT/PATCH and DELETE routes.

**Code Example:**

```js
app.post('/notes', createNote);
app.get('/notes', listNotes);
app.patch('/notes/:id', updateNote);
app.delete('/notes/:id', deleteNote);
// Handlers are project-specific functions.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q43. What is the right status for creating a resource?

**Easy Answer:**

201 Created is commonly used when a POST request successfully creates a resource. You can also include a Location header.

**Code Example:**

```js
app.post('/items', (req, res) => {
  res.location('/items/123').status(201).json({ id: '123' });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q44. How do you implement pagination?

**Easy Answer:**

Accept page and limit, validate them, and query only the required items. For large datasets cursor pagination can work better.

**Code Example:**

```js
app.get('/products', (req, res) => {
  const page = Math.max(1, Number(req.query.page) || 1);
  const limit = Math.min(50, Math.max(1, Number(req.query.limit) || 10));
  res.json({ page, limit });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q45. What is API versioning?

**Easy Answer:**

It allows API contracts to change without immediately breaking existing clients. URL versioning is one easy approach.

**Code Example:**

```js
app.get('/api/v1/users', (req, res) => res.json({ version: 1, users: [] }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q46. How do you validate API input?

**Easy Answer:**

Use a validation library or explicit checks before storing data. Never assume req.body has the expected shape.

**Code Example:**

```js
app.post('/users', (req, res) => {
  const name = req.body?.name;
  if (typeof name !== 'string' || !name.trim()) return res.status(400).json({ error: 'Name required' });
  res.status(201).json({ name: name.trim() });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q47. What is idempotency?

**Easy Answer:**

Repeating an idempotent request has the same intended resource effect as doing it once. PUT and DELETE are designed to be idempotent; POST often is not.

**Code Example:**

```js
app.put('/settings/theme', (req, res) => {
  // Setting the same theme again should have the same final effect.
  res.json({ theme: req.body?.theme });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q48. How do you design consistent API errors?

**Easy Answer:**

Respond using predictable JSON fields, status codes and safe messages. Do not expose stack traces or secrets to users.

**Code Example:**

```js
res.status(400).json({ error: { code: 'INVALID_INPUT', message: 'Check submitted fields' } });
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q49. How do you create a health-check endpoint?

**Easy Answer:**

Expose a lightweight endpoint for load balancers and monitoring. A readiness check can separately test required dependencies.

**Code Example:**

```js
app.get('/health', (req, res) => res.status(200).json({ status: 'ok' }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q50. What is content negotiation?

**Easy Answer:**

Clients send Accept headers to express response preferences. Use req.accepts() to check supported content types.

**Code Example:**

```js
app.get('/format', (req, res) => {
  if (!req.accepts('json')) return res.sendStatus(406);
  res.json({ message: 'JSON supported' });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Error Handling

---

### Q51. What is Express error-handling middleware?

**Easy Answer:**

It has four parameters: err, req, res, next. Put it after routes to handle failures in one place.

**Code Example:**

```js
app.use((err, req, res, next) => {
  if (res.headersSent) return next(err);
  res.status(500).json({ error: 'Internal server error' });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q52. What does next(err) do?

**Easy Answer:**

It skips normal middleware and forwards the error to matching error-handling middleware. Useful for callback-based APIs.

**Code Example:**

```js
app.get('/failed', (req, res, next) => {
  next(new Error('Something failed'));
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q53. How does Express 5 handle async errors?

**Easy Answer:**

A rejected Promise or thrown error from an async route handler is forwarded automatically to the error handler. This is an Express 5 feature.

**Code Example:**

```js
app.get('/users', async (req, res) => {
  throw new Error('Database unavailable');
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q54. How do you create a custom 404 error?

**Easy Answer:**

Return 404 when a known resource ID does not exist. This differs from a catch-all 404 for unmatched routes.

**Code Example:**

```js
app.get('/posts/:id', (req, res) => {
  const post = null;
  if (!post) return res.status(404).json({ error: 'Post not found' });
  res.json(post);
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q55. What is a custom error class?

**Easy Answer:**

A custom Error subclass can carry an HTTP status and an application error code. Central middleware can translate it into a response.

**Code Example:**

```js
class AppError extends Error {
  constructor(message, status = 500) { super(message); this.status = status; }
}
throw new AppError('Invalid request', 400);
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q56. Why check res.headersSent?

**Easy Answer:**

If headers were already sent, we cannot start another normal JSON response. Delegate to Express's default error handler.

**Code Example:**

```js
app.use((err, req, res, next) => {
  if (res.headersSent) return next(err);
  res.status(500).json({ error: 'Unexpected failure' });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q57. How do you deal with unhandled async callback errors?

**Easy Answer:**

Errors inside timer callbacks are not returned as the route's Promise. Catch them and pass them to next(err).

**Code Example:**

```js
app.get('/timer', (req, res, next) => {
  setTimeout(() => {
    try { throw new Error('Timer failed'); } catch (err) { next(err); }
  }, 10);
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q58. What is the difference between 400 and 422?

**Easy Answer:**

400 usually means the request is invalid or malformed. 422 is often used for syntactically valid input that fails domain validation; choose a consistent API policy.

**Code Example:**

```js
app.post('/register', (req, res) => {
  if (!req.body?.email) return res.status(422).json({ error: 'Email required' });
  res.sendStatus(201);
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q59. How do you log errors safely?

**Easy Answer:**

Log useful server-side context but avoid passwords, tokens or full sensitive bodies. Send a generic public message.

**Code Example:**

```js
app.use((err, req, res, next) => {
  console.error({ path: req.path, message: err.message });
  if (res.headersSent) return next(err);
  res.status(500).json({ error: 'Internal server error' });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q60. What is error-handling order?

**Easy Answer:**

A custom error handler should be registered after the routes it protects. Express chooses error middleware only when an error is forwarded.

**Code Example:**

```js
app.get('/boom', () => { throw new Error('Boom'); });
app.use((err, req, res, next) => res.status(500).send('Handled'));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Authentication & Security

---

### Q61. What is a global error response strategy?

**Easy Answer:**

Map known validation and business errors to clear 4xx codes, and unknown failures to a generic 500. Preserve details in internal logs.

**Code Example:**

```js
app.use((err, req, res, next) => {
  if (res.headersSent) return next(err);
  const code = Number.isInteger(err.status) && err.status >= 400 && err.status < 500 ? err.status : 500;
  res.status(code).json({ error: code === 500 ? 'Server error' : err.message });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q62. What is authentication?

**Easy Answer:**

Authentication checks who the user is. Login can create a session or issue an access token after credentials are verified.

**Code Example:**

```js
const requireLogin = (req, res, next) => {
  if (!req.user) return res.sendStatus(401);
  next();
};
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q63. What is authorization?

**Easy Answer:**

Authorization decides what an authenticated user is allowed to do. A logged-in user should not automatically access an admin route.

**Code Example:**

```js
const requireAdmin = (req, res, next) => {
  if (req.user?.role !== 'admin') return res.sendStatus(403);
  next();
};
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q64. How can JWT authentication work in Express?

**Easy Answer:**

Client sends a signed bearer token; server verifies signature, issuer, audience and expiry, then derives the user identity. Never just decode and trust claims.

**Code Example:**

```js
const jwt = require('jsonwebtoken'); // npm i jsonwebtoken
const token = req.get('Authorization')?.replace(/^Bearer /, '');
const claims = jwt.verify(token, process.env.JWT_SECRET, { algorithms: ['HS256'] });
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q65. What is session authentication?

**Easy Answer:**

Session authentication stores session state on the server, identified by a browser cookie. Use a production session store instead of the default MemoryStore.

**Code Example:**

```js
const session = require('express-session'); // npm i express-session
app.use(session({ secret: process.env.SESSION_SECRET, resave: false, saveUninitialized: false, cookie: { httpOnly: true, secure: true, sameSite: 'lax' } }));
// Behind a trusted HTTPS proxy configure trust proxy correctly.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q66. How should passwords be stored?

**Easy Answer:**

Never store plaintext passwords. Hash them with a password hashing algorithm such as Argon2id or bcrypt and verify on login.

**Code Example:**

```js
const bcrypt = require('bcrypt'); // npm i bcrypt
const hash = await bcrypt.hash(password, 12);
const isValid = await bcrypt.compare(password, hash);
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q67. What is CORS?

**Easy Answer:**

CORS is a browser security mechanism controlling whether frontend JavaScript may read a cross-origin response. It is not authentication.

**Code Example:**

```js
const cors = require('cors'); // npm i cors
app.use(cors({ origin: 'https://app.example.com' }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q68. How do you handle a CORS preflight?

**Easy Answer:**

Browsers can send an OPTIONS request before certain cross-origin requests. The cors middleware typically handles the needed preflight response.

**Code Example:**

```js
const cors = require('cors');
app.use(cors({ origin: 'https://app.example.com', methods: ['GET', 'POST'] }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q69. What is Helmet middleware?

**Easy Answer:**

Helmet sets a number of helpful HTTP security headers. It supports defence in depth but does not replace input validation or authentication.

**Code Example:**

```js
const helmet = require('helmet'); // npm i helmet
app.use(helmet());
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q70. How do you apply rate limiting?

**Easy Answer:**

Limit requests to sensitive endpoints to reduce brute-force and abuse. Use a shared store when running multiple app instances.

**Code Example:**

```js
const rateLimit = require('express-rate-limit'); // npm i express-rate-limit
app.use('/login', rateLimit({ windowMs: 60_000, limit: 5, standardHeaders: 'draft-8', legacyHeaders: false }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q71. What is CSRF and when does it matter?

**Easy Answer:**

CSRF tricks a browser into sending an authenticated request. It especially matters for cookie-based authentication; consider SameSite cookies, CSRF tokens and Origin checking.

**Code Example:**

```js
app.post('/transfer', requireLogin, verifyCsrfToken, transferMoney);
// verifyCsrfToken and transferMoney are application handlers.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q72. How do you prevent injection attacks?

**Easy Answer:**

Validate inputs and use parameterised database queries. Never build SQL directly from untrusted strings.

**Code Example:**

```js
const result = await db.query('SELECT * FROM users WHERE id = $1', [req.params.id]);
// db is a configured database client.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q73. What is the safest way to manage secrets?

**Easy Answer:**

Put secrets in environment variables or a secret manager, never in a public Git repo. Rotate secrets if exposed.

**Code Example:**

```js
const secret = process.env.JWT_SECRET;
if (!secret) throw new Error('Missing JWT_SECRET');
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q74. How do you control request body size?

**Easy Answer:**

Limit JSON and upload sizes to reduce memory abuse. Choose limits based on product requirements.

**Code Example:**

```js
app.use(express.json({ limit: '100kb' }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q75. What is the role of HTTPS and trust proxy?

**Easy Answer:**

HTTPS protects data in transit. Behind a trusted reverse proxy, configure trust proxy carefully so Express interprets secure connections correctly.

**Code Example:**

```js
// Only enable when the proxy topology is known and trusted.
app.set('trust proxy', 1);
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Database & Architecture

---

### Q76. How do you connect Express with MongoDB?

**Easy Answer:**

Use a database client such as Mongoose. Connect once during startup and share models with route handlers.

**Code Example:**

```js
const mongoose = require('mongoose'); // npm i mongoose
await mongoose.connect(process.env.MONGODB_URI);
// Define models separately and use them in controllers.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q77. How do you connect Express with PostgreSQL?

**Easy Answer:**

Use a connection pool such as pg and parameterised SQL. Keep credentials in environment variables.

**Code Example:**

```js
const { Pool } = require('pg'); // npm i pg
const pool = new Pool({ connectionString: process.env.DATABASE_URL });
const result = await pool.query('SELECT NOW()');
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q78. What is an Express controller?

**Easy Answer:**

A controller is a function containing the HTTP request handling logic. Separating controllers from routers keeps routes readable.

**Code Example:**

```js
const listUsers = (req, res) => res.json([]);
router.get('/users', listUsers);
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q79. What is a service layer?

**Easy Answer:**

A service holds reusable business logic without relying on HTTP request or response objects. Controllers call services.

**Code Example:**

```js
const userService = { findById: async (id) => ({ id, name: 'Asha' }) };
app.get('/users/:id', async (req, res) => {
  res.json(await userService.findById(req.params.id));
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q80. What is dependency injection in Express?

**Easy Answer:**

Pass dependencies into controller factories instead of importing them globally. It simplifies mocking and testing.

**Code Example:**

```js
const makeGetUser = (userRepo) => async (req, res) => {
  res.json(await userRepo.find(req.params.id));
};
router.get('/:id', makeGetUser(userRepository));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q81. How do you implement file uploads?

**Easy Answer:**

Use upload middleware such as multer, validate size and type, and store uploads outside public static folders. Do not trust user filenames.

**Code Example:**

```js
const multer = require('multer'); // npm i multer
const upload = multer({ dest: 'tmp/', limits: { fileSize: 2 * 1024 * 1024 } });
app.post('/upload', upload.single('avatar'), (req, res) => res.json({ uploaded: Boolean(req.file) }));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q82. How does Express support WebSockets?

**Easy Answer:**

Express handles ordinary HTTP routes. A WebSocket library like ws can attach to the underlying Node.js HTTP server.

**Code Example:**

```js
const { WebSocketServer } = require('ws'); // npm i ws
const server = app.listen(3000);
const wss = new WebSocketServer({ server });
wss.on('connection', socket => socket.send('Connected'));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q83. What are Server-Sent Events (SSE)?

**Easy Answer:**

SSE streams one-way server updates using text/event-stream. It is suitable for notifications and live progress where client-to-server messaging is not required.

**Code Example:**

```js
app.get('/events', (req, res) => {
  res.set('Content-Type', 'text/event-stream');
  res.write('data: Connected\
\
');
  req.on('close', () => res.end());
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q84. What is a background job queue?

**Easy Answer:**

A queue moves slow work like email processing outside the HTTP response path. Worker processes consume tasks later.

**Code Example:**

```js
app.post('/emails', async (req, res) => {
  await emailQueue.add('send', { recipient: req.body.email });
  res.status(202).json({ queued: true });
});
// emailQueue is a configured queue such as BullMQ.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q85. How do you test an Express endpoint?

**Easy Answer:**

Use a test framework and Supertest to make HTTP-style requests without deploying the server.

**Code Example:**

```js
const request = require('supertest'); // npm i -D supertest
const response = await request(app).get('/health');
expect(response.status).toBe(200);
// Use inside a test runner like Jest.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Testing & Real-Time APIs

---

### Q86. What is unit testing versus integration testing?

**Easy Answer:**

Unit tests isolate a small function; integration tests check connected pieces such as routes and database interactions.

**Code Example:**

```js
const sum = (a, b) => a + b;
// Unit: expect(sum(2, 3)).toBe(5)
// Integration: request(app).get('/users')
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q87. How do you mock a service in route tests?

**Easy Answer:**

Inject a fake service so the route test is predictable without accessing a real external API or database.

**Code Example:**

```js
const fakeRepo = { find: async (id) => ({ id, name: 'Test' }) };
const handler = makeGetUser(fakeRepo);
// Mount handler in a test Express app.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q88. How do you enable response compression?

**Easy Answer:**

Compression middleware can reduce response transfer size. Your CDN or reverse proxy may already handle it.

**Code Example:**

```js
const compression = require('compression'); // npm i compression
app.use(compression());
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q89. How do you cache responses?

**Easy Answer:**

Set appropriate HTTP cache headers for public resources; private data usually needs stricter cache controls. Redis can cache expensive computations.

**Code Example:**

```js
app.get('/public-info', (req, res) => {
  res.set('Cache-Control', 'public, max-age=60');
  res.json({ info: 'Public data' });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q90. What is graceful shutdown?

**Easy Answer:**

Stop accepting new traffic and close resources when SIGTERM arrives. This supports safer deployment rollouts.

**Code Example:**

```js
const server = app.listen(3000);
process.on('SIGTERM', () => {
  server.close(() => process.exit(0));
});
// Also close DB pools and add a shutdown timeout in production.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## Performance, Deployment & Advanced

---

### Q91. How do you deploy Express behind a reverse proxy?

**Easy Answer:**

Use a reverse proxy or platform load balancer for TLS termination and request forwarding. Restrict proxy trust to known hops.

**Code Example:**

```js
app.set('trust proxy', 1); // Only for a known one-hop trusted proxy.
app.get('/health', (req, res) => res.sendStatus(200));
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q92. How do you avoid blocking the event loop?

**Easy Answer:**

Do not run long synchronous CPU tasks inside request handlers. Use workers, external jobs or async I/O where appropriate.

**Code Example:**

```js
const fs = require('node:fs/promises');
app.get('/data', async (req, res) => {
  const text = await fs.readFile('data.txt', 'utf8');
  res.type('text').send(text);
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q93. How do you organise a production Express project?

**Easy Answer:**

Separate app configuration, routes, controllers, services, validation and database access. Keep app creation separate from listen() to support tests.

**Code Example:**

```js
// src/app.js -> build and export app
// src/server.js -> connect dependencies and app.listen()
// src/routes/, controllers/, services/, middleware/
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q94. What is observability in Express?

**Easy Answer:**

Logs, metrics and distributed traces help you understand failures and latency. Attach a request ID to correlate requests across services.

**Code Example:**

```js
const crypto = require('node:crypto');
app.use((req, res, next) => {
  req.id = crypto.randomUUID();
  res.set('X-Request-ID', req.id);
  next();
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q95. What is API documentation using OpenAPI?

**Easy Answer:**

An OpenAPI specification describes endpoints, request bodies, responses and authentication. Tools can generate human-friendly API documentation.

**Code Example:**

```js
// openapi.yaml
// paths:
//   /health:
//     get:
//       responses:
//         '200':
//           description: OK
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q96. What changed from Express 4 to Express 5?

**Easy Answer:**

Major changes include automatic forwarding of rejected async handler promises, named wildcards, changed optional route syntax and different req.body defaults. Test before upgrading.

**Code Example:**

```js
// Express 5: named wildcard
app.get('/{*splat}', (req, res) => res.send('Fallback'));
// Express 5 forwards errors from returned rejected Promises.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q97. How do you add request timeouts?

**Easy Answer:**

Timeouts protect resources from very slow requests. Configure limits at the HTTP server and reverse proxy layers; measure workloads before selecting values.

**Code Example:**

```js
const server = app.listen(3000);
server.requestTimeout = 120_000; // milliseconds
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q98. How do you implement feature flags?

**Easy Answer:**

Feature flags allow a gradual rollout without deploying separate code to every user. Evaluate them against trusted user context.

**Code Example:**

```js
app.get('/dashboard', (req, res) => {
  if (process.env.NEW_DASHBOARD === 'true') return res.json({ version: 2 });
  res.json({ version: 1 });
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q99. How do you protect Express from duplicate writes?

**Easy Answer:**

Use an idempotency key and a durable store to recognise retried POST requests. The same key should return the original outcome.

**Code Example:**

```js
app.post('/payments', requireLogin, idempotencyMiddleware, createPayment);
// Back idempotencyMiddleware with atomic storage.
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

### Q100. How can you profile slow Express endpoints?

**Easy Answer:**

Measure route latency using timing middleware and application metrics, then fix the slow database query or blocking task rather than guessing.

**Code Example:**

```js
app.use((req, res, next) => {
  const started = performance.now();
  res.on('finish', () => console.log(req.path, Math.round(performance.now() - started), 'ms'));
  next();
});
```

**Interview Tip:** Tell the interviewer the expected behaviour, key validation/security concern, and one real project use case.

[⬆️ Back to Top](#-top-100-expressjs-interview-questions--answers-2026)

---

## 🎯 Last-Minute Interview Checklist

- Be ready to explain middleware execution order and `next()`.
- Explain `req.params` vs `req.query` vs `req.body`.
- Practise GET, POST, PUT, PATCH and DELETE endpoints.
- Know 200, 201, 204, 400, 401, 403, 404, 422, 429 and 500.
- Understand Express 5 promise errors and error-handling middleware.
- Cover CORS, secure cookies, authentication, authorisation and input validation.
- Test APIs and explain how to deploy with logs and health checks.

## 📖 Official References

- [Express.js Official Documentation](https://expressjs.com/)
- [Express 5 Error Handling](https://expressjs.com/en/5x/guide/error-handling/)
- [Migrating to Express 5](https://expressjs.com/en/guide/migrating-5/)
- [Express Production Security Best Practices](https://expressjs.com/en/advanced/best-practice-security.html)

## 🤝 Contributing

Found an error or want to add a clearer code example? Open an issue or pull request. Keep answers beginner-friendly, technically correct, and focused on Express 5.

## 📜 License

This learning material is intended for use under the MIT License. Add a `LICENSE` file containing the MIT license text to the repository before advertising it as licensed.

---

<div align="center">

### 💙 Keep Learning, Keep Building!

**Code with Jamshed** • JavaScript → React.js → TypeScript → Node.js → Express.js

</div>
