# IOAM Collector

The IOAM Collector is used inside the [Cross-Layer Telemetry](https://github.com/Advanced-Observability/cross-layer-telemetry) (CLT) project.

Its role is to enhance OpenTelemetry traces and spans for a [OpenTelemetry Collector](https://opentelemetry.io/docs/collector) compatible backend with IOAM data.

## Building

```bash
git clone https://github.com/Advanced-Observability/ioam-collector
cd ioam-collector
go build
```

## Running

1. Set the environment variable `OTEL_EXPORTER_OTLP_ENDPOINT` to the endpoint URL of your OpenTelemetry Collector.
The list of compatible environment variables can be found [here](https://pkg.go.dev/go.opentelemetry.io/otel/exporters/otlp/otlptrace/otlptracegrpc#section-readme).
2. Run the executable

By default, it listens on port **7123**, configurable with the `-p` flag.

```bash
OTEL_EXPORTER_OTLP_ENDPOINT="https://localhost:443" ./ioam-collector -p 7124
```
