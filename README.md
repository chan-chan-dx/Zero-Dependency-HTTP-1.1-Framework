# Zero-Dependency HTTP/1.1 Framework

Custom zero-dependency HTTP/1.1 framework built in Python — high-performance routing, observability, and security.

---

> ⚠️ **Note to the Career Experience Recuriter on Source Code**  
> Due to **Business Conduct policies**, I cannot share this code publicly.  
> However, I can provide **private access** to the Git log with timestamps and the codebase upon request during recruitment processes.  
---

🛠️ **Stack:** Pure Python  

## Overview
I designed and built a custom Python HTTP/1.1 framework from scratch, without relying on ASGI or httptools.  
The framework emphasises **developer experience (DX)**, **performance**, and **observability**.

## Highlights
- Custom request parser and modular routing/middleware architecture  
- Handler concurrency via threads or processes  
- **Performance:** 0.074 ms execution in business logic vs Django (142 ms), Falcon (110 ms), Uvicorn (4 ms)  
- First-class observability: JSON logs, trace IDs, latency metrics, slow-request tracing  
- Security baked-in: CORS, CSRF with HttpOnly cookies, secret redaction, request schema validation  
- Redis caching middleware with helper functions

## Status
- Pending Business Conduct approval for release  

---

