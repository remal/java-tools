

<!-- toc -->

- [Tools/approaches for Java projects](#toolsapproaches-for-java-projects)
  * [Common](#common)
  * [Local environment](#local-environment)
    + [Inbox Zero](#inbox-zero)
    + [Total Commander](#total-commander)
    + [Notepad++](#notepad)
    + [Intellij IDEA](#intellij-idea)
      - [Jetbrains Toolbox](#jetbrains-toolbox)
      - [Jetbrains Mono](#jetbrains-mono)
      - [IDEA plugins](#idea-plugins)
      - [IDEA required plugins for the project](#idea-required-plugins-for-the-project)
  * [Code repository](#code-repository)
    + [.gitignore file](#gitignore-file)
    + [.gitattributes file](#gitattributes-file)
    + [EditorConfig](#editorconfig)
    + [Renovate](#renovate)
    + [Dependabot](#dependabot)
    + [Branching strategy](#branching-strategy)
  * [Java & JVM languages](#java--jvm-languages)
    + [Gradle](#gradle)
    + [Maven](#maven)
      - [Maven wrapper](#maven-wrapper)
  * [Testing](#testing)
    + [Test Pyramid](#test-pyramid)
    + [JUnit 5](#junit-5)
    + [Mockito](#mockito)
    + [Testcontainers](#testcontainers)
    + [Spring Cloud Contract](#spring-cloud-contract)
    + [PIT Mutation Testing](#pit-mutation-testing)
  * [Static analysis](#static-analysis)
    + [Checkstyle](#checkstyle)
    + [SonarQube](#sonarqube)
    + [Nullity annotations](#nullity-annotations)
  * [Spring Framework](#spring-framework)
  * [Libraries](#libraries)
    + [Lombok](#lombok)
  * [Immutables](#immutables)
  * [Hibernate Validator](#hibernate-validator)
  * [Mapstruct](#mapstruct)
  * [Flyway](#flyway)
  * [Liquibase](#liquibase)

<!-- tocstop -->

# Tools/approaches for Java projects

## Common

* (:ru:) "Что такое Работающий Продукт и как его делать": https://www.youtube.com/watch?v=KwPrt17wcZs

## Local environment

### Inbox Zero

An approach to email management aimed at keeping the inbox empty.

* https://whatis.techtarget.com/definition/inbox-zero
* https://www.entrepreneur.com/article/290175

### Total Commander

A file manager for Windows.

* https://www.ghisler.com/

### Notepad++

A free source code editor and Notepad replacement that supports several languages.

* https://notepad-plus-plus.org/
* EditorConfig plugin: https://github.com/editorconfig/editorconfig-notepad-plus-plus

### Intellij IDEA

#### Jetbrains Toolbox

Install and update Jetbrains tools easily.

* https://www.jetbrains.com/toolbox-app/

#### Jetbrains Mono

A font for developers.

* https://www.jetbrains.com/lp/mono/

#### IDEA plugins

* Lombok: https://plugins.jetbrains.com/plugin/6317-lombok
* Maven Wrapper (for IDEA versions **below** 2020.2): https://plugins.jetbrains.com/plugin/10160-maven-wrapper-intellij-idea-plugin
* Laconic POM: https://plugins.jetbrains.com/plugin/10580-laconic-pom
* .ignore: https://plugins.jetbrains.com/plugin/7495--ignore
* Advanced Java Folding: https://plugins.jetbrains.com/plugin/9320-advanced-java-folding
* Checkstyle-IDEA: https://plugins.jetbrains.com/plugin/1065-checkstyle-idea
* SonarLint: https://plugins.jetbrains.com/plugin/7973-sonarlint
* Save actions: https://plugins.jetbrains.com/plugin/7642-save-actions

#### IDEA required plugins for the project

How to set plugins that are required for the project. This configuration can be shared within the team and IDEA will notify developers if they miss some plugins.

* https://www.jetbrains.com/help/idea/settings-required-plugins.html

## Code repository

### .gitignore file

Specifies intentionally untracked files to ignore

* https://git-scm.com/docs/gitignore
* https://github.com/github/gitignore
* .gitignore for Jetbrains products (most of IDE settings are commited): https://github.com/github/gitignore/blob/master/Global/JetBrains.gitignore

### .gitattributes file

Git attributes per path.

* https://git-scm.com/docs/gitattributes
* https://github.com/alexkaratarakis/gitattributes
* https://dev.to/deadlybyte/please-add-gitattributes-to-your-git-repository-1jld

### EditorConfig

EditorConfig helps maintain consistent coding styles for multiple developers working on the same project across various editors and IDEs

* https://editorconfig.org/
* IDEA code style can be managed from EditConfig: https://blog.jetbrains.com/idea/2019/06/managing-code-style-on-a-directory-level-with-editorconfig/

### Renovate

Automated dependency updates. Supports http://github.com/, https://gitlab.com/, https://bitbucket.org/.

* https://renovate.whitesourcesoftware.com/

### Dependabot

Automated dependency updates for http://github.com/.

* https://docs.github.com/en/github/managing-security-vulnerabilities/configuring-github-dependabot-security-updates

### Branching strategy

* GitFlow: https://medium.com/@okandavut/what-is-gitflow-c0be7a659992
* GitHub flow: https://guides.github.com/introduction/flow/

## Java & JVM languages

* (:ru:) "Как нам спасти Java": https://www.youtube.com/watch?v=TSAlj04_tkA + https://www.youtube.com/watch?v=cPXTozVjSHo
* Javac params: https://docs.oracle.com/en/java/javase/11/tools/javac.html
* JPMS
  * Split Packages issue: https://www.logicbig.com/tutorials/core-java-tutorial/modules/split-packages.html

### Gradle

Build tool

* https://gradle.org/
* Plugins: https://plugins.gradle.org/

### Maven

Build tool

* https://maven.apache.org/

#### Maven wrapper

The Maven Wrapper is an easy way to ensure a user of your Maven build has everything necessary to run your Maven build.

* https://github.com/takari/maven-wrapper
* http://jakub.marchwicki.pl/posts/2015/06/04/maven-wrapper/
* IDEA natively supports Maven Wrapper from 2020.2: https://blog.jetbrains.com/idea/2020/05/intellij-idea-2020-2-early-access-program-is-starting/

## Testing

### Test Pyramid

![Test Pyramid](https://martinfowler.com/articles/practical-test-pyramid/testPyramid.png)

* https://martinfowler.com/articles/practical-test-pyramid.html

### JUnit 5

* https://junit.org/junit5/docs/current/user-guide/
* Migration from JUnit 4: https://junit.org/junit5/docs/current/user-guide/#migrating-from-junit4

### Mockito

* https://site.mockito.org/
* Mocking a final class: https://www.baeldung.com/mockito-final

### Testcontainers

* https://www.testcontainers.org/

### Spring Cloud Contract

* https://spring.io/projects/spring-cloud-contract

### PIT Mutation Testing

* https://pitest.org/
* Gradle plugin: https://gradle-pitest-plugin.solidsoft.info/

## Static analysis

### Checkstyle

* https://checkstyle.sourceforge.io/
* Checkstyle-IDEA plugin: https://plugins.jetbrains.com/plugin/1065-checkstyle-idea

### SonarQube

* https://www.sonarqube.org/
* SonarLint plugin: https://plugins.jetbrains.com/plugin/7973-sonarlint

### Nullity annotations

* https://www.jetbrains.com/help/idea/inferring-nullity.html
* Spring Null-Safety Annotations: https://www.baeldung.com/spring-null-safety-annotations, https://docs.spring.io/spring/docs/5.2.9.RELEASE/spring-framework-reference/core.html#null-safety
* Spring Data null-safety: https://docs.spring.io/spring-data/commons/docs/current/reference/html/#repositories.nullability.annotations

## Spring Framework

* https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-external-config-vs-value
* https://www.baeldung.com/configuration-properties-in-spring-boot
* https://docs.spring.io/spring-boot/docs/current/reference/html/appendix-configuration-metadata.html#configuration-metadata-annotation-processor
* https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-2.0-Migration-Guide#configuration-properties-migration

## Libraries

### Lombok

* https://projectlombok.org/
* https://projectlombok.org/features/configuration
* https://github.com/rzwitserloot/lombok/issues/2044

### Immutables

Java annotation processors to generate simple, safe and consistent value objects

* https://immutables.github.io/

### Hibernate Validator

* https://hibernate.org/validator/
* https://docs.jboss.org/hibernate/validator/7.0/reference/en-US/html_single/#validator-annotation-processor
* https://beanvalidation.org/2.0/

### Mapstruct

Java mapper library

* https://mapstruct.org/
* https://mapstruct.org/documentation/dev/reference/html/#mapping-with-constructors
* https://mapstruct.org/documentation/dev/reference/html/#mapping-with-builders

### Flyway

Database migrations tool

* https://flywaydb.org/

### Liquibase

Database migrations tool

* https://www.liquibase.org/
