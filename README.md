
---

# Project Setup Guide

## Initialize a Worker

1. **Create and initialize your application:**

   ```bash
   npm create cloudflare -- my-app
   ```

2. **When prompted, select `no` for the question:**
   - "Do you want to deploy your application?"

## Explore `package.json` Dependencies

- Notice that `wrangler` is included as a dependency:

  ```json
  "wrangler": "^3.0.0"
  ```

- Note that `express` is not a dependency in the project.

## Start the Worker Locally

To start the worker locally, run:

```bash
npm run dev
```

## Returning JSON in the Worker

To return JSON from your worker, use the following code:

```typescript
export default {
  async fetch(request: Request, env: Env, ctx: ExecutionContext): Promise<Response> {
    return Response.json({
      message: "hi"
    });
  },
};
```
npx wrangler login
npx wrangler whoami
npm run deploy
---

