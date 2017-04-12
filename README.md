# Python + Flask + SparkPost Example on Google App Engine Standard

<a href="https://www.sparkpost.com"><img src="https://www.sparkpost.com/sites/default/files/attachments/SparkPost_Logo_2-Color_Gray-Orange_RGB.svg" width="200px"/></a>

[Sign up](https://app.sparkpost.com/sign-up?src=Dev-Website&sfdcid=70160000000pqBb) for a SparkPost account and visit our [Developer Hub](https://developers.sparkpost.com) for even more content.

This sample app demonstrates how to send email with Python and [python-sparkpost](https://github.com/SparkPost/python-sparkpost) on the Google App Engine standard environment.

### Prerequisites

 - a [Google Cloud Platform](https://cloud.google.com/) account
 - the [Google Cloud SDK](https://cloud.google.com/sdk/) installed and configured

### Setup

1. Sign up for a SparkPost account [here](https://app.sparkpost.com/sign-up).

1. Create an API key with *Transmissions: read/write* privilege [here](https://app.sparkpost.com/account/credentials).

1. Add your API key to `app.yaml`.

1. Install the app's dependencies:
    ```sh
    mkdir lib
    pip install -r requirements -t lib
    ```

### Running Locally

1. Run the app using the Google Cloud SDK dev app server:
    ```sh
    $GCLOUD_SDK/bin/dev_appserver.py app.yaml
    ```

1. Visit the app in your browser: [http://localhost:8080/](http://localhost:8080/)

### Deploying To Google App Engine

1. Deploy the app and dependencies to your Google Cloud project:
    ```sh
    gcloud app deploy
    ```

1. Visit the app in your browser: 
    ```sh
    gcloud app browse
    ```

### Running The Tests

```sh
pip install pytest responses flaky
pytest main_test.py
```

