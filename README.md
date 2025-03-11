# NextJS App Router Directories as Subdomains

This repository demonstrates the integration of NGINX with Next.js to facilitate the routing of directories as subdomains.
It serves as supplementary material for the article [Subdomain Routing using directories in Next.js App Router (NGINX).](https://code-specialist.com/good-to-know/nextjs-approuter-subdomain)

## Objective and Anticipated Outcome

The primary goal is to showcase how specific app directories can be served as subdomains using NGINX with Next.js. Consider the following desired outcome:

```
.
└── app/
    ├── blog/
    │   ├── page.tsx
    ├── home/
    │   ├── page.tsx
    └── admin/
    │   ├── page.tsx
    └── layout.tsx
```

- `/blog` on `blog.code-specialist.local`
- `/home` on `code-specialist.local`
- `/admin` on `admin.code-specialist.local`

## Hosts file

Ensure that the following entries are added to your hosts file:

```
127.0.0.1 admin.code-specialist.local
127.0.0.1 code-specialist.local
127.0.0.1 blog.code-specialist.local
```

The hosts file is located at `/etc/hosts` for MacOS and Linux-based systems and `C:\Windows\System32\drivers\etc\hosts` for Windows.

## Pre-requisites

- Docker
- Docker Compose
- NodeJS
- NPM

## How to use

### Set Up Reverse Proxy

1. Navigate to the nginx directory, e.g., cd nginx.
2. In a terminal, execute `docker-compose up` to launch the reverse proxy.

### Run Next.js Application

1. Move to the nextjs directory, e.g., cd nextjs.
2. Install the necessary dependencies using npm install.
3. Start the Next.js app by running npm run dev in a terminal.
4. Visit the following URLs in your browser:
   - http://code-specialist.local
   - http://admin.code-specialist.local
   - http://blog.code-specialist.local

By following these steps, you'll successfully implement subdomain routing for specific app directories using NGINX and Next.js. For a detailed walkthrough, refer to the linked article
