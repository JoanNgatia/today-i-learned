## Observability metrics

> Observability - Aggregation of metrics, logs and traces to measure the performance of an application, and pre-emptively monitor for failures.

### Logging

- Taking notes of things happening in a system.
- Logging consists of multiple steps:
  1. Collecting and ingesting the logs - if the system is distributed, find a way to send all the logs to a central place.
  2. Processing ingested logs.
  3. Indexing the logs, which involves segmenting tue logs into groups and generating metrics and dashboards.

### Tracing

- Chanelling a single user's or request's journey through a system.
- Getting start and end points of each request in an application.
- Provides better visibility in understanding the exact points when things failed / happened in a program, and what actions were taken around the failure event.

### Profiling

- Capturing a system's health over time.
- Profiles range from Low-level metrics on infrastructure such as CPU usage or file I/O to higher-lvel metrucs like throughput or latency.
- These metrics provide visibility on what to improve in the applications.

#### Additional Reading
- [greeeg post](https://greeeg.com/differences-between-logging-tracing-profiling)
- [Netflix's lessons on observability](https://netflixtechblog.com/lessons-from-building-observability-tools-at-netflix-7cfafed6ab17)
- [Monitoring the SRE Golden Signals](https://www.slideshare.net/OpsStack/how-to-monitoring-the-sre-golden-signals-ebook/)
