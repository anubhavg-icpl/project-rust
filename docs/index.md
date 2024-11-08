# Project Rust

## Overview

Project Rust is a template microservice that demonstrates building scalable web services using Rust.

## Features

- REST API with Actix-web
- Health check endpoint
- Echo service
- Structured logging
- Docker support
- Backstage integration

## Quick Links

- [API Documentation](api.md)
- [Development Guide](development.md)
- [Operations Guide](operations.md)

## Getting Started

1. Clone the repository
```bash
git clone https://github.com/anubhavg-icpl/project-rust.git
```

2. Build the project
```bash
cargo build
```

3. Run the service
```bash
cargo run
```

4. Test the endpoints
```bash
# Health check
curl http://localhost:8080/health

# Echo service
curl -X POST -H "Content-Type: application/json" \
     -d '{"content":"Hello"}' \
     http://localhost:8080/echo
```