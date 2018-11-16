# idea-gradle-source-sets-bug

Reproduction of the IDEA Gradle Source Sets bug https://youtrack.jetbrains.com/issue/IDEA-202337.

Steps to Reproduce:

1. Open IntelliJ IDEA
1. File -> Open
1. Select the project directory
1. Run the `BarTest` configuration

Actual:

```
Error:(9, 9) java: cannot find symbol
  symbol:   variable Foo
  location: class com.example.BarTest
```

Expected:

```
foo
```

Comments:

Run the `idea-gradle-source-sets-bug [integrationTest]` configuration and see that Gradle is able to run the test.
