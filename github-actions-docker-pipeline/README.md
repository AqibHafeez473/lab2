# GitHub Actions Docker Pipeline

This project demonstrates how to build and deploy Docker images using GitHub Actions and the GitHub Container Registry.

## Project Structure

```
github-actions-docker-pipeline
├── .github
│   └── workflows
│       └── docker-build-deploy.yml  # GitHub Actions workflow for CI/CD
├── Dockerfile                         # Dockerfile for building the application image
├── src
│   └── app.js                        # Main application file
├── package.json                      # npm configuration file
└── README.md                         # Project documentation
```

## Getting Started

To get started with this project, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd github-actions-docker-pipeline
   ```

2. **Build the Docker image**:
   You can build the Docker image locally using the following command:
   ```bash
   docker build -t <image-name> .
   ```

3. **Run the application**:
   After building the image, you can run the application using:
   ```bash
   docker run -p 3000:3000 <image-name>
   ```

4. **Access the application**:
   Open your browser and navigate to `http://localhost:3000` to access the application.

## CI/CD Pipeline

This project includes a GitHub Actions workflow located in `.github/workflows/docker-build-deploy.yml`. The workflow is triggered on pushes to the main branch and performs the following steps:

- Builds the Docker image from the Dockerfile.
- Pushes the built image to the GitHub Container Registry.

Make sure to set up the necessary secrets in your GitHub repository for authentication with the GitHub Container Registry.

## License

This project is licensed under the MIT License. See the LICENSE file for details.