# Installation Guide

## Prerequisites

- Rust 1.70 or newer
- Cargo package manager
- Git

## Setup Steps

1. Clone the Repository
   ```bash
   git clone https://github.com/anubhavg-icpl/project-rust.git
   cd project-rust
   ```

2. Build the Project
   ```bash
   cargo build
   ```

3. Run Tests
   ```bash
   cargo test
   ```

4. Start the Service
   ```bash
   cargo run
   ```

## Docker Installation

If you prefer using Docker:

```bash
# Build the image
docker build -t project-rust .

# Run the container
docker run -p 8080:8080 project-rust
```

## Verification

To verify your installation:

```bash
# Check health endpoint
curl http://localhost:8080/health

# Expected output:
{
  "status": "healthy",
  "version": "0.1.0"
}