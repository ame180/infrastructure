# Infrastructure

This repository is a monorepo for Docker images that are reused across multiple projects. It also contains the setup for automatic updates and builds of these images using GitHub Actions workflows.

## Automatic Updates

Images in this repository are automatically rebuilt and pushed on a weekly schedule, as well as on manual request. This ensures that base images and dependencies are kept up to date with the latest security patches and improvements.

## Images

Below is a list of images managed in this repository. Each image has its own directory and Dockerfile. Major versions are tracked separately to avoid breaking downstream dependencies.

- **nginx-node**: Nginx image set up to route HTTP traffic to a Node.js container, or serve static files if they exist.
- **nginx-php**: Nginx image configured to forward requests to PHP-FPM, or serve static files if present.
  - **Environment Variables**:
    - `APP_PATH`: The root directory of the application (default: `/app`).
- **mariadb**: A MariaDB instance optimized for minimal base memory usage.
