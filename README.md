This is a test project to build a simple node.js app at GCP Cloud Run

The instructions are contained in Google Cloud Run course, Lab w3.

To build this app:

1. Clone this repo to GCP CLI.
2. gcloud services enable run.googleapis.com
3. gcloud config set compute/region us-central1
4. LOCATION="us-central1"
5. gcloud builds submit --tag gcr.io/$GOOGLE_CLOUD_PROJECT/helloworld
6. check using: gcloud container images list
7. test locally: docker run -d -p 8080:8080 gcr.io/$GOOGLE_CLOUD_PROJECT/helloworld, then preview on 8080
8. gcloud run deploy --image gcr.io/$GOOGLE_CLOUD_PROJECT/helloworld --allow-unauthenticated --region=$LOCATION and then try URL in any browser


