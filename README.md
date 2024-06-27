# Karsajobs Project

This project was created as a submission for the Dicoding Microservices class.

The Karsajobs project is a microservices-based application designed to manage job postings. It consists of a backend service written in Go and a frontend service built with Vue.js. The project also includes Kubernetes configuration files to deploy the services.

## Backend Service: Karsajobs

The backend service for Karsajobs is written in Go. It provides RESTful APIs to manage job postings. 

### Key Files:
- `cmd/web/main.go`: Entry point for the backend service.
- `cmd/web/handlers.go`: HTTP handlers for the service.
- `pkg/models/mongodb`: MongoDB models and helpers.

### Building and Running:
1. **Build the Docker Image**:
    ```sh
    ./build_push_image_karsajobs.sh
    ```

2. **Run the Container**:
    ```sh
    docker-compose up -d
    ```

## Frontend Service: Karsajobs-UI

The frontend service for Karsajobs is built with Vue.js. It provides a user interface for managing job postings.

### Key Files:
- `src/App.vue`: Main Vue component.
- `src/components`: Vue components for different parts of the application.

### Building and Running:
1. **Build the Docker Image**:
    ```sh
    ./build_push_image_karsajobs_ui.sh
    ```

2. **Run the Container**:
    ```sh
    docker-compose up -d
    ```

## Kubernetes Deployment

The project includes Kubernetes configuration files to deploy the services in a Kubernetes cluster.

### Key Files:
- `kubernetes/backend`: Deployment and service files for the backend.
- `kubernetes/frontend`: Deployment and service files for the frontend.
- `kubernetes/mongodb`: Deployment, service, and configuration files for MongoDB.

### Deploying to Kubernetes:
1. **Apply Namespace**:
    ```sh
    kubectl apply -f namespace.yml
    ```

2. **Deploy MongoDB**:
    ```sh
    kubectl apply -f kubernetes/mongodb/
    ```

3. **Deploy Backend**:
    ```sh
    kubectl apply -f kubernetes/backend/
    ```

4. **Deploy Frontend**:
    ```sh
    kubectl apply -f kubernetes/frontend/
    ```

## Additional Information

This project demonstrates a complete microservices application, including backend, frontend, and database services, all containerized and deployed using Docker and Kubernetes. The setup ensures a consistent and reproducible environment across development, testing, and production.


