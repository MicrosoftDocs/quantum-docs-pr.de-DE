---
title: 'Entwickeln mit Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 1fd829c684502092bb7491b0f46b5f690320c941
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831017"
---
# <a name="develop-with-q--c"></a>Entwickeln mit Q # +C#

Installieren Sie das QDK, C# um Host Programme zum Abrufen von Q #-Vorgängen zu entwickeln.

Q # ist speziell für .NET-Sprachen konzipiert, insbesondere C#. Sie können mit dieser Kopplung innerhalb verschiedener Entwicklungsumgebungen arbeiten:

- [F # und C# Verwendung von Visual Studio (Windows)](#VS)
- [Q # + C# Verwenden von Visual Studio Code (Windows, Linux und Mac)](#VSC)
- [Q # + C# mit dem Befehlszeilen Tool "`dotnet`"](#command)

## Entwickeln mit Q # + C# mithilfe von Visual Studio<a name="VS"></a>

Visual Studio bietet eine umfangreiche Umgebung für die Entwicklung von f #-Programmen. Die f # Visual Studio-Erweiterung enthält Vorlagen für Q #-Dateien und-Projekte sowie Syntax Hervorhebung, Codevervollständigung und IntelliSense-Unterstützung.


1. Voraussetzungen

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload

1. Installieren der Q#-Erweiterung für Visual Studio

    - Herunterladen und Installieren der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Erstellen einer neuen Q#-Anwendung

        - Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.
        - Geben Sie im Suchfeld als Suchbegriff `Q#` ein.
        - Wählen Sie **Q#-Anwendung** aus.
        - Wählen Sie **Weiter** aus.
        - Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.
        - Klicken Sie auf **Erstellen**

    - Untersuchen des Projekts

        Es sollten zwei Dateien erstellt worden sein: `Driver.cs` (C#-Hostanwendung) und `Operation.qs` (Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung auf der Konsole definiert wird).

    - Ausführen der Anwendung

        - Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.
        - Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.

> [!NOTE]
> * Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.  

## Entwickeln mit Q # + C# mit Visual Studio Code<a name="VSC"></a>

Visual Studio Code (vs Code) bietet eine umfangreiche Umgebung für die Entwicklung von Q #-Programmen unter Windows, Linux und Mac.  Die q # vs Code-Erweiterung bietet Unterstützung für die f #-Syntax Hervorhebung, Codevervollständigung und f #-Code Ausschnitte.

1. Voraussetzungen

   - [VS-Code](https://code.visualstudio.com/download)
   - [.Net Core SDK 3,1 oder höher](https://www.microsoft.com/net/download)

1. Installieren der VS Code-Erweiterung für Quantum

    - Installieren Sie die [VS Code-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Installieren Sie die Quantum-Projektvorlagen:

   - Navigieren Sie zu **Ansicht** -> **Befehlspalette**.
   - Auswählen von " **Q #: Install Project Templates** "

    Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Erstellen eines neuen Projekts:

        - Navigieren Sie zu **Ansicht** -> **Befehlspalette**.
        - Wählen Sie **Q #: Neues Projekt erstellen** aus.
        - **Eigenständige Konsolenanwendung** auswählen
        - Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.
        - Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).

    - Wenn Sie die C# Erweiterung für vs Code nicht bereits installiert haben, wird ein Popup Fenster angezeigt. Installieren Sie die Erweiterung. 

    - Führen Sie die Anwendung aus.

        - Zum **Terminal** -> **neuen Terminal** wechseln
        - Geben Sie `dotnet run` ein.
        - Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.


> [!NOTE]
> * Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

## Entwickeln mit Q # + C# mit dem `dotnet`-Befehlszeilen Tool<a name="command"></a>

Natürlich können Sie Q#-Programme auch über die Befehlszeile erstellen und ausführen, indem Sie einfach das .NET Core SDK und die QDK-Projektvorlagen installieren. 

1. Voraussetzungen

    - [.Net Core SDK 3,1 oder höher](https://www.microsoft.com/net/download)

1. Installieren der Quantum-Projektvorlagen für .NET

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Erstellen einer neuen Anwendung

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - Navigieren Sie zum neuen Anwendungsverzeichnis.

       ```bash
       cd runSayHello
       ```

    Es sollten zwei Dateien und die Projektdateien der Anwendung erstellt worden sein: eine Q#-Datei (`Operation.qs`) und eine C#-Hostdatei (`Driver.cs`).

    - Ausführen der Anwendung

        ```bash
        dotnet run
        ```

        Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`.

    
## <a name="whats-next"></a>Wie geht es weiter?

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.
