# Portfolio-App

This document contains a minimal, production-ready starter for a Portfolio application using Laravel (API) and Vue 3 (Vite) as the frontend. It includes database migration, API routes, controller, simple resource, and a Vue frontend with components

Features

CRUD Projects (title, description, image, url, tags)

Laravel API (sanctum optional for auth)

Vue 3 + Vite SPA consuming API via Axios

File upload (images) stored in storage/app/public

Tech Stack

Backend: PHP 8.1+, Laravel 10+

Frontend: Vue 3 (Composition API), Vite

DB: MySQL / SQLite for dev

HTTP: Axios

Quick Setup (commands):
# create laravel project
composer create-project laravel/laravel portfolio-backend
cd portfolio-backend

# create frontend inside Laravel (optional) or separate folder
npm create vite@latest portfolio-frontend -- --template vue
cd portfolio-frontend
npm install

In the Laravel app:
# install packages
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"

# create storage link
php artisan storage:link

# migrate
php artisan migrate

# run
php artisan server

In the frontend folder:
npm install axios
npm run dev

Database: Migration (projects table):

database/migrations/2025_01_01_000000_create_projects_table.php

Model & Resource:

app/Models/Project.php
app/Http/Resources/ProjectResource.php
