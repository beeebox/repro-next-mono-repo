# Tracespan Issue

To reproduce

`cd packages/server && yarn`
`cd packages/client && yarn`

`yarn dev` in client package

Try to load http://localhost:3000

Observe this error in the console

```
- event compiled client and server successfully in 148 ms (168 modules)
- wait compiling / (client and server)...
- event compiled client and server successfully in 73 ms (191 modules)
TypeError: trace.getSpan is not a function
    at NextTracerImpl.getActiveScopeSpan (/Users/jamesfox/next-reproduction-app/node_modules/next/dist/server/lib/trace/tracer.js:71:22)
    at NextTracerImpl.trace (/Users/jamesfox/next-reproduction-app/node_modules/next/dist/server/lib/trace/tracer.js:90:103)
    at DevServer.handleRequest (/Users/jamesfox/next-reproduction-app/node_modules/next/dist/server/base-server.js:243:41)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async DevServer.handleRequest (/Users/jamesfox/next-reproduction-app/node_modules/next/dist/server/dev/next-dev-server.js:892:16)
```
