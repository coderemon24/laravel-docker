📦 Laravel Docker Setup

This repository provides a ready-to-use Docker environment for running Laravel applications easily.
You can clone this repo and install your Laravel project inside the main-app folder.

🚀 Features
Laravel-ready Docker setup
PHP + Apache
MySQL support
Easy project mounting via main-app
Beginner-friendly structure

📁 Project Structure
laravel-docker/
│
├── main-app/          # Your Laravel project goes here
├── docker/            # Docker configuration files
├── docker-compose.yml
├── Dockerfile
└── README.md

⚙️ Requirements
Make sure you have installed:

Docker
Docker Compose

🛠️ Installation Guide
1. Clone the repository
    git clone https://github.com/coderemon24/laravel-docker.git
    cd laravel-docker
    
2. Install Laravel inside main-app
    If Laravel is not installed yet:
    cd main-app
    composer create-project laravel/laravel .
    
3. Start Docker containers

Go back to root folder:

cd ..
docker-compose up -d --build

4. Run migrations (optional)
    docker exec -it app bash
    php artisan migrate
    
🌐 Access Project
    After successful setup, open in browser:
    http://localhost:8000
    (Configure your port in docker-compose.yml if needed)

🗄️ Database Configuration (.env)
    Update your Laravel .env file:

    DB_CONNECTION=mysql
    DB_HOST=mysql
    DB_PORT=3306
    DB_DATABASE=demo
    DB_USERNAME=test
    DB_PASSWORD=test
    
🔄 Useful Commands
    Stop containers
    docker-compose down
    Rebuild containers
    docker-compose up -d --build
    Enter app container
    docker exec -it app bash
    
📌 Notes
    Always place your Laravel project inside main-app
    Do not run composer install on host if using container PHP (optional setup dependent)
    Make sure ports are not blocked by other services
