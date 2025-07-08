# Jack Lei - Personal Website

A modern, responsive personal website built with HTML, CSS, and JavaScript featuring a Revolution Slider with particles effect.

## Features

- 🎨 Modern design with particles animation
- 📱 Fully responsive
- ⚡ Simple and fast static website
- 🐳 Docker ready
- 📦 No build process required
- 🔄 Automated Docker builds with GitHub Actions

## Quick Start with Docker

```bash
# Build and run the website
docker-compose up -d

# Access the website at http://localhost:8080
```

### Using Docker directly

```bash
# Build the container
docker build -t jacklei-website .

# Run the container
docker run -d -p 8080:80 --name jacklei-website jacklei-website

# Access the website at http://localhost:8080
```

## GitHub Actions

This repository includes automated Docker builds via GitHub Actions:

### GitHub Container Registry (Default)
- **Workflow**: `.github/workflows/docker-build.yml`
- **Registry**: `ghcr.io`
- **Image**: `ghcr.io/yourusername/jacklei-website`
- **Triggers**: Push to main/master, tags, pull requests
- **No setup required** - uses `GITHUB_TOKEN` automatically

### Docker Hub (Alternative)
- **Workflow**: `.github/workflows/docker-hub.yml`
- **Registry**: `docker.io`
- **Image**: `yourusername/jacklei-website`
- **Setup required**: Add secrets `DOCKER_USERNAME` and `DOCKER_PASSWORD`

### Using the Built Images

```bash
# From GitHub Container Registry
docker run -d -p 8080:80 ghcr.io/yourusername/jacklei-website:main

# From Docker Hub (if configured)
docker run -d -p 8080:80 yourusername/jacklei-website:main
```

## Development

### Local Development

Simply open `index.html` in your browser or use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server -p 8000

# Using PHP
php -S localhost:8000
```

### Project Structure

```
jacklei.com/
├── assets/
│   ├── css/          # Stylesheets
│   ├── fonts/        # Font files
│   ├── images/       # Images
│   └── js/           # JavaScript files
├── .github/
│   └── workflows/    # GitHub Actions workflows
├── index.html        # Main page
├── Dockerfile        # Docker configuration
├── docker-compose.yml # Docker Compose configuration
└── README.md         # This file
```

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Revolution Slider
- Nginx (Docker deployment)
- GitHub Actions (CI/CD)

## License

This project is for personal use. 