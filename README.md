# NodeJs Interview Questions and Answers

> NodeJs Interviews – Top Questions &amp; Answers for Web Developers

---

## ## **1. What is Node.js?**

Node.js is a runtime environment that lets JavaScript run outside the browser using the V8 engine. It’s designed for building fast, scalable network applications.

---

## **2. Why is Node.js single-threaded?**

Node.js uses a single-threaded model to avoid context switching overhead and simplify asynchronous programming. Heavy work is offloaded to the internal thread-pool.

---

## **3. What is the V8 engine?**

V8 is Google’s high-performance JavaScript engine that compiles JS directly into machine code, making Node.js extremely fast.

---

## **4. What is the Event Loop in Node.js?**

The Event Loop is the heart of Node.js. It handles callbacks, async tasks, timers, I/O operations, and keeps the app non-blocking.

---

## **5. Explain Non-blocking I/O.**

Non-blocking I/O allows Node.js to handle multiple operations simultaneously without waiting for slow tasks like database or file operations.

---

## **6. What is npm?**

npm is the default package manager for Node.js used to install, update, publish, and manage dependencies.

---

## **7. What are Node.js Modules?**

Modules are reusable blocks of code. Node.js supports CommonJS (`require`) and ES Modules (`import`) depending on project settings.

---

## **8. Difference between CommonJS and ES Modules?**

| CommonJS               | ES Modules        |
| ---------------------- | ----------------- |
| require()              | import            |
| Synchronous            | Asynchronous      |
| Used mostly in Node.js | Browser + Node.js |

---

## **9. What is package.json?**

A metadata file that stores project config, dependencies, scripts, version, entry point, and more.

---

## **10. What is package-lock.json?**

It locks the exact dependency versions to ensure consistent installs across systems.

---

## **11. What are DevDependencies?**

Packages used only during development, like testing or bundling tools.

---

## **12. What is Express.js?**

Express.js is a lightweight Node.js framework used to build REST APIs and server-side applications.

---

## **13. What are Middlewares in Express?**

Middleware functions run between the request and response cycle for tasks like logging, validation, error handling, etc.

---

## **14. How do you create a simple server in Node.js?**

```js
const http = require("http");
http.createServer((req, res) => {
  res.end("Hello Node!");
}).listen(3000);
```

---

## **15. What is asynchronous programming?**

A way to execute tasks without blocking other operations using callbacks, promises, or async/await.

---

## **16. What are Promises?**

Promises represent future values and help handle async operations in a cleaner way than callbacks.

---

## **17. What is async/await?**

Syntactic sugar over Promises that makes async code look synchronous.

---

## **18. What is callback hell?**

A messy nested callback structure that makes code unreadable.

---

## **19. How to avoid callback hell?**

Use:

* Promises
* async/await
* Named functions
* Modular code

---

## **20. What is EventEmitter?**

A core module that allows you to create and listen to custom events.

---

## **21. How do you create custom events?**

```js
const EventEmitter = require("events");
const emitter = new EventEmitter();
emitter.on("greet", () => console.log("Hello"));
emitter.emit("greet");
```

---

## **22. What is the fs module?**

The `fs` (File System) module handles file operations like read, write, update, and delete.

---

## **23. Difference between readFile and readFileSync?**

* readFile — async, non-blocking
* readFileSync — sync, blocks the thread

---

## **24. What is the http module?**

A built-in Node module used to create web servers.

---

## **25. What is clustering?**

Clustering allows Node.js to use multiple CPU cores by creating worker processes that share the same server port.

---

## **26. What is load balancing?**

Distributing incoming network traffic across multiple servers or processes.

---

## **27. What is process.nextTick()?**

A microtask that executes before the next event loop iteration.

---

## **28. What are microtasks?**

Tiny tasks queued for immediate execution (Promises, nextTick).

---

## **29. What is buffer in Node.js?**

A temporary memory storage used to handle binary data like files, streams, or network packets.

---

## **30. What is a Stream?**

Streams are data-handling methods that let you process chunks of data piece-by-piece.

---

## **31. Types of streams?**

* Readable
* Writable
* Duplex
* Transform

---

## **32. What is pipe() in streams?**

Used to pass output from one stream to another.

---

## **33. What is CORS?**

A browser security feature that restricts cross-origin requests.

---

## **34. How to enable CORS in Express?**

```js
const cors = require("cors");
app.use(cors());
```

---

## **35. What is Middleware Chaining?**

Multiple middleware execute sequentially until the response is sent.

---

## **36. What is Helmet?**

Helmet adds HTTP security headers to protect Express apps.

---

## **37. What is Rate Limiting?**

A method to limit the number of requests from a client to avoid DDoS attacks.

---

## **38. What is JWT?**

JSON Web Tokens are used for secure authentication between client and server.

---

## **39. How does JWT work?**

Client gets a signed token → attaches it to headers → server verifies → grants access.

---

## **40. What is dotenv?**

A library to load environment variables from a `.env` file.

---

## **41. What is nodemon?**

A dev tool that automatically restarts your Node.js server on file changes.

---

## **42. What is PM2?**

A production process manager for Node.js to keep applications alive, load balanced, and monitored.

---

## **43. What is REST API?**

REST is an architectural style using HTTP methods to create scalable APIs.

---

## **44. What is gRPC?**

A high-performance RPC framework using Protocol Buffers instead of JSON.

---

## **45. What is Socket.io?**

A library used for real-time communication (chat apps, live updates).

---

## **46. What are cookies?**

Small data pieces stored in the browser for sessions or preferences.

---

## **47. What is session?**

A server-side stored user state.

---

## **48. Difference between session and JWT?**

| Session                 | JWT                |
| ----------------------- | ------------------ |
| Stored server-side      | Stored client-side |
| Heavy for scaling       | Lightweight        |
| Works well for web apps | Great for APIs     |

---

## **49. What is bcrypt?**

A hashing library used to safely store passwords.

---

## **50. What is MongoDB?**

A NoSQL database often used with Node.js for flexible, JSON-like data storage.

---

## **51. What is Mongoose?**

An ODM library that simplifies CRUD operations in MongoDB.

---

## **52. What is SQL vs NoSQL?**

SQL uses tables; NoSQL uses documents, key-value, or graphs.

---

## **53. What is the difference between PUT and PATCH?**

* PUT → replace entire record
* PATCH → update specific fields

---

## **54. What is error handling middleware?**

```js
app.use((err, req, res, next) => {
  res.status(500).send(err.message);
});
```

---

## **55. What is HMR (Hot Module Replacement)?**

Automatically reloads modules without restarting the server during development.

---

## **56. What is the crypto module?**

Node's built-in module for hashing, encryption, and secure random generation.

---

## **57. What is child_process?**

Allows executing external applications or shell commands from Node.

---

## **58. What is util.promisify()?**

Converts callback-based functions into Promises.

---

## **59. What is cluster.fork()?**

Creates new worker processes.

---

## **60. What is OS module used for?**

Provides system information like CPU, RAM, OS type.

---

## **61. What is a throttle function?**

Prevents a function from running too frequently.

---

## **62. What is debounce?**

Delays function execution until the last event fires.

---

## **63. What is Caching?**

Storing data temporarily to reduce load and increase speed.

---

## **64. How to use Redis with Node?**

Redis is used as an in-memory data store for caching sessions or frequently-used data.

---

## **65. What is process.env?**

Environment variables accessible inside Node.

---

## **66. What is middleware ordering?**

The sequence middleware is defined matters; earlier ones run first.

---

## **67. What is an API gateway?**

A centralized entry point for all microservices.

---

## **68. What are microservices?**

A system architecture where each feature is a separate small service.

---

## **69. What is monolithic architecture?**

A single, large application with tightly-coupled modules.

---

## **70. What is rate limiter-flex?**

A popular library for rate-limiting in Express.

---

## **71. What is CSRF?**

Cross-Site Request Forgery — an attack tricking users into unwanted actions.

---

## **72. How to prevent CSRF?**

Use CSRF tokens, SameSite cookies, and proper validation.

---

## **73. What is XSS?**

Cross-Site Scripting — injecting JS into web pages.

---

## **74. How to prevent XSS?**

Input sanitization and using Helmet.

---

## **75. What is path module?**

Helps work with file and directory paths.

---

## **76. What is OS module?**

Provides operating system-level information.

---

## **77. What is a deadlock?**

A state where two tasks wait for each other forever.

---

## **78. Does Node.js support multithreading?**

Yes, through Worker Threads (introduced in Node 10.5).

---

## **79. What is Worker Threads?**

Used for CPU-intensive tasks like crypto or image processing.

---

## **80. What is the difference between forEach and for...of?**

forEach cannot use async/await properly; for...of can.

---

## **81. What is try-catch used for?**

Catching exceptions and preventing app crashes.

---

## **82. What is process.kill()?**

Terminates a process programmatically.

---

## **83. What is global object in Node.js?**

Equivalent to `window` in browsers, but called `global`.

---

## **84. What is REPL?**

Read-Eval-Print-Loop: Node’s interactive shell.

---

## **85. What is a memory leak?**

Unused memory not released, causing increased RAM usage.

---

## **86. How to fix memory leaks?**

Use profiling tools, avoid global variables, and manage listeners properly.

---

## **87. What is ESM Support in Node?**

Node supports native ES modules using `"type": "module"` in package.json.

---

## **88. What is MIME type?**

Identifies the type of content being served (e.g., text/html).

---

## **89. What is compression middleware?**

Compresses responses to reduce bandwidth usage.

---

## **90. What is graceful shutdown?**

Closing server connections safely before stopping the server.

---

## **91. What is Winston?**

A popular logging library for Node.js.

---

## **92. What is Morgan?**

HTTP request logger middleware.

---

## **93. What is API versioning?**

Keeping multiple API versions active using routes like `/v1`, `/v2`.

---

## **94. What is a 404 middleware?**

Handles unmatched routes.

---

## **95. What is SSR?**

Server-Side Rendering — rendering pages on the server.

---

## **96. What is content negotiation?**

Server determines the best content format based on client headers.

---

## **97. What is ETag?**

A caching header that helps the client validate resources.

---

## **98. What is Clustered Caching?**

Using cache across multiple processes or servers.

---

## **99. What is a build tool in Node?**

Tools like Webpack, Babel, or ESBuild to bundle and optimize code.

---

## **100. Why choose Node.js?**

* Fast
* Scalable
* Huge ecosystem
* Perfect for real-time apps
* Uses JavaScript end-to-end

---