# nextjs-gae-demo

Demonstration of [Next.js](https://nextjs.org) 8.x on [Google App Engine's Standard Environment for Node.js](https://cloud.google.com/appengine/docs/standard/nodejs/).

### Prerequisites

1. Install the [Google Cloud Platform SDK](https://cloud.google.com/sdk/).
2. Clone this repo.

### Test the App

Start the app to make sure it runs properly.

```sh
npm run dev
```

### Configuring a New GCP Project and Application

If you have not set up a project and application to run this demo, follow the steps below. Otherwise, skip to the next section.

First, authenticate to GCP if you have not already:

```sh
gcloud auth login
```

Using the GCP CLI, create a new project and application. Replace `PROJECT-NAME` with your own.

```sh
gcloud projects create PROJECT-NAME
gcloud config set project PROJECT-NAME
gcloud app create
```

Wait a few minutes while Google provisions resources. While you are waiting, enable the Cloud Build API for your project by visiting the Cloud Build API page for your project (ex: https://console.developers.google.com/apis/api/cloudbuild.googleapis.com/overview?project=PROJECT-NAME).

### Building and Deploying the Application

Easy!

```sh
npm run build
npm run deploy
```

Visit the link provided by GCP to test.
