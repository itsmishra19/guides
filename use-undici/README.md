Discover why you should prefer Undici for making HTTP requests in Node.js over axios or node-fetch.

# Why Undici

Undici is a powerful and efficient library for making HTTP requests in Node.js, offering significant advantages over popular alternatives like node-fetch and axios. Here are a few reasons why people should consider using undici:

1. Performance: Undici is designed to provide outstanding performance. It achieves this by utilizing Node.js's `http2` module and implementing a highly optimized HTTP/1.1 and HTTP/2 client. As a result, undici can handle a large number of concurrent requests with minimal resource usage, making it an excellent choice for high-performance applications.

2. Low Memory Footprint: Compared to other HTTP clients, undici has a significantly lower memory footprint. It achieves this by using a stream-based approach that avoids buffering entire responses in memory. This makes undici ideal for handling large payloads or streaming responses, as it efficiently processes data in a memory-friendly manner.

3. Minimal Dependencies: Undici has minimal external dependencies, reducing the risk of security vulnerabilities and making it easier to maintain and upgrade. By keeping the codebase lean, undici ensures a smaller attack surface and better long-term compatibility.

4. Fully Featured: Despite its lightweight nature, undici provides comprehensive support for HTTP features, including request and response headers, streaming requests and responses, automatic handling of redirects, and support for custom SSL/TLS certificates. It offers a clean and intuitive API that allows developers to interact with HTTP services with ease.

5. Well-Maintained: Undici is actively maintained by a dedicated team, ensuring that it stays up-to-date with the latest HTTP standards and security protocols. Regular updates and bug fixes make undici a reliable choice for developers who want a stable and robust HTTP client.

Overall, if you're looking for a high-performance, memory-efficient, and feature-rich HTTP client for your Node.js applications, undici is a fantastic option. Its performance optimizations and streamlined design make it a superior choice over node-fetch and axios in terms of speed, resource usage, and flexibility.

## Installation

Firstly, we need to install `undici` to our project, you can run the following command:
```bash
npm install undici
    or
yard add undici
```


## Importing Undici

After we have successfully installed `undici` to our project, we need to import fetch from undici:
```js
//If you use commonJS
const { fetch } = require("undici");

//If you use ESM
import { fetch } from "undici";
```

# Making GET request

```js
   fetch("https://thronesapi.com/api/v2/Characters", {
        method: "GET"
    })
      .then(x => console.log(await x.json()))
      .catch(e => console.error(e));
```

# Making POST request with custom headers

```js
   fetch("https://some.api.to/query", {
        method: "GET",
        headers: {
            authorization: "Bearer sometoken"
        }
    })
      .then(x => console.log(await x.json()))
      .catch(e => console.error(e));
```

# Issues

If you are facing any issues with Undici you can read their [official documentation](https://undici.nodejs.org/#/) or checkout the [github repository](https://github.com/nodejs/undici) for bugs or any issues 