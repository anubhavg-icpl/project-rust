
# Development Guide

## Setup Development Environment

1. **Install Rust**
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

2. **Install Development Tools**
   ```bash
   rustup component add clippy rustfmt
   cargo install cargo-watch cargo-audit
   ```

3. **Clone Repository**
   ```bash
   git clone https://github.com/your-org/project-rust.git
   cd project-rust
   ```

## Development Workflow

### Local Development

1. **Run in Development Mode**
   ```bash
   cargo watch -x run
   ```

2. **Run Tests**
   ```bash
   cargo test
   cargo test -- --nocapture  # With output
   ```

3. **Check Code Style**
   ```bash
   cargo fmt -- --check
   cargo clippy
   ```

### Best Practices

1. **Code Style**
   - Follow Rust standard formatting (rustfmt)
   - Use clippy recommendations
   - Document public APIs

2. **Testing**
   - Write unit tests for all public functions
   - Use integration tests for API endpoints
   - Maintain test coverage

3. **Commits**
   - Use conventional commits format
   - Keep commits focused and atomic
   - Include tests with feature changes

## Building for Production

```bash
# Build release version
cargo build --release

# Run security audit
cargo audit

# Run all checks
cargo build --all-targets
cargo test
cargo clippy
cargo fmt -- --check
```

## Common Issues

1. **Build Failures**
   - Check Rust version compatibility
   - Verify dependencies in Cargo.toml
   - Clear cargo cache if needed

2. **Test Failures**
   - Ensure test database is available
   - Check environment variables
   - Verify test data prerequisites