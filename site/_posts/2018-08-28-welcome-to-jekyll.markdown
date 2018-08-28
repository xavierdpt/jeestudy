---
layout: post
title:  "JEE Study #1: Java and Eclipse Setup on Windows 10"
date:   2018-08-28 17:19:35 +0200
categories: jee servlets
---
Hi guys !

In this session, we install the Java 10 Development Kit (JDK) and Eclipse Photon on Windows 10. The JDK is necessary for developing Java EE applications, and Eclipse is one popular Java IDE.

# Java

**Some practice**

Look for `Java Development Kit 10` on the web.

Get the file `?`.

During installation, I usually omit the "Public JRE", which is not strictly necessary.

Done.

**Some discussion**

The reason why I usually omit the "Public JRE" is because I ran into cases where the "Public JRE" updated itself, while the JDK remained on the same version. This lead to very confusing issues, where different pieces of software where using different version of almost the same thing. Disabling the Public JRE and using only one JDK ensures that everything is using the same version of Java.

# Eclipse

**Some practice**

Look for `eclipse` on the web.

You should end up with the Windows x64 Installer.

Upon first execution, you may have to update the installer.

The choose the "Eclipse IDE for Java EE Developer" in the list.

Done.

# Sample maven project

**Some practice**

Start the "new maven project" wizard.

Make sure "Create a simple project" is checked.

You can choose to put the project files in a location external to the workspace.

In the next page of the wizard, enter the following information:

* Group Id : `example.company`
* Artifact Id : `myproject`
* Version : `0.0.0`

Click on "Finish".

Create a new class named `example.company.myproject.Main`.

Add a main method which outputs "Hello Word !" to the console.

Run it.

**Some discussion**

RFC 6761 reserves the `example` top level domain name for examples. We use this to make the projects in this serie live in the fictitious `company.example` website. We also use version `0.0.0` everywhere to denote the fact that the projects in this serie are not versioned at all.

Eclipse adds the `.settings`, `target`, `.classpath` and `.project` to Maven projects, and these files cache information derived from the `pom.xml`. Some changes to `pom.xml` thus require removing the project from eclipse, then removing these files, and importing the project into Eclipse again to have the changes be taken into account.
