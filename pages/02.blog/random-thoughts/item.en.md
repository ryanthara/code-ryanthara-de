---
title: 'Random Thoughts'
date: '13:34 05/26/2017'
taxonomy:
    category:
        - blog
    tag:
        - journal
hide_git_sync_repo_link: false
blog_url: /blog
show_sidebar: true
show_breadcrumbs: true
show_pagination: true
hide_from_post_list: false
feed:
    limit: 10
---

A few ingredients are enough to learn programming. Typically, you start with a simple program that outputs “Hello World!” in almost every programming language.

A simple editor, the command line, ..., you can also use an integrated development environment without any frills.

In the case of JavaFX, one way is via:
* Install IntelliJ IDEA
* Install OpenJDK
* Install JavaFX

A new JavaFX project is then created and the Execute button is pressed. **Error message**

	Error: JavaFX runtime components are missing, and are required to run this application
    
The answer can be found in this [Stackoverflow post](https://stackoverflow.com/questions/52467561/intellij-cant-recognize-javafx-11-with-openjdk-11).

Before you run the default project, you just need to add these to the VM options:
    
    --module-path /Users/<user>/Downloads/javafx-sdk-11/lib --add-modules=javafx.controls,javafx.fxml

Which can also be found in the [documentation](https://openjfx.io/openjfx-docs/) of JavaFX.