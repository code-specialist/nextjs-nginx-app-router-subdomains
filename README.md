# NextJS App Router Directories as Subdomains

This repository show cases how to use NGINX with NextJS to route directories as subdomains. This is additional material for the article [Subdomain Routing using directories in NextJS App Router (NGINX)](https://code-specialist.com/good-to-know/nextjs-approuter-subdomain).

## Hosts file

You will need to add the following entries to your hosts file:

```
127.0.0.1 admin.code-specialist.local
127.0.0.1 code-specialist.local
127.0.0.1 blog.code-specialist.com
```

## Pre-requisites

- Docker
- Docker Compose
- NodeJS
- NPM

## How to run

### Reverse Proxy

1. Go to the nginx directory e.g. `cd nginx`
2. Run `docker-compose up` in a terminal to start the reverse proxy

### NextJS
1. Go to the nextjs directory e.g. `cd nextjs`
2. Install the dependencies `npm install`
3. Run `npm run dev` in a terminal to start the NextJS app
4. Visit `http://code-specialist.local` / `http://admin.code-specialist.local` / `http://blog.code-specialist.local` in your browser
