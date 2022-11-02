The Millicast Java SDK for Android is hosted on this Maven repository.

# Millicast Java SDK for Android
- This can be used in an Android project to publish/subscribe to/from the Millicast Platform.
- The list of [versions](https://github.com/millicast/Maven/packages/1217522/versions) hosted on this Maven repository.
- The AAR and Javadoc files are also available for download [here](https://github.com/millicast/millicast-native-sdk/releases).

# Installing the SDK via Maven from GitHub Packages
## Pre-requisites:
- A valid GitHub account with a **personal access token (PAT)** with a `read:packages` scope.
- The following articles provide more information on how to create and use a PAT:
  - [Creating a personal access token
](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
  - [Working with the Gradle registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-gradle-registry)

## Adding the SDK via Gradle
- Maven details:
   - Url: https://maven.pkg.github.com/millicast/maven
   - Group ID: com.millicast
   - Artifact ID: millicast-sdk-android
- In your Android project's ***app/build.gradle***, add:
  - A maven repository for the Millicast Maven on GitHub Packages
    - For example:
      ``` gradle
      repositories {
          // Millicast SDK via Maven from GitHub Packages
          maven {
              name = "GitHubPackages"
              url = uri("https://maven.pkg.github.com/millicast/maven")
              credentials {
                  username = githubUsername
                  password = githubPat
              }
          }
      }
      ```
    - Where:
	  - `githubUsername`
		- The **username** of the GitHub account to use.
	  - `githubPat`
		- GitHub user's **personal access token (PAT)** with a `read:packages` scope.
  - A dependency line to use the Millicast SDK
    - To use the latest version of Millicast SDK:
      ``` gradle
      dependencies {
          implementation 'com.millicast:millicast-sdk-android'
      }
      ```
    - To use a specific version of Millicast SDK, for example 1.4.0:
      ``` gradle
      dependencies {
          implementation 'com.millicast:millicast-sdk-android:1.4.0'
      }
      ```
- For an example, you may refer to the [***app/build.gradle***](https://github.com/millicast/Millicast-Java-SDK-Android-Sample-App-in-Java/blob/master/app/build.gradle) of the [Millicast Java SDK Android Sample App](https://github.com/millicast/Millicast-Java-SDK-Android-Sample-App-in-Java).

# Using the SDK
The following resources provide more information on the usage of the SDK:
- SDK [documentation](https://millicast.github.io/doc/java/com/millicast/package-summary.html).
- Dolby.io Real-time Streaming [documentation](https://docs.dolby.io/streaming-apis/docs).
- The [Millicast Java SDK Android Sample App](https://github.com/millicast/Millicast-Java-SDK-Android-Sample-App-in-Java) provides more information and examples on SDK usage.
