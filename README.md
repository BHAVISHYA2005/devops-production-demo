# DevOps Production Demo

[![CI/CD Pipeline](https://github.com/BHAVISHYA2005/devops-production-demo/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/BHAVISHYA2005/devops-production-demo/actions/workflows/ci-cd.yml)

A production-ready Node.js application demonstrating DevOps best practices including containerization, CI/CD pipelines, and automated deployment.

## 🚀 Features

- **RESTful API** with Express.js
- **Docker containerization** with multi-stage builds
- **CI/CD pipeline** with GitHub Actions
- **Automated deployment** to Render
- **Health checks** and monitoring endpoints
- **Security headers** with Helmet.js
- **Comprehensive testing** with Jest
- **Production logging** with Morgan
- **CORS support** for cross-origin requests

## 📋 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Welcome message and app info |
| GET | `/health` | Health check endpoint |
| GET | `/api/users` | Get all users |
| POST | `/api/users` | Create a new user |

## 🛠️ Local Development

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Docker (optional)

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/BHAVISHYA2005/devops-production-demo.git
   cd devops-production-demo
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start development server:**
   ```bash
   npm run dev
   ```

4. **Run tests:**
   ```bash
   npm test
   ```

The application will be available at `http://localhost:3000`

## 🐳 Docker

### Build and run locally:

```bash
# Build the image
docker build -t devops-production-demo .

# Run the container
docker run -p 3000:3000 devops-production-demo
```

### Using Docker Compose (optional):

```bash
docker-compose up --build
```

## 🚀 Deployment

### Render Deployment

This application is configured for automatic deployment to Render through GitHub Actions.

#### Setup Steps:

1. **Create a Render account** at [render.com](https://render.com)

2. **Create a new Web Service** on Render:
   - Connect your GitHub repository
   - Choose "Docker" as the environment
   - Set the region and instance type

3. **Configure GitHub Secrets:**
   Go to your GitHub repository → Settings → Secrets and add:
   
   ```
   RENDER_SERVICE_ID=your-render-service-id
   RENDER_API_KEY=your-render-api-key
   RENDER_URL=https://your-app-name.onrender.com
   ```

4. **Deploy:**
   - Push to the `main` branch
   - GitHub Actions will automatically build and deploy

### Manual Deployment

You can also deploy manually using the Render dashboard or CLI.

## 🔧 Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Server port | `3000` |
| `NODE_ENV` | Environment mode | `development` |

## 📊 Monitoring

- **Health Check:** `GET /health`
- **Application Logs:** Available through your hosting platform
- **Docker Health Check:** Built-in container health monitoring

## 🔐 Security Features

- **Helmet.js:** Security headers
- **CORS:** Cross-origin resource sharing
- **Input validation:** Request body validation
- **Non-root user:** Docker container runs as non-root
- **Dependency scanning:** Automated security scans

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests with coverage
npm run test:coverage

# Run tests in watch mode
npm run test:watch
```

## 📁 Project Structure

```
devops-production-demo/
├── .github/
│   └── workflows/
│       └── ci-cd.yml          # GitHub Actions CI/CD pipeline
├── app.js                     # Main application file
├── app.test.js               # Test suite
├── package.json              # Node.js dependencies
├── Dockerfile                # Docker configuration
├── .dockerignore            # Docker ignore file
└── README.md                # This file
```

## 🔄 CI/CD Pipeline

The GitHub Actions pipeline includes:

1. **Test Stage:**
   - Code checkout
   - Dependencies installation
   - Linting (if configured)
   - Unit tests
   - Coverage reports

2. **Build Stage:**
   - Docker image build
   - Multi-platform support (AMD64, ARM64)
   - Image push to GitHub Container Registry

3. **Security Stage:**
   - Vulnerability scanning with Trivy
   - Security report upload

4. **Deploy Stage:**
   - Automatic deployment to Render
   - Health check verification

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support and questions:
- Create an issue in this repository
- Contact: your-email@example.com

---

**Built with ❤️ for DevOps interviews and production deployments**