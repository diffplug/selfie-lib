# selfie-lib: snapshot testing for Python and JVM

> **Moved:** this library now lives at `diffplug/selfie-lib`, with docs at [lib.selfie.dev](https://lib.selfie.dev). Maven and PyPI coordinates and the API are unchanged, so you don't need to change anything. [Read the announcement](https://github.com/diffplug/selfie-lib/issues/595).

![gif demo of selfie in action](https://docs.diffplug.com/selfie/selfie-demo.gif)

## Key features

- Just add a test dependency ([py](https://lib.selfie.dev/py/get-started#installation), [jvm](https://lib.selfie.dev/jvm/get-started#installation)), zero setup, zero config.
- Snapshots can be [inline literals](https://lib.selfie.dev/py#literal) or [on disk](https://lib.selfie.dev/py#like-a-filesystem).
- Use `expect_selfie` for testing or `cache_selfie` for [memoizing expensive API calls](https://lib.selfie.dev/py/cache).
- Disk snapshots are automatically [garbage collected](https://github.com/diffplug/selfie-lib/blob/main/jvm/selfie-runner-junit5/src/main/kotlin/com/diffplug/selfie/junit5/SelfieGC.kt) when the test class or test method is removed.
- Snapshots are **just strings**. Use html, json, markdown, whatever. No [magic serializers](https://lib.selfie.dev/py/cache#roundtripping-typed-data).
- Record **multiple facets** of the entity under test, e.g. for a web request...
  - store the HTML as one facet
  - store HTML-rendered-to-markdown as another facet
  - store cookies in another facet
  - **assert some facets on disk, others inline**
  - see gif above for live demo, detailed example [here](https://lib.selfie.dev/py/facets#harmonizing-disk-and-inline-literals)

Python and JVM ports are both production-ready.

## Documentation

- Quickstart **([py](https://lib.selfie.dev/py/get-started#quickstart), [jvm](https://lib.selfie.dev/jvm/get-started#quickstart))**
- Facets **([py](https://lib.selfie.dev/py/facets), [jvm](https://lib.selfie.dev/jvm/facets))**
- Caching / memoizing **([py](https://lib.selfie.dev/py/cache), [jvm](https://lib.selfie.dev/jvm/cache))**
- Why selfie **([py](https://lib.selfie.dev/py), [jvm](https://lib.selfie.dev/jvm))**
- API reference **([py](https://pydoc.selfie.dev/namespacemembers_func), [jvm](https://kdoc.selfie.dev/))**

## Contributing

PRs welcome! Horror stories and glory stories too, share your experience! See [`CONTRIBUTING.md`](CONTRIBUTING.md).


## Acknowledgements

Heavily inspired by [origin-energy's java-snapshot-testing](https://github.com/origin-energy/java-snapshot-testing), which in turn is heavily inspired by [Facebook's jest-snapshot](https://jestjs.io/docs/snapshot-testing).
