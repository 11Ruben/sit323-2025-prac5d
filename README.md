# SIT323- Cloud Native Application Development

## sit323-2025-prac5d - Publishing the microservice into the cloud

## Steps for completing this task:

### 1. Login to Google Cloud:
``` gcloud auth login ```

### 2. Create a new repository in Google Cloud
Make sure to select **"australia-southeast2 (Melbourne)"** as region

### 3. Authenticate with Google Cloud Artifact Registry:
``` gcloud auth configure-docker australia-southeast2-docker.pkg.dev ```

### 4. Tag the pre-build image from docker:
``` docker tag sit323-2025-prac5d australia-southeast2-docker.pkg.dev/sit323-25t1-ruben-ooi-318b5cc/task5d/sit323-2025-prac5d:v1 ```

### 5. Push the image into Google Cloud repository:
``` docker push australia-southeast2-docker.pkg.dev/sit323-25t1-ruben-ooi-318b5cc/task5d/sit323-2025-prac5d:v1 ```

### 6. Run the published image:
``` docker run -p 3040:3040 australia-southeast2-docker.pkg.dev/sit323-25t1-ruben-ooi-318b5cc/task5d/sit323-2025-prac5d:v1 ```
