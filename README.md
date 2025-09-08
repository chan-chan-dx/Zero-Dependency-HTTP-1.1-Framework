# Zero-Dependency HTTP/1.1 Framework

Custom zero-dependency HTTP/1.1 framework built in Python — high-performance routing, observability, and security.

---

> ⚠️ **Note to the Career Experience Recuriter on Source Code**  
> Due to **Business Conduct policies**, I cannot share this code publicly.  
> However, I can provide **private access** to the Git log with timestamps and the codebase upon request during recruitment processes.  
---

🛠️ **Stack:** Pure Python  

## 📋 Overview
I designed and built a custom Python HTTP/1.1 framework from scratch, without relying on ASGI or httptools.  
The framework emphasises **developer experience (DX)**, **performance**, and **observability**.

## 👀 Highlights
- Custom request parser and modular routing/middleware architecture  
- Handler concurrency via threads or processes  
- **Performance:** 0.074 ms execution in business logic vs Django (142 ms), Falcon (110 ms), Uvicorn (4 ms)  
- First-class observability: JSON logs, trace IDs, latency metrics, slow-request tracing  
- Security baked-in: CORS, CSRF with HttpOnly cookies, secret redaction, request schema validation  
- Redis caching middleware with helper functions

## 📊 Performance Benchmarks

Benchmarked against popular Python frameworks on a simple **Hello World** endpoint.  
Latency measured at the **business-logic + middleware execution layer** via built-in observability middleware.  

| Framework               | Avg Latency        | Weekly Downloads | Relative Performance    |
|-------------------------|--------------------|------------------|-------------------------|
| 🚀 **Custom Framework** | **~0.000074s (0.074ms)** | N/A (custom)     | ✅ Baseline (fastest)   |
| Uvicorn (ASGI server)   | ~0.004s (4ms)      | 20M+             | ~54× slower             |
| Falcon                  | ~0.11s (110ms)     | 60K+             | ~1600× slower           |
| Django                  | ~0.142s (142ms)    | 6M+              | ~1900× slower           |

⚠️ **Note:**  
- Results reflect *business handler + middleware execution time*, not full end-to-end socket latency.  
- Django was benchmarked with **development features disabled** and with **some default middleware stack disabled** to simulate production mode more fairly.  
- These results highlight the trade-off between **minimal abstractions** and **batteries-included frameworks**.  

⚡ **Result:** The custom framework consistently delivered **sub-millisecond latency (74µs)** — up to **1900× faster than Django** and **54× faster than Uvicorn** in Hello World benchmarks.  

## Status
- Pending Business Conduct approval for release  

---

