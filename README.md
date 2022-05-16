# Service Level Objectives (SLOs)
A Service Level Objective (SLO) is meant to be a measure for how to make customers happy. A customer can be an actual human being, another service, or another system that your service interacts with. The SLOs for 
your particular service should measure what matters to your service. It can for example be availability, latency, throughput, durability, end-to-end-latency or correctness.

Technically speaking, an SLO is a limit on how many times a Service Level Indicator can fall out of the defined scope. For example, a service might have uptime as one of the indicators as to how well the service is performing. The SLO could then be `during a 4 week rolling window the service should have a minimum 99% uptime`.

Another service might have response time as an indicator, an SLO could then be `99% of requests should resolve within 100 ms and 95% within 50 ms`.

SLO documents should be written using plain business English. A template for SLO documents can be found [here](https://sre.google/workbook/slo-document/). They are then implemented in [PromQL](https://prometheus.io/docs/prometheus/latest/querying/basics/) if Prometheus is used as metrics system.
