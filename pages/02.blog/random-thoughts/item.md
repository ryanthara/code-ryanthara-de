---
title: 'IntelliJ, OpenJDK, JavaFX und Hello World!'
date: '06:00 10/10/2024'
taxonomy:
    category:
        - blog
    tag:
        - JavaFX
        - IntelliJ
hide_git_sync_repo_link: false
blog_url: /blog
show_sidebar: true
show_breadcrumbs: true
show_pagination: true
hide_from_post_list: false
feed:
    limit: 10
---

Wenige Zutaten reichen um das Programmieren zu lernen. Typischerweise beginnt man in fast jeder Programmiersprache mit einem einfachen Programm, welches „Hello World!“ ausgibt.

Hierzu genügt ein einfacher Editor, die Kommandozeile, ..., man kann auch schnörkellos eine integrierte Entwicklungsumgebung dazu benutzen.

Im Fall von JavaFX führt ein Weg über:
* IntelliJ IDEA installieren
* OpenJDK installieren
* JavaFX installieren

Anschließend wird ein neues JavaFX-Projekt angelegt und die Ausführen-Taste gedrückt. **Fehlermeldung**

	Error: JavaFX runtime components are missing, and are required to run this application
    
Die Antwort steckt in diesem [Stackoverflow-Beitrag](https://stackoverflow.com/questions/52467561/intellij-cant-recognize-javafx-11-with-openjdk-11).

	Before you run the default project, you just need to add these to the VM options:
    --module-path /Users/<user>/Downloads/javafx-sdk-11/lib --add-modules=javafx.controls,javafx.fxml

Was übrigens auch in der [Dokumentation](https://openjfx.io/openjfx-docs/) von JavaFX zu finden ist.