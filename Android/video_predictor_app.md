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
  One of the dependencies uses the kotlin version of the viewmodel library whereas the code uses the java version. Specify both to enforce the latest version for all dependencies:
   
   ```
   def lifecycle_version = "2.4.0"
   implementation "androidx.lifecycle:lifecycle-viewmodel:$lifecycle_version"
   implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version"
   ```
   
   for access to S3 bucket and authentication
   ```
   def amplify_version = "1.36.5"
   implementation "com.amplifyframework:aws-storage-s3:$amplify_version"
   implementation "com.amplifyframework:aws-auth-cognito:$amplify_version"
   ```
   Now sync gradle, it will download all the necessary libraries
   
   Add the following the function in MainActivity   
   ```
   private fun configureAmplify(){
        // function to configure amplify and add the authentications
        try {
            Amplify.addPlugin(AWSCognitoAuthPlugin())
            Amplify.addPlugin(AWSS3StoragePlugin())
            Amplify.configure(applicationContext)
            Log.i("AssistMe", "Initialized amplify")
        } catch (error: AmplifyException){
            Log.i("AssistMe", "Could not initialize Amplify", error)
        }
    }
   ```
   
   Add the call in onCreate function
   ```
   configureAmplify()
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
