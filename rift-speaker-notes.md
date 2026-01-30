# Rift Presentation - Speaker Notes

## Slide 1: Title Slide
**Duration: ~1 min**

"Good morning/afternoon everyone. I'm here today to talk about something that impacts all of us who work with integration testing - mock server performance.

We've invested heavily in test automation. We have mature service virtualization with Mimeo and Mountebank. The configurations work well, the patterns are established.

But there's a bottleneck we've been living with: mock server overhead. Every request to Mountebank takes time - time that adds up across thousands of tests.

Today I want to show you Rift - a tool that can make our integration tests run 20 to 250 times faster, using our existing mock configurations unchanged."

---

## Slide 2: Why We're Here
**Duration: ~1 min**

"Let's start with why we're here.

We rely heavily on service virtualization. Mimeo and Mountebank let us test our services against mock APIs without spinning up real dependencies.

The problem is: mock server performance directly impacts how fast our CI/CD pipelines run. When every request to a mock server takes milliseconds, those milliseconds add up across thousands of tests.

Today's goal is simple: show you a tool that makes your integration tests 20 to 250 times faster, using your existing mock configurations unchanged. No rewrites, no migrations - just faster."

---

## Slide 3: The Integration Testing Bottleneck
**Duration: ~1 min**

"Let's talk about the integration testing bottleneck.

We all know unit tests are fast - milliseconds per test. E2E tests are slow by nature - they're testing real systems.

But integration tests should be fast. They're testing your code against controlled mock responses. So why do they often take seconds per request?

The answer is mock server overhead. Every time your test makes a request to a mock server, that server has to:
1. Receive the request
2. Match it against predicates (sometimes dozens of them)
3. Execute any behaviors like JSON transformations
4. Generate and send the response

When your mock server is written in Node.js, this overhead adds up. Multiply it by thousands of tests, and you're looking at significant CI/CD time.

This is exactly what Rift solves."

---

## Slide 4: Introducing Rift
**Duration: ~1 min**

"This is Rift. It's a high-performance mock server written in Rust that's 100% compatible with Mountebank's API.

Let me emphasize what that means: you can take your existing Mimeo imposter configurations - the exact same JSON files - and run them on Rift without changing a single line.

Rift achieves this through:
- Native Rust performance instead of JavaScript interpretation
- Async I/O with Tokio for handling thousands of concurrent connections
- Optimized predicate matching algorithms
- Zero garbage collection pauses

It ships as a single 20MB binary that uses about 50MB of RAM - compared to Mountebank's 200MB+ footprint with the Node.js runtime."

---

## Slide 5: Performance: The Numbers
**Duration: ~2 min**

"Let's look at real benchmark numbers. These were run on equivalent hardware - 2 CPUs, 1GB RAM for each service.

[PAUSE - let audience read table]

For simple health checks, Rift is 20 times faster. That's significant, but it's just the beginning.

Where Rift really shines is complex predicate matching:
- JSONPath predicates are **247 times faster**. That's not a typo.
- XPath predicates are **170 times faster**.
- Complex AND/OR combinations are **32 times faster**.

The 'Last Stub Match' row is particularly interesting. When you have 50 stubs and the matching one is last, Mountebank has to check all 50. At 291 requests per second, that overhead adds up. Rift handles the same scenario at 22,000 RPS.

**What does this mean in practice?** If your integration test suite currently takes 10 minutes, it could potentially run in 30 seconds to 2 minutes with Rift."

---

## Slide 6: Why the Massive Improvement
**Duration: ~1 min**

"Why is Rift so much faster? It comes down to the fundamental difference between interpreted and native code.

Mountebank runs on Node.js - V8 JavaScript engine with garbage collection, JIT warmup, and single-threaded execution.

Rift is compiled Rust code running directly on the CPU with:
- No garbage collector - memory is managed at compile time
- No warmup needed - starts at full speed immediately
- Async I/O - efficiently uses all CPU cores
- SIMD-optimized JSON parsing that's 10x faster

For JSONPath specifically, Mountebank uses a JavaScript library. Rift uses a Rust implementation compiled to native code. That's why JSONPath is 247 times faster."

---

## Slide 7: Zero-Friction Migration
**Duration: ~1 min**

"The migration to Rift is designed to be zero-friction.

Step one: Replace the Docker image. One line change.

Step two: Point to your existing configuration files. Same command-line flags.

Step three: Run your tests. They work exactly as before, just faster.

This isn't theoretical - I've tested it with our Solo configurations. 35 imposter files with 674 stubs total loaded and ran correctly on Rift with no modifications."

