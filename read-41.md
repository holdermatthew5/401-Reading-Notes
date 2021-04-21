# Deployment with Vercel

Create a Vercel account
Install vercel (is that app level or computer level?)
Import vercel
`npm run build` builds the next.js app in the `.next` folder.
`npm run start` starts a node.js server that supports staticly generated server-side render pages and API routes.
Making this change (`"start": "next start -p $PORT"`) in the package.json allows you to set a custom port.