# CLEAN WATER EXPLORER

A Web Application for users to locate safely managed water points.

## Prerequisites

You'll need the following:
* [IBM Cloud account](https://console.ng.bluemix.net/registration/)
* [Cloud Foundry CLI](https://github.com/cloudfoundry/cli#downloads)
* [Git](https://git-scm.com/downloads)
* [Maven](https://maven.apache.org/download.cgi)


## 1. Clone the application

Clone the repository and change to the directory to where the clean-water app is located.
```
git clone https://github.com/emkgth/clean-water.git
cd clean-water
```

## 2. Run the app locally

build a .war file as defined in the pom.xml file to run the app.
Install the .war file in your webapp container. 
To run locally, you will need to configure a proxy (this is a ArcGIS Requirement. You can find instructions here: https://codeload.github.com/Esri/resource-proxy/zip/refs/heads/master

## 3. Deploy the app to IBM Cloud

You can use the Cloud Foundry CLI to deploy the app.

Choose your API endpoint

```
cf api <API-endpoint>
```

Replace the *API-endpoint* in the command with an API endpoint from the following list.

|URL                             |Region          |
|:-------------------------------|:---------------|
| https://api.ng.bluemix.net     | US South       |
| https://api.eu-de.bluemix.net  | Germany        |
| https://api.eu-gb.bluemix.net  | United Kingdom |
| https://api.au-syd.bluemix.net | Sydney         |


Login to your IBM Cloud account:

```
cf login
```

From within the *clean-water* directory push your app to IBM Cloud
```
cf push
```

When deployment completes you should see a message indicating that your app is running.  View your app at the URL listed in the output of the push command. 
You can also go to your ibm cloud account, select Resource list -> Cloud Foundry Apps - > Clean Water App -> Visit App URL

