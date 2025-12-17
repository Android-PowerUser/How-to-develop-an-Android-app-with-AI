### App Development with AI for free


Go to [jules.google.com](https://jules.google.com) connect Jules to your GitHub account. Create a new repo or fork from another one. Let Jules create a file and folder structure for an Android app with Java Code. You can review the generated files in the `/app/` folder in the repo. You can create an Agents.md file in the root directory for programming rules that will read anytime


> ⚠️ **IMPORTANT:** Always use the planning feature in Jules (rocket icon)! AI instructions surprisingly often implement something different than intended. Good planning significantly improves LM results.


If have already code in the repo, because it is a fork, give the task to Jules. Jules analyzes the code and tells you the relevant files. Because simpler AI models (like Gemini 2.5/3 Pro) have weaknesses with complex tasks, copy these files to [lmarena.ai](https://lmarena.ai). Select "Direct" and then "Claude Opus 4.5 Thinking". Copy the task from Jules and paste it there. Paste Claude's output unchanged back into Jules. Even Gemini 2.5 Pro automatically recognizes where the code belongs and replaced the old one.


## Building the App


You can build the app directly in GitHub. For this, you need the path `/.github/workflows/manual.yml` in the Github root directory. You cannot create empty paths, but you can create multiple paths at once, plus a file. The content of the yml file must be this:


```yaml
name: Android Build

on:
 # push:
   # branches: [ main, develop ]
 # pull_request:
  #  branches: [ main ]
  workflow_dispatch:  # Ermöglicht manuelle Ausführung des Workflows

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v3

    - name: Set up JDK
      uses: actions/setup-java@v3
      with:
        java-version: '17'
        distribution: 'temurin'
        cache: gradle

    - name: Grant execute permission for gradlew
      run: chmod +x gradlew

    - name: Build with Gradle
      run: ./gradlew assembleRelease

    - name: Upload APK
      uses: actions/upload-artifact@v4
      with:
        name: app-release
        path: app/build/outputs/apk/release/app-release-unsigned.apk
```





Now you can use Github Workflows.
You need Gradle files, like in [Screen Operator](https://github.com/Android-PowerUser/ScreenOperator). You can copy them or get these from Android Studio. A fork have probably already the files.
You can build only in your fork or repo, otherwise you can't run the workflow. 1. Click on the ⚙️ gear icon (on mobile)
2. Click on **Actions**
3. Select **Android Build** (or the corresponding workflow)
4. Start the build for your branch
> ⏱️ **Duration:** approximately 5 minutes


In case of compilation errors can Gemini 2.5 Pro often fix the errors themselves, if there are no more than 5 errors. If there are much more you need Jules → Claude → Jules

In cases where you use libraries or the project has them, you may need to adjust the manual.yml.


## Cost Information

Gemini 2.5 Pro is free with a high limit 
Gemini 3 Pro is 1 month free and you can cancel the subscription before it cost anything.

