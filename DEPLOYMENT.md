# 🚀 Ecommerce System - Deployment Guide

## GitHub Actions Workflows

The project includes automated workflows:

### 1. **Tests** (`.github/workflows/test.yml`)
- Runs on every push and pull request
- Tests Python syntax
- Runs linting checks
- Environment: Python 3.10

### 2. **Build** (`.github/workflows/build.yml`)
- Builds Docker image
- Caches build layers for faster builds
- Validates Dockerfile

## Local Deployment

### Prerequisites
- Docker & Docker Compose
- Python 3.10+
- pip

### Quick Start

```bash
# Clone repository
git clone https://github.com/kanoon254569-cell/store.git
cd store

# Option 1: Using Docker Compose
docker-compose up -d

# Option 2: Run locally
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python -m uvicorn backend.main:app --host 0.0.0.0 --port 8000
```

### Access Points
- **Admin Dashboard**: http://localhost:8000 (port depends on setup)
- **API Docs**: http://localhost:8000/docs
- **Admin Credentials**: Use credentials set through `create_admin_user.py`

## Cloud Deployment Options

### Option 1: Heroku (Free tier available)
```bash
# Install Heroku CLI
brew install heroku

# Login
heroku login

# Create app
heroku create your-app-name

# Deploy
git push heroku main
```

### Option 2: Railway (Simple: Connect GitHub repo directly)
1. Visit https://railway.app
2. Click "New Project"
3. Select "Deploy from GitHub repo"
4. Select this repository
5. Configure environment variables
6. Deploy

### Option 3: AWS / DigitalOcean / Google Cloud
Deploy using Docker image:
```bash
# Build and push to Docker Hub (requires account)
docker build -t yourusername/ecommerce:latest .
docker push yourusername/ecommerce:latest
```

## Environment Variables

Create `.env` file in root directory:
```
MONGODB_URL=your_mongo_url
JWT_SECRET=your_secret_key
ADMIN_EMAIL=admin@ecommerce.com
```

## API Endpoints

- `POST /auth/register` - Register user
- `POST /auth/login` - User login
- `POST /auth/admin-login` - Admin login
- `GET /products` - Get all products
- `POST /orders` - Create order
- `GET /dashboard` - Get admin dashboard

See `/docs` endpoint for full API documentation

## Troubleshooting

### Port already in use
```bash
# Change port
python -m uvicorn backend.main:app --port 8001
```

### Database connection errors
- Ensure MongoDB is running
- Check MONGODB_URL in environment

### Authorization errors
- Create admin user: `python create_admin_user.py`
- Ensure JWT_SECRET is set in .env

## CI/CD Pipeline

Every push to `main` branch automatically:
1. Runs Python syntax tests
2. Builds Docker image
3. Caches layers for faster builds

Add more workflows in `.github/workflows/` for additional automation.
