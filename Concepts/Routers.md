# Hono Routers

Hono provides five types of routers, each designed for different use cases.

## 1. RegExpRouter
- **Fastest router** in the JavaScript world.
- Creates **one large regular expression** for all routes, allowing single-pass matching.
- **Best for:** High-performance applications with many routes.
- **Limitation:** Does not support all routing patterns.
![Router Diagram](Linear-router.png)
![Router Diagram](RegExp-Router.png)


## 2. TrieRouter
- Uses the **Trie-tree algorithm** instead of loops.
- **Slower than RegExpRouter**, but much faster than Express.
- **Supports all patterns**, unlike RegExpRouter.
- **Best for:** Applications needing flexibility with routing patterns.
![Router Diagram](Trie-Tree.png)

## 3. SmartRouter
- **Automatically selects the best router** (RegExpRouter or TrieRouter) based on routing needs.
- **Default router in Hono.**
- **Best for:** General use when unsure which router to pick.

## 4. LinearRouter
- **Optimized for fast route registration** (ideal for environments where apps reinitialize frequently).
- **Much faster than RegExpRouter** in registering routes.
- **Best for:** Fastly Compute and environments with frequent app restarts.

## 5. PatternRouter
- **Smallest and lightest router** (application size under 15KB).
- Ideal for **resource-limited environments**.
- **Best for:** Ultra-lightweight deployments.

### Performance Benchmark (GET /user/lookup/username/hey)
| Router          | Speed  |
|---------------|---------|
| **LinearRouter**  | **1.82 µs/iter**  |
| MedleyRouter  | 4.44 µs/iter  |
| KoaTreeRouter | 3.81 µs/iter  |
| TrekRouter    | 5.84 µs/iter  |
| FindMyWay     | 60.36 µs/iter |

LinearRouter is **33x faster** than FindMyWay and **2.45x faster** than MedleyRouter!

---
Choose the right router based on your application's needs!

