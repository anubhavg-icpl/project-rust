# Operations Guide

## Deployment

### Local Environment

```bash
cargo run --release
```

### Docker Deployment

1. **Build Image**
   ```bash
   docker build -t project-rust:latest .
   ```

2. **Run Container**
   ```bash
   docker run -p 8080:8080 project-rust:latest
   ```

### Configuration

The service uses environment variables for configuration:

| Variable | Description | Default |
|----------|-------------|---------|
| RUST_LOG | Log level (error, warn, info, debug, trace) | info |
| HOST | Service host | 127.0.0.1 |
| PORT | Service port | 8080 |

## Monitoring

### Health Checks

Monitor the `/health` endpoint for service health:

```bash
curl http://localhost:8080/health
```

### Logging

The service uses structured logging with the following levels:

- ERROR: Service errors requiring immediate attention
- WARN: Important events that need investigation
- INFO: Normal operational events
- DEBUG: Detailed information for debugging

### Metrics

Future versions will include:

- Prometheus metrics endpoint
- Request latency metrics
- Error rate metrics
- Custom business metrics

## Maintenance

### Backup and Recovery

Currently no persistent data to backup.

### Upgrading

1. Build new version
2. Run tests
3. Deploy new container
4. Verify health check
5. Remove old container

### Troubleshooting

Common issues and solutions:

1. **Service Unavailable**
   - Check service logs
   - Verify port bindings
   - Check resource usage

2. **High Latency**
   - Monitor system resources
   - Check network connectivity
   - Review concurrent connections

3. **Memory Issues**
   - Check for memory leaks
   - Review heap usage
   - Adjust container limits