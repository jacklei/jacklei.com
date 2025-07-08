# Jack Lei - Personal Website

A modern, responsive personal website built with HTML, CSS, and JavaScript featuring a Revolution Slider with particles effect.

## Features

- 🎨 Modern design with particles animation
- 📱 Fully responsive
- ⚡ Ultra-fast performance with Bun bundling
- 🐳 Docker ready
- 📦 Lightning-fast build system

## Quick Start with Docker

### Option 1: Using Docker Compose (Recommended)

```bash
# Build and run the website
docker-compose up -d

# Access the website at http://localhost:8080
```

### Option 2: Using Docker directly

```bash
# Build the Docker image
docker build -t jacklei-website .

# Run the container
docker run -d -p 8080:80 --name jacklei-website jacklei-website

# Access the website at http://localhost:8080
```

## Development

### Building with Bun

```bash
# Make build script executable
chmod +x build.sh

# Run the build process
./build.sh
```

This will:
- Install Bun dependencies
- Bundle and optimize all assets with lightning speed
- Create production-ready files in `dist/`
- Show build information and file sizes

### Development Server

```bash
# Start development server with hot reload
bun run dev

# Preview production build
bun run preview
```

### Installing Bun

If you don't have Bun installed:
```bash
curl -fsSL https://bun.sh/install | bash
```

### Local Development

Simply open `index.html` in your browser or use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server -p 8000
```

## Project Structure

```
jacklei.com/
├── assets/
│   ├── css/          # Stylesheets
│   ├── fonts/        # Font files
│   └── js/           # JavaScript files
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
- Bun (Ultra-fast JavaScript runtime & bundler)

## License

This project is for personal use. 