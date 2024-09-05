Why can we not run an artifact transform on only one single dependency?

To repro:

1. Run `./gradlew resolveConfigurationAndHopefullyRunTransformAndThrowException`
2. If it fails, this means it has worked as expected, as we have reached the transform and thrown an exception
3. If it does not fail, Gradle is not running the transform as expected
