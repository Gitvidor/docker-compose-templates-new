# Docker Compose Services Collection

This repository contains a collection of Docker Compose configurations for commonly used services in development and production environments. Each service is configured independently, allowing for flexible deployment based on your needs.

## Available Services

### 1. Redis
- **Version**: Latest
- **Port**: 6379
- **Features**:
  - Data persistence enabled
  - Appendonly mode
  - Volume mounting for data
  - Custom network configuration

### 2. MySQL
- **Version**: 8.0
- **Port**: 3306
- **Features**:
  - Configurable root password
  - Default database creation
  - User creation support
  - Data persistence
  - Initialization scripts support

### 3. Nginx
- **Version**: Latest
- **Ports**: 80, 443
- **Features**:
  - SSL support
  - Custom configuration mounting
  - Static content hosting
  - Log management
  - SSL certificate management

### 4. MongoDB
- Standalone MongoDB instance
- Data persistence
- Custom network configuration

### 5. Elasticsearch
- Full-text search engine
- Data persistence
- Custom network configuration

### 6. PostgreSQL
- Advanced open source database
- Data persistence
- Custom network configuration

### 7. Grafana
- Metrics visualization
- Dashboard management
- Custom network configuration

### 8. RabbitMQ
- Message broker
- Management interface
- Custom network configuration

### 9. Kafka
- Distributed streaming platform
- Zookeeper integration
- Custom network configuration

### 10. Jenkins
- Continuous Integration/Deployment
- Build automation
- Custom network configuration

### 11. Prometheus
- Metrics collection
- Monitoring solution
- Custom network configuration

## Usage

Each service is contained in its own directory with a dedicated `docker-compose.yaml` file. To use any service:

1. Navigate to the service directory:
   ```bash
   cd <service-name>
   ```

2. Start the service:
   ```bash
   docker-compose up -d
   ```

3. Stop the service:
   ```bash
   docker-compose down
   ```

## Configuration

Each service can be configured by modifying its respective `docker-compose.yaml` file. Environment variables, ports, and volumes can be adjusted according to your needs.

## Data Persistence

All services are configured with data persistence using Docker volumes. Data will be preserved across container restarts.

## Networks

Each service uses its own isolated network by default. If you need services to communicate with each other, you'll need to create a common network or adjust the network configurations.

## Security

- Default passwords should be changed before deploying to production
- SSL certificates should be properly configured for production use
- Sensitive environment variables should be managed securely

## Contributing

Feel free to contribute by:
1. Forking the repository
2. Creating a feature branch
3. Committing your changes
4. Creating a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.