# Project Rust

A Rust-based microservice component that demonstrates basic web service functionality.

## Quick Start

```bash
# Run the service locally
cargo run

# Run tests
cargo test

# Build for release
cargo build --release
```

## Features

- Health check endpoint
- Echo service
- Structured logging
- Configuration via environment variables
- Docker support

## API Endpoints

- `GET /health` - Health check endpoint
- `POST /echo` - Echo service that returns the sent message

## Development

See the [development guide](docs/development.md) for detailed setup instructions.

## Documentation

Full documentation is available in the `docs/` directory:

- [API Documentation](docs/api.md)
- [Development Guide](docs/development.md)
- [Operations Guide](docs/operations.md)

## License

MIT License