#SOLVED
I have used X64 JDK,
after switch to amd64 JDK all work's fine! (like this one: 11.0.14+9-LTS (arm64) "BellSoft")

### Reproduce bug with iosSimulatorArm64Test skipped
Issue: https://youtrack.jetbrains.com/issue/KT-53702/gradle-task-iosSimulatorArm64Test-skipped  

Reproduced on Apple Silicone Mac's  
I made simple project from KMM template.  
And add FailedTest. Expect, what test task will fail.  

 - `./gradlew shared:iosX64Test -i` - work's as expected (test FailedTest.failedTest FAILED)  
 - `./gradlew shared:iosSimulatorArm64Test -i` - Task :shared:iosSimulatorArm64Test SKIPPED (But we expect runs and fail)

Also, we have explored that onlyIf{} condition in iosSimulatorArm64Test task returns false

