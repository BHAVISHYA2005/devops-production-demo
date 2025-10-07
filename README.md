# DevOps Production Demo

A Node.js REST API demonstrating modern DevOps practices with automated CI/CD pipeline and containerization.

## Quick Start

```bash
# Clone and run locally
git clone https://github.com/BHAVISHYA2005/devops-production-demo.git
cd devops-production-demo
npm install
npm start
```

Visit `http://localhost:3000` to see the API running.

## API Endpoints

- `GET /` - Welcome message
- `GET /health` - Health check
- `GET /api/users` - Sample user data

## Testing

```bash
npm test
```

## Docker

```bash
# Build and run container
docker build -t devops-demo .
docker run -p 3000:3000 devops-demo
```

## Features

- **REST API** with Express.js
- **Automated Testing** with Jest
- **Docker Containerization** with security best practices
- **CI/CD Pipeline** with GitHub Actions
- **Health Monitoring** endpoints
- **Production Ready** with proper error handling

## CI/CD Pipeline

The GitHub Actions workflow automatically:
1. Runs tests on every push
2. Builds Docker image
3. Performs security scanning
4. Deploys to cloud platforms

## Tech Stack

- **Backend**: Node.js, Express.js
- **Testing**: Jest, Supertest
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Deployment**: Render (cloud-ready)

## Development

```bash
# Run in development mode
npm run dev

# Run tests with watch
npm run test:watch
```

---

Built for demonstrating DevOps best practices in production environments.