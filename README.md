# CustomTaskManagerRails

This repository contains a Task Management System built with Ruby on Rails. Users can create, update, delete, and manage tasks, along with user authentication and authorization functionalities. Endpoints are designed for tasks, projects, and user management, providing a comprehensive solution for managing tasks and projects efficiently.

## Features

- User registration and authentication
- Create, read, update, and delete tasks
- Manage projects
- User authorization with JWT

## Prerequisites

- Ruby
- Rails
- SQLite (for development)

## Getting Started

### Setting Up the Environment

1. **Update your package list:**
   ```sh
   sudo apt update
   ```

2. **Install dependencies:**
   ```sh
   sudo apt install -y curl gpg build-essential
   ```

3. **Install RVM (Ruby Version Manager):**
   ```sh
   \curl -sSL https://get.rvm.io | bash -s stable
   source ~/.rvm/scripts/rvm
   ```

4. **Install Ruby using RVM:**
   ```sh
   rvm install ruby
   rvm use ruby --default
   ```

5. **Verify the installation:**
   ```sh
   ruby -v
   ```

6. **Install Bundler (a dependency manager for Ruby):**
   ```sh
   gem install bundler
   ```

7. **Install Rails:**
   ```sh
   gem install rails
   ```

8. **Verify the installation:**
   ```sh
   rails -v
   ```

### Setting Up the Project

1. **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/CustomTaskManagerRails.git
   cd CustomTaskManagerRails
   ```

2. **Install dependencies:**
   ```sh
   bundle install
   ```

3. **Set up the database:**
   ```sh
   rails db:create
   rails db:migrate
   ```

4. **Run the server:**
   ```sh
   rails server
   ```

5. **Access the application:**
   Open your browser and go to `http://localhost:3000`.

<! --

## API Endpoints

### User Endpoints

- **Register:**
  - `POST /users`
  - Request body:
    ```json
    {
      "username": "your_username",
      "password": "your_password",
      "password_confirmation": "your_password"
    }
    ```

- **Login:**
  - `POST /login`
  - Request body:
    ```json
    {
      "username": "your_username",
      "password": "your_password"
    }
    ```

### Task Endpoints

- **Get all tasks:**
  - `GET /tasks`
  - Header: `Authorization: Bearer <token>`

- **Create a new task:**
  - `POST /tasks`
  - Request body:
    ```json
    {
      "title": "Task Title",
      "description": "Task Description",
      "project_id": 1
    }
    ```
  - Header: `Authorization: Bearer <token>`

- **Update a task:**
  - `PUT /tasks/:id`
  - Request body:
    ```json
    {
      "title": "Updated Task Title",
      "description": "Updated Task Description",
      "project_id": 1
    }
    ```
  - Header: `Authorization: Bearer <token>`

- **Delete a task:**
  - `DELETE /tasks/:id`
  - Header: `Authorization: Bearer <token>`

### Project Endpoints

- **Get all projects:**
  - `GET /projects`
  - Header: `Authorization: Bearer <token>`

- **Create a new project:**
  - `POST /projects`
  - Request body:
    ```json
    {
      "name": "Project Name",
      "description": "Project Description"
    }
    ```
  - Header: `Authorization: Bearer <token>`

- **Update a project:**
  - `PUT /projects/:id`
  - Request body:
    ```json
    {
      "name": "Updated Project Name",
      "description": "Updated Project Description"
    }
    ```
  - Header: `Authorization: Bearer <token>`

- **Delete a project:**
  - `DELETE /projects/:id`
  - Header: `Authorization: Bearer <token>`

-->
