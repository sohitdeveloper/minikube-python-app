# Minikube Django Application

This project demonstrates how to deploy a Django web application on Minikube, a tool that enables you to run Kubernetes locally. The web application is built using Django, a high-level Python web framework.

## Prerequisites

Before you begin, ensure you have the following prerequisites installed on your local machine:

- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Docker](https://docs.docker.com/get-docker/)
- Python (for local development)
- Django (for local development)

## Installation

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/sohitdeveloper/minikube-python-app.git
    ```

2. Navigate to the project directory:

    ```bash
    cd minikube-python-app
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

To run the Django web application locally, use the following command:

```bash
python manage.py runserver
```

This will start the Django development server, and you can access the web application by visiting `http://localhost:8000` in your web browser.

## Deployment on Minikube

To deploy the Django application on Minikube, follow these steps:

1. Start Minikube:

    ```bash
    minikube start
    ```

2. Build the Docker image:

    ```bash
    docker build -t minikube-django-app .
    ```

3. Apply the Kubernetes manifests:

    ```bash
    kubectl apply -f deployment.yml
    kubectl apply -f service.yml
    ```

4. Access the deployed application:

    ```bash
    minikube service minikube-django-app-service
    ```

This will open the Django web application in your default web browser.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---

Make sure to replace `minikube-django-app`, `deployment.yml`, and `service.yml` with your actual project name and Kubernetes YAML file names. If you have any further questions or need additional assistance, feel free to ask!
