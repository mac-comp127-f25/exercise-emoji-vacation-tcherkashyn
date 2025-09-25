Upgrade steps for Java 21

Goal: Configure this project to use Java 21 (LTS) via Gradle toolchain and verify a local JDK 21 is available.

What changed in the project:
- `build.gradle` now configures a Gradle Java toolchain requesting Java 21 and sets `sourceCompatibility`/`targetCompatibility` to Java 21.

Local steps to finish the upgrade (Windows / PowerShell):

1) Install a JDK 21 if you don't have one. Two convenient options:
   - Adoptium / Temurin (recommended):
     - Visit https://adoptium.net and download the Windows x64 JDK 21 installer and run it.
   - Or use a package manager like chocolately (if installed):
     - choco install temurin-21-jdk -y

2) Make sure JAVA_HOME points to the JDK 21 installation and is on PATH (PowerShell):

   $env:JAVA_HOME = 'C:\Program Files\Eclipse Adoptium\jdk-21' ; $env:Path = $env:JAVA_HOME + '\bin;' + $env:Path

   (Adjust the path to match your installation.)

3) Build the project with Gradle. If this repo doesn't include a Gradle wrapper you can use your system gradle. Example (PowerShell):

   # using gradle wrapper if available
   .\gradlew.bat build

   # or using system gradle
   gradle build

Gradle will download a matching JDK if toolchain cannot find a local JDK. If you prefer Gradle to always use the local JDK, configure `org.gradle.java.home` in `gradle.properties` to point to your JDK 21 installation.

Notes:
- If your Gradle version is old and doesn't support toolchains, update Gradle or use `org.gradle.java.home` instead.
- I couldn't call the Copilot upgrade planner in this environment because that feature requires a Copilot Pro plan. I updated `build.gradle` directly to request Java 21.

If you'd like, I can:
- Add a `gradle.properties` file with `org.gradle.java.home` set (you must provide the local JDK path), or
- Download and install a JDK 21 into the workspace automatically (requires permission to run installers), or
- Update or add a Gradle wrapper to a newer Gradle version that fully supports toolchains.