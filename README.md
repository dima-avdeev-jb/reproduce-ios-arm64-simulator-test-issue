### Reproduce bug 

I made simple project from KMM template.  
And add FailedTest. Expect, what test task will fail.  
 - `./gradlew shared:iosX64Test` - work's as expected (FailedTest.failedTest FAILED)  
 - `./gradlew shared:iosSimulatorArm64Test` - skip test running and return success (But we expect fail!)
