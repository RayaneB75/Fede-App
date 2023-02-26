# Federation Application

This projects focuses on providing the "Federation des associations d'IMT Atlantique" with a mobile application to distribute to students. The application is meant to be used by students to find information about the associations and their events.

The origin comes from the fact that all events and informations about the associations are currently distributed through Facebook. This is not optimal as it is not easy to find information about the associations and their events. The goal of this project is to provide a mobile application that will allow students to find these informations easily and not rely on Facebook groups.

This project is linked to the [Federation Application Backend]() project. It's a go application that will provide the data to the mobile application (database, API requests and so on).

## Getting Started

This project is a Flutter application (to build application for iOS and Android simultaneously).

For help getting started with Flutter, view the online [documentation](https://flutter.dev/).

Here are also some useful links:
- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)


## Targeted infrastructure

The application is meant to be used by students of IMT Atlantique. The application will be distributed through the Google Play Store and the Apple App Store.

But, only the IMT Atlantique students will be able to use the application. The goal is to provide a way for the students to log in to the application. This will be done by providing on the first login a form to fill in with the student's IMT Atlantique email address. This will be used to verify that the student is a student of IMT Atlantique.

Then, the student will be able to choose the campus he is currently on. This will be used to provide the student with the events and informations about the associations that are relevant to him. This information is not static and could be updated by the student (if he changes campus for example).

Nonetheless, the student will not be able to logout (yet) as the application is meant to be used by students all the time.


## Features

The application will provide the following features:
- A login page to log in with the student's IMT Atlantique email address
- A main page with latest events and informations about the associations
- A page to display the events of the associations the student is following
  - This should also contain a way to follow/unfollow an association
  - The list of associations should be sorted by name
- A contact page to contact the developers of the application

## Architecture

The application will be built using the Model-View-Controller (MVC) architecture. This architecture is well suited for Flutter applications as it is the architecture used by Flutter.

The application will be built using the following packages:
- [provider](https://pub.dev/packages/provider) to provide the state of the application to the widgets
- [http](https://pub.dev/packages/http) to make HTTP requests to the backend
- 