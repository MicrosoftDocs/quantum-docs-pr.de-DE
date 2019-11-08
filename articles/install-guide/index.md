---
title: Installieren des Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 580ac14f2e839d723884a96e9c5fd336ebcb5da0
ms.sourcegitcommit: 30fcb35986b43388ad65dfb876eb3ad8ad0533ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2019
ms.locfileid: "73799161"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Installieren des Microsoft Quantum Development Kit (QDK)

Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können. Das QDK umfasst Folgendes:

- Programmiersprache Q#
- Bibliotheken zur Abstraktion komplexer Funktionen in Q#
- Hostanwendung (in Python oder einer .NET-Sprache geschrieben), mit der in Q# geschriebene Quantenvorgänge ausgeführt werden
- Tools für die Entwicklung

Je nach ausgewählter Entwicklungsumgebung müssen unterschiedliche Installationsschritte ausgeführt werden. Wählen Sie Ihre Umgebung in den Abschnitten unten aus.

## <a name="develop-with-python"></a>Entwickeln mit Python

Das qsharp-Paket für Python vereinfacht das Simulieren von Q#-Vorgängen und -Funktionen in Python. IQ# (ausgesprochen „aɪ-kjuː-ʃɑrp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.

1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3.6 oder höher
    - Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager
    - [.NET Core SDK 3.0 oder höher](https://www.microsoft.com/net/download)

1. Installieren Sie das Paket `qsharp`.

    ```bash
    pip install qsharp
    ```

1. Installieren Sie das Paket `iqsharp`.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - Erstellen Sie ein Python-Programm mit dem Namen `hello_world.py`, um den Q#-Vorgang `SayHello()` aufzurufen:

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - Führen Sie das Programm aus:

        ```bash
        python hello_world.py
        ```

    - Überprüfen Sie die Ausgabe. Ihr Programm sollte die folgenden Zeilen ausgeben:

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a>Entwickeln mit Jupyter-Notebooks

Jupyter Notebook ist ein beliebtes Tool in der Wissenschaft und Forschung sowie bei der onlinebasierten kollaborativen Programmierung, das sich durch direkte Codeausführung (jetzt auch für Q#-Code) auszeichnet sowie Anweisungen, Hinweise und andere Inhalte bietet.  Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.

IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.


1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3.6 oder höher
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.0 oder höher](https://www.microsoft.com/net/download)

1. Installieren Sie das Paket `iqsharp`.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:

        ```bash
        jupyter notebook
        ```

    - Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird. Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

    - Erstellen Sie ein Jupyter-Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Führen Sie diese Zelle des Notebooks aus:

        ![Zelle im Jupyter-Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

        In der Ausgabe der Zelle sollte `SayHello` angezeigt werden. Bei der Ausführung in Jupyter-Notebooks wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.


    - Simulieren Sie auf einem Quantencomputer in einer neuen Zelle die Ausführung des gerade erstellten Vorgangs mithilfe der `%simulate`-Magic:

        ![Zelle im Jupyter-Notebook mit %simulate-Magic](~/media/install-guide-jupyter-simulate.png)

        Auf dem Bildschirm sollte die Nachricht zusammen mit dem Ergebnis des von Ihnen aufgerufenen Vorgangs angezeigt werden (in diesem Fall: leer).


## <a name="develop-with-c-on-windows-using-visual-studio"></a>Entwickeln mit C# unter Windows mit Visual Studio

Visual Studio bietet eine umfangreiche Umgebung für die Entwicklung von Q#-Programmen sowie großartige Features wie Codevervollständigung und Syntaxhervorhebung, die Entwickler bei der Erstellung von Anwendungen unterstützen.  Die Q#-Erweiterung für Visual Studio enthält Vorlagen für Q#-Dateien und -Projekte sowie Syntaxhervorhebung und IntelliSense-Unterstützung.


1. Voraussetzungen

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload

1. Installieren der Q#-Erweiterung für Visual Studio

    - Herunterladen der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Hinzufügen der Erweiterung zu Visual Studio

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

## <a name="develop-with-c-using-visual-studio-code"></a>Entwickeln mit C# und Visual Studio Code

Visual Studio Code (VS Code) bietet eine umfangreiche Umgebung für die Entwicklung von Q#-Programmen in zahlreichen verschiedenen Computerumgebungen (einschließlich Windows, Linux und Mac) sowie großartige Features wie Codevervollständigung und Syntaxhervorhebung, die Entwickler bei der Erstellung von Anwendungen unterstützen.  Die Q#-VS Code-Erweiterung beinhaltet Syntaxhervorhebung und Q#-Codeausschnitte.

1. Voraussetzungen

   - [VS-Code](https://code.visualstudio.com/download)
   - [.NET Core SDK 3.0 oder höher](https://www.microsoft.com/net/download)

1. Installieren der VS Code-Erweiterung für Quantum

    - Installieren Sie die [VS Code-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Installieren Sie die Quantum-Projektvorlagen:

   - Navigieren Sie zu **Ansicht** -> **Befehlspalette**.
   - Wählen Sie **Q#: Install project templates** (Q#: Projektvorlagen installieren) aus.

    Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Erstellen eines neuen Projekts:

        - Navigieren Sie zu **Ansicht** -> **Befehlspalette**.
        - Wählen Sie **Q#: Create New Project** (Q#: Neues Projekt erstellen) aus.
        - Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.
        - Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).

    - Führen Sie die Anwendung aus.

        - Navigieren Sie zu **Debuggen** -> **Ohne Debuggen starten**.
        - Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.

> [!NOTE]
> * > * Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a>Entwickeln mit C# per Befehlszeilentool `dotnet`

Natürlich können Sie Q#-Programme auch über die Befehlszeile erstellen und ausführen, indem Sie einfach das .NET Core SDK und die QDK-Projektvorlagen installieren. 

1. Voraussetzungen

    - [.NET Core SDK 3.0 oder höher](https://www.microsoft.com/net/download)

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
