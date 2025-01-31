# Philosophy of Hono

## Why Hono Was Created
I wanted to build a web app on **Cloudflare Workers**, but there was no good framework for it. So, I decided to create **Hono**.

At first, I was just learning how to build a router using **Trie trees**. Then, a friend introduced an ultra-fast router called **RegExpRouter**. Another friend built **Basic Authentication middleware**.

Since Hono uses **Web Standard APIs**, it works not just on Cloudflare Workers but also on **Deno and Bun**. When people asked, *"Is there Express for Bun?"*—we could say, *"No, but there is Hono!"* (Though Express now works on Bun.)

Over time, more developers joined in, adding **GraphQL support, Firebase authentication, Sentry middleware**, and even a **Node.js adapter**.

## Why Hono?
- ⚡ **Super fast**
- 🌍 **Works everywhere** (Cloudflare, Deno, Bun, Node.js)
- 🛠 **Easy to extend** (growing ecosystem)

Hono is built on **Web Standards**, and maybe one day, it will become the **standard** for web frameworks!

