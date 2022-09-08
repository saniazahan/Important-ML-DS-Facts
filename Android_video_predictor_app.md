## Workflow
- First create an android app that has a upload button
- Need an account on AWS
   sign up for an AWS account and create an AWS Identity and Access Management (IAM) admin user
https://docs.aws.amazon.com/sagemaker/latest/dg/gs-set-up.html
  
- Amazon S3 bucket is used to store data for training and testing  
  Follow the below tutorials
- AWS amplify 
 
## Configfure amplify following the commands in the video section
   https://www.youtube.com/watch?v=hyFmtK0OjfI
   Amplify Libraries
   https://docs.amplify.aws/lib/q/platform/android/
   
   After initializing amplify in the project directory follow the below instructions
   
   Under Gradle Scripts, open build.gradle (Module: AppName).

   Add the following lines:
   ```
   android {
    compileOptions {
        // Support for Java 8 features
        coreLibraryDesugaringEnabled true
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
      }
   }
   
   dependencies {
    // Amplify core dependency
    implementation 'com.amplifyframework:core:1.36.5-dev-preview.0'

    // Support for Java 8 features
    coreLibraryDesugaring 'com.android.tools:desugar_jdk_libs:1.1.5'
   }
   ```
   

   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
  
  ### Choose File and Upload to Firebase Storage - Android Kotlin
  https://www.youtube.com/watch?v=j11O6DvkePg

  ### AWS - Uploading a File To S3 - Android Kotlin
  https://www.youtube.com/watch?v=qgrXMzFMHx4
  


Bring your own model on AWS Sagemaker
https://aws.amazon.com/blogs/machine-learning/bring-your-own-model-with-amazon-sagemaker-script-mode/
https://aws.amazon.com/blogs/machine-learning/bring-your-own-deep-learning-framework-to-amazon-sagemaker-with-model-server-for-apache-mxnet/




## Kotlin coroutines on Android
A coroutine is a concurrency design pattern that you can use on Android to simplify code that executes asynchronously.
https://developer.android.com/kotlin/coroutines
