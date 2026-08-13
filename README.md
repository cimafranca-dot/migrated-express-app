# Native Node App - Module 2

A simple To-Do app built using only Node.js `http` module. No Express.

## How to Run
npm install
node server.js
Then open http://localhost:3000

## Reflection Questions

### 1. What was the most "painful" part of building this without a framework?
The most painful was handling requests manually. Because had to write every statements and manually read files with `fs.readFile`, and set headers myself. I got stuck with `ERR_CONNECTION_REFUSED` because I forgot to add `return;` after `res.end()` and the server crashed. I even spent 3 hours because of it, And you cannot just copy and paste everything.

### 2. Why do we need to manually collect "chunks" of data in the POST route?
Because we need to be articulate it terms of manually collevting a data, it might cause a lots of error if we are not doing it proper;y.

### 3. What HTTP status code did we return when a task was successfully created, and why?
We returned `201 Created`. `200 OK` is for general success, but `201` is more specific and correct for POST when a new resource is created on the server.

### 4. If you had to add a DELETE route, what would the code look like?
```javascript
if (req.url.startsWith('/api/tasks/') && req.method === 'DELETE') {
  const id = parseInt(req.url.split('/')[3]);
  tasks.splice(id, 1);
  res.writeHead(200, { 'Content-Type': 'application/json' });
  res.end(JSON.stringify({ message: 'Deleted' }));
  return;
}