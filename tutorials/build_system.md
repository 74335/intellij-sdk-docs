---
title: Building Plugins with Gradle
---
<!-- Copyright 2000-2020 JetBrains s.r.o. and other contributors. Use of this source code is governed by the Apache 2.0 license that can be found in the LICENSE file. -->

The [gradle-intellij-plugin](https://github.com/JetBrains/gradle-intellij-plugin) Gradle plugin is the recommended solution for building IntelliJ plugins. 
The plugin takes care of the dependencies of your plugin project - both the base IDE and other plugin dependencies.

If a new plugin will be Scala-based, a plugin development workflow [sbt-idea-plugin](https://github.com/JetBrains/sbt-idea-plugin), is available.
The workflow is analogous to the Gradle workflow but tailored to developing IntelliJ Platform plugins in Scala.
JetBrains does not officially support this Scala workflow, and at this time the workflow has only minimal documentation.

The gradle-intellij-plugin provides tasks to run the IDE with your plugin and to publish your plugin to the [JetBrains plugins repository](/plugin_repository/index.md). 
To make sure that your plugin is not affected by [API changes](/reference_guide/api_changes_list.md) which may happen between major releases of the platform, you can easily build your plugin against many versions of the base IDE.

> **WARNING** When adding additional repositories to your Gradle build script, make sure to always use HTTPS protocol.

> **Note** Please make sure to always upgrade to the latest version of `gradle-intellij-plugin`.
Follow releases on [GitHub](https://github.com/JetBrains/gradle-intellij-plugin/releases). 
 
Below are a series of guides to developing and deploying Gradle-based IntelliJ Platform Plugins:  
*  [1. Getting Started with Gradle-Based Plugins](build_system/prerequisites.md)
*  [2. Configuring Gradle-Based Plugins](build_system/gradle_guide.md)
*  [3. Deploying a Plugin with Gradle](build_system/deployment.md)
