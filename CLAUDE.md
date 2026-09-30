# unify-lab — rules for Claude sessions

Owner-approved (Ofir, 2026-09-30): this repo is a sandboxed test bench.
Inside `subjects/*` Claude may install and run the subject app's own code:
`npm install`, `npm ci`, `npm run build|dev|preview`, `npx vite` (incl. a
backgrounded dev/preview server bound to localhost / 127.0.0.1).

- Always `cd subjects/<NN-name>` first, then run the exact command.
- Installs come from the public npm registry per the subject's package.json. Nothing else.
- Servers bind to localhost only. Never expose them, never deploy.
- Never run these outside `subjects/`, and never pipe remote scripts into a shell.