---

## Slide 8: API Compatibility
**Duration: ~1 min**

"Let me be specific about compatibility. Rift implements every predicate type that Mountebank supports.

All the string operators: equals, deepEquals, contains, startsWith, endsWith, matches.

Advanced query languages: JSONPath and XPath.

Logical operators: and, or, not.

All response types and behaviors.

Rift has 126 compatibility test scenarios that verify byte-for-byte identical responses."

---

## Slide 9: Solo-Test Migration Results
**Duration: ~1 min**

"I ran our Solo test configurations through Rift. Here are the results.

35 imposter files covering multiple services: Euphoria for appointments, Tadashi for sales and pricing, Seiko for staff management, Aqua for call tracking, Yoji for dealer services, and more.

These files contain 674 stubs - that's 674 different request/response mappings. They use 1,923 predicates - multiple predicates per stub for precise matching. And 593 of them have JavaScript wait behaviors for latency simulation.

All of them loaded and ran correctly on Rift.

This is real validation that Rift can handle the complexity of production service virtualization configurations."

---

## Slide 10: Rift-Exclusive: Fault Injection
**Duration: ~1 min**

"Now let's talk about what Rift can do that Mountebank can't.

Rift has built-in fault injection for chaos engineering. In Mountebank, if you want probabilistic failures, you have to write JavaScript inject functions.

With Rift, you add a _rift extension. This example adds:
- 30% probability of latency
- 10% probability of 503 errors

Declarative, no JavaScript to debug. And the _rift namespace means your configs remain Mountebank-compatible."

---

## Slide 11: Rift-Exclusive: Observability
**Duration: ~30 sec**

"Rift has built-in Prometheus metrics. Request counts, latency histograms, fault injection counters. Scrape with Prometheus, visualize with Grafana."

---

## Slide 12: Getting Started
**Duration: ~1 min**

"Getting started with Rift is straightforward.

Pull the Docker image, point it at your existing imposter configs, and run your tests. That's it.

If you want to try it for your team:
1. Take your existing Mimeo or Solo configurations
2. Run them on Rift locally
3. Measure the difference in response times
4. If it works well, try it in your CI pipeline

The migration is low-risk because your configs don't change. If something doesn't work, you can switch back to Mountebank instantly."

---

## Slide 13: Summary: Why Rift
**Duration: ~1 min**

"Let me summarize why Rift matters.

You get dramatically faster CI pipelines - 20 to 250 times faster mock responses.

You pay zero migration cost. Your existing configs work unchanged.

Developers spend less time waiting. You get new capabilities like fault injection and metrics.

Bottom line: same configs, same API, dramatically faster."

---

## Slide 14: Resources
**Duration: ~30 sec**

"Here are the resources to get started.

The Rift GitHub repository has full documentation, examples, and compatibility information. The Docker image is publicly available - you can try it today.

If you want to try Rift for your team, start with your existing imposter configs. If something doesn't work, file a GitHub issue."

---

## Slide 15: Q&A
**Duration: Open**

"Any questions?"

### Anticipated Questions:

**Q: "What if we find a compatibility issue?"**
A: "File a GitHub issue - the project is actively maintained. We can also work around most issues with config changes."

**Q: "Can we use both Rift and Mountebank?"**
A: "Yes, they can run in the same environment. Different imposters on different ports."

**Q: "What's the learning curve?"**
A: "Zero for basic use - same API. New features like fault injection have good documentation."

**Q: "Is this production-ready?"**
A: "It's at version 0.1.0 (beta), but passing 126 compatibility tests and handling 35+ imposter configs suggests stability."

**Q: "Who maintains Rift?"**
A: "Open source project on GitHub. Active development, responsive to issues."

---

## Presentation Timing

| Slide | Topic | Duration |
|-------|-------|----------|
| 1 | Title | 1 min |
| 2 | Why We're Here | 1 min |
| 3 | Bottleneck | 1 min |
| 4 | Introducing Rift | 1 min |
| 5 | Performance Numbers | 2 min |
| 6 | Why So Fast | 1 min |
| 7 | Migration | 1 min |
| 8 | API Compatibility | 1 min |
| 9 | Solo Results | 1 min |
| 10 | Fault Injection | 1 min |
| 11 | Observability | 30 sec |
| 12 | Getting Started | 1 min |
| 13 | Summary | 1 min |
| 14 | Resources | 30 sec |
| 15 | Q&A | Open |

**Total: ~15 minutes + Q&A**
