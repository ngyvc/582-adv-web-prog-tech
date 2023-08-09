# Node

## Top Tips

- Soon

## Essential links

- [Nodejs](https://nodejs.org/en/)
- [Guides](https://nodejs.org/en/docs/guides)
- [Getting Started](https://nodejs.org/en/docs/guides/getting-started-guide)
- [Anatomy of an HTTP Transaction](https://nodejs.org/en/docs/guides/anatomy-of-an-http-transaction)

## Node basics

Create a HTML file named ```index.html```

```js
console.log("Hello World!");
console.warn("Warning!");
console.error("Error!");
console.log(global);
console.log(process);
console.log(__dirname);
console.log(__filename);
```

### Moddules & ES6 syntax

```js
import { readFile } from "fs/promises";

let template = await readFile(
  new URL("./template.html", import.meta.url),
  "utf-8"
);

console.log(template);
```

```js
import { readFile, writeFile } from "fs/promises";

let template = await readFile(
  new URL("./template.html", import.meta.url),
  "utf-8"
);

const data = {
  title: "My new file",
  body: "I wrote this file to disk using node",
};

for (const [key, val] of Object.entries(data)) {
  template = template.replace(`{${key}}`, val);
}

await writeFile(new URL("./index.html", import.meta.url), template);
```

```js
import http from "http";

const host = "localhost";
const port = 8000;

const server = http.createServer((req, res) => {
  if (req.method === "POST") {
    let body = "";

    req.on("data", (chunk) => {
      body += chunk.toString();
    });

    req.on("end", () => {
      if (req.headers["content-type"] === "application/json") {
        body = JSON.parse(body);
      }

      console.log(body);
      res.writeHead(201);
      res.end("ok");
    });
  } else {
    res.writeHead(200);
    res.end("hello from my server");
  }
});

server.listen(port, host, () => {
  console.log(`Server is running on http://${host}:${port}`);
});
```

## CURL

```bash
curl -X POST <https://reqbin.com/echo/post/json> -H 'Content-Type: application/json' -d '{"login":"my_login","password":"my_password"}'
```

or use Thunder Client extension on vscode, just make sure to send request using http://[::]:8000 if localhost doesn't work.

[Thunder Client](https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client)
