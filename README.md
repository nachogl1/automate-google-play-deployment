# Deployment Pipeline for GitActions and Google Play

**It is assumed that you have all the necessary tools to run Angular-Ionic applications (Node, NPM, Angular, Ionic, Capacitor, etc).**
*Please, for further details and infromation refer to*
 - https://ionicframework.com/docs
 - https://capacitorjs.com/

## Steps followed to create this repo (New Ionic Project)
 
 - Run the following command to create the project **ionic start automate-google-play-deployment blank --capacitor**

## Steps that were taken to make it run after being created
 - After creating it, you must build the app at least once before adding any platform (iOS, Android, etc). For this you run **ionic build**. This will create 
a folder called **www**
 - Install necessary dependencies to add your platform via running **npm install @capacitor/android**
 - After this, we will need to add the platform we want to work on, for this tutorial we will only focus on Android (Google Play Store), for this we will run
 **npx cap add android** (*Note: npx is a new utility available in npm 5 or above that executes local binaries/scripts to avoid global installs.*)
 - Usually, what I used to do to make it run is open Android Studio IDE, this will load the project, I will construct the APK and then, manually, take the file 
and upload it myself on the Google Play Console. We will automate this so you do not even need to run Android Studio, but just in case you need it, you would need to 
 download the IDE and you can run the following command to open it automatically: **npx cap open android**

## Things to know when you make changes in your project, and you want to sync it
 - Every time you perform a build (e.g. ionic build) that changes your web directory (default: www), you'll need to copy those changes down to your native projects:
**npx cap copy**. Have a look at npx cap sync for more functionalities.

## How to run it
- Run the command: **ionic serve**
