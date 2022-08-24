### Reproduce bug 

I made simple project from KMM template.  
And add FailedTest. Expect, what test task will fail.  

 - `./gradlew shared:iosX64Test -i` - work's as expected (test FailedTest.failedTest FAILED)  
 - `./gradlew shared:iosSimulatorArm64Test -i` - Task :shared:iosSimulatorArm64Test SKIPPED (But we expect runs and fail)

Also, we have explored that onlyIf{} conditions in iosSimulatorArm64Test task returns false

