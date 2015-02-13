Leeroy-Gradle
=============

leeroy.gradle adds a custom build flavor to your Android Gradle project for use with [Leeroy](https://www.github.com/Morlunk/Leeroy).

This project and the Leeroy project are both still very experimental. Use at your own risk.

How to use
----------

Include these two lines anywhere in your project's build.gradle:

    apply from: '<path to Leeroy-Gradle>/leeroy.gradle'

    setupLeeroy('<path to Leeroy-Gradle>', '<artifact regex>')

where `<path to Leeroy-Gradle>` is the path to this git repository, and `<artifact regex>` is a regular expression identifying the APK artifact on the Jenkins server to update the target project with.

When being built using the Jenkins Gradle plugin, the 'leeroy' build flavour will become available. Note that since this flavour is in its own dimension, it can be applied to other flavours thanks to the new manifest merger in modern versions of the Android Gradle plugin.

That's it! All builds of your app that use Leeroy-Gradle will be detected by the Leeroy app.
