# Instana OpenTelemetry Go Contrib

> [!IMPORTANT]
> This project is currently in **beta** status and is susceptible to breaking changes. APIs, features, and functionality may change without notice. Use in production environments at your own risk.

## Overview

Instana OpenTelemetry Go Contrib is based on Open Source [OpenTelemetry Go Contrib](https://github.com/open-telemetry/opentelemetry-go-contrib). It provides a collection of 3rd-party packages for OpenTelemetry-Go which focuses on supporting Instana OpenTelemetry and IBM platforms (S390X Linux, PowerPC Linux, AIX) as well as other platforms (Linux x64/ARM64, macOS, and Windows).

This repository contains instrumentation libraries, propagators, detectors, exporters, samplers, bridges, and processors that extend the core OpenTelemetry-Go functionality.

## Contents

- [Examples](./examples/): Examples of OpenTelemetry libraries usage.
- [Instrumentation](./instrumentation/): Packages providing OpenTelemetry instrumentation for 3rd-party libraries.
- [Propagators](./propagators/): Packages providing OpenTelemetry context propagators for 3rd-party propagation formats.
- [Detectors](./detectors/): Packages providing OpenTelemetry resource detectors for 3rd-party cloud computing environments.
- [Exporters](./exporters/): Packages providing OpenTelemetry exporters for 3rd-party export formats.
- [Samplers](./samplers/): Packages providing additional implementations of OpenTelemetry samplers.
- [Bridges](./bridges/): Packages providing adapters for 3rd-party instrumentation frameworks.
- [Processors](./processors/): Packages providing additional implementations of OpenTelemetry processors.

## Project Status

This project contains both stable and unstable modules. Refer to the module for its version or our [versioning manifest](./versions.yaml).

Project versioning information and stability guarantees can be found in the [versioning documentation](VERSIONING.md).

### Compatibility

OpenTelemetry-Go Contrib ensures compatibility with the current supported versions of the [Go language](https://golang.org/doc/devel/release#policy):

> Each major Go release is supported until there are two newer major releases.
> For example, Go 1.5 was supported until the Go 1.7 release, and Go 1.6 was supported until the Go 1.8 release.

## Getting Started

### Download and Build

The Instana OpenTelemetry Go Contrib is available in source as `tar.gz` or `zip` file which can be downloaded from releases.

Before building from source, make sure the following tools are installed:
- Go 1.25 or above
- Standard build tools for your platform (gcc/g++ on Linux/AIX, Xcode Command Line Tools on macOS, Visual Studio Build Tools on Windows)

To build everything, run:
```bash
make
```

### Using the Library

To use Instana OpenTelemetry Go Contrib in your project, add a replace directive in your `go.mod` file to point to the local path or repository:

```go
replace go.opentelemetry.io/contrib => /path/to/instana-opentelemetry-go-contrib
```

Then import the packages in your Go code as usual:
```go
import (
    "go.opentelemetry.io/contrib/instrumentation/net/http/otelhttp"
    "go.opentelemetry.io/contrib/propagators/b3"
)
```

## Contributing

For information on how to contribute, consult [the contributing guidelines](./CONTRIBUTING.md)