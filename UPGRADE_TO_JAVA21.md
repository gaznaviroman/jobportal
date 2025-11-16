Upgrade notes — Java 21

What I changed
- Updated `<java.version>` in `pom.xml` from `17` to `21` so the project will compile targeting Java 21.

What you must do locally
1. Install JDK 21 (Adoptium/Temurin or other vendor).
   - macOS (Homebrew example):
     - `brew install temurin21` or use your preferred installer.
2. Make sure your `JAVA_HOME` points to the JDK 21 installation. Example (bash):
   - `export JAVA_HOME=$(/usr/libexec/java_home -v21)`
   - Verify with `java -version`.
3. Build and test the project:
   - `./mvnw -v` (verify Maven and Java)
   - `./mvnw -DskipTests package` (quick build)
   - `./mvnw test` (run tests when ready)

Notes & troubleshooting
- Spring Boot parent is `3.5.6` in this project. Spring Boot 3.5.x series is intended to support modern Java versions; if you hit compatibility issues, consider upgrading Spring Boot as a separate step.
- If you use an IDE (IntelliJ, VS Code), update the project's SDK/JDK to Java 21 in the IDE settings and refresh the Maven project.
- If compilation failures occur after this change, share the build output and I can help triage dependency or code issues.

Next steps I can take for you
- Run the build here (I will run `./mvnw -DskipTests package` now and report results).
- If build fails, I can apply minimal changes to fix compile errors (if they're straightforward).
- Optionally bump Spring Boot to a newer patch in 3.5.x if needed.

If you'd like me to proceed with the build now, say "go ahead and build" or I'll run it automatically.
