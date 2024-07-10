## ENSE 375 - Software Testing and Validation - Laboratory

# Lab 6: Widget Testing with Web / Mobile

### University of Regina
### Faculty of Engineering and Applied Science - Software Systems Engineering

### Lab Instructor: [Trevor Douglas](mailto:trevor.douglas@uregina.ca)

## Introduction

Flutter provides a robust testing framework that allows developers to automate and validate various aspects of their app's behavior, including unit testing, widget testing, and integration testing. Testing in Flutter not only helps catch bugs early in the development cycle but also promotes code quality and facilitates a smoother user experience.

In this lab you will be introduced to Unit and Widget testing.

## Background

## Procedure
For the pre-lab, we are going to recreate the BMI Calculator but this time we are going to include automation testing.

![bmi mockup](res/bmi-mockup.png)

Let's start by setting up the project:

Paste this as your new main file...


<details>
<summary>expand main.dart</summary>

in `main.dart`
```dart
import 'package:flutter/material.dart';
import 'bmi.dart';

void main() {
   runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: BMI(),
    );
  }
}


```

</details>

Create `lib/bmi.dart` and paste in the following:

<details>
<summary>expand bmi.dart</summary>

```dart
import 'package:flutter/material.dart';

class BMI {

    double calculateBMI(double height, double weight) {
        double heightInCM = height;
        double weightInKg = weight;
        double heightInM = heightInCM / 100;
        double heightSquared = heightInM * heightInM;
        double result = weightInKg / heightSquared;
        return result;
    }


}
```

</details>


