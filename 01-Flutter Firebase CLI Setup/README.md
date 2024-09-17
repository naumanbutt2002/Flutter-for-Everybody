Click flutter icon on 

then follow steps
at C:/users

npm install -g firebase-tools
firebase login
firebase projects:list
dart pub global activate flutterfire_cli

Then, at the root of your Flutter project directory, run this command:
flutterfire configure --project_name

replace this project name with your project


then
main.dart:
import 'package:flutter/material.dart';
import 'package:firebase_core/firebase_core.dart';
import 'firebase_options.dart';

void main() async{
  WidgetsFlutterBinding.ensureInitialized(); // Ensure that Firebase is initialized
  await Firebase.initializeApp(
    options: DefaultFirebaseOptions.currentPlatform,
);
  runApp(const MyApp());
}

then in android>app>build.gradle
make  minSdk = 21

defaultConfig {
        minSdk = 21
        targetSdk = flutter.targetSdkVersion
        versionCode = flutter.versionCode
        versionName = flutter.versionName
    }