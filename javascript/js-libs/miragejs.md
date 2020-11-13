# Mirage JS

[Mirage JS Website](https://miragejs.com/)

- Build complete frontend features, even if your API doesn't exist.
- MIrage JS is an API mocking library that lets frontend developers build complete features without touching their backend APIs.

- Mirage JS is an API mocking library that lets you:
  - build
  - test
  - share
  - without having to rely on any backend services.

### [Mirage JS Docs](https://miragejs.com/docs/getting-started/introduction/)

### [Sam Selikoff](https://samselikoff.com/)

### **Mirage JS & Redux Tookit**

**Example REST API and Client**
To keep the example project isolated but realistic, the initial project setup already included a fake in-memory REST API for our data (configured using the Mirage.js mock API tool). The API uses /fakeApi as the base URL for the endpoints, and supports the typical GET/POST/PUT/DELETE HTTP methods for /fakeApi/posts, /fakeApi/users, and fakeApi/notifications. It's defined in src/api/server.js.

The project also includes a small HTTP API client object that exposes client.get() and client.post() methods, similar to popular HTTP libraries like axios. It's defined in src/api/client.js.

We'll use the client object to make HTTP calls to our in-memory fake REST API for this section.

Also, the mock server has been set up to reuse the same random seed each time the page is loaded, so that it will generate the same list of fake users and fake posts. If you want to reset that, delete the 'randomTimestampSeed' value in your browser's Local Storage and reload the page, or you can turn that off by editing src/api/server.js and setting useSeededRNG to false.
