# Task:
Creating a Build Farm

The goal of the task is to create a build farm for a simple application with running tests and release generation.
Write a program that outputs two lines to the console:

```
build N
Hello, World!
```

where N should be the current build number. During the build stage, run tests to verify the validity of the version number. Upload the source code to a repository on GitHub.
Configure a GitHub Actions workflow to automatically build the project on every commit. Also, set up automatic release generation either on every commit or upon tag creation.

# Self-check:
* The package version increases from build to build.
* The current version is displayed in the welcome message.
* The helloworld package containing the executable file helloworld is published as a release in the repository.

# Verification:

The task is considered successfully completed if, after installing the package downloaded from the release: apt update && apt install -y helloworld-0.0.X-Linux.deb
(where X is the build number), and running the binary file: helloworld_cli the following message appears:

```
Version: X
Hello, World!
```

(where X is, again, the build number).
