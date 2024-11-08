# Project Rust Documentation

Welcome to the Project Rust documentation. This service provides a foundation for building scalable microservices in Rust.

## Overview

Project Rust is a template microservice that demonstrates:

- Modern Rust web service development
- Integration with Backstage developer portal
- Best practices for service documentation
- API-first development approach

## Getting Started

1. **Prerequisites**
   - Rust 1.70 or newer
   - Cargo package manager
   - Docker (optional)

2. **Local Development**
   ```bash
   # Clone the repository
   git clone https://github.com/your-org/project-rust.git
   
   # Build the project
   cargo build
   
   # Run tests
   cargo test
   
   # Start the service
   cargo run
   ```

3. **Verify Installation**
   ```bash
   # Check health endpoint
   curl http://localhost:8080/health
   ```

## Architecture

The service follows a clean architecture pattern with:

- REST API layer using actix-web
- Structured logging
- Health checking
- Configuration management
- Error handling

## Documentation Sections

- [API Documentation](api.md) - API endpoints and usage
- [Development Guide](development.md) - Setup and development workflow
- [Operations Guide](operations.md) - Deployment and monitoring