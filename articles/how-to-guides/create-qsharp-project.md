---
title: 'Erfahren Sie, wie Sie ein Q #-Projekt mit dem Quantum Development Kit (QDK) erstellen.'
description: 'Initialisieren eines Projekts für die Quantum-Entwicklung mit dem QDK und f # in der von Ihnen ausgewählten Entwicklungsumgebung'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: 8af8e3288aab731520ede984d5f89644de292385
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578210"
---
# <a name="create-a-q-project-in-your-development-environment"></a>Erstellen eines Q #-Projekts in Ihrer Entwicklungsumgebung

Erfahren Sie, wie Sie ein Q #-Projekt mit dem QDK erstellen.

Ein q #-Projekt enthält q #-Dateien, die den Quantum-Code enthalten, sowie ein Host Programm zum Ausführen des Quantum-Programms. Sie können das Host Programm in .NET-Sprachen schreiben, z. b. in c# oder in Python. Sie können auch Q #-Code in einer Jupyter Notebook ausführen, indem Sie den IQ #-Kernel verwenden.

Wählen Sie in den folgenden Abschnitten Ihre Entwicklungsumgebung und Sprache aus:

* [Python](#create-a-python-project)
* [Jupyter Notebook-Instanzen in Q#](#create-a-q-jupyter-notebook-project)
* [C# mit Visual Studio](#create-a-c-project-on-windows-using-visual-studio)
* [C# mit vs Code](#create-a-c-project-using-vs-code)
* [C# mit der Befehlszeile](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a>Erstellen eines Python-Projekts

1. Voraussetzungen

     * Installieren des [quantumentwicklungskit für python](xref:microsoft.quantum.install.python)

1. Erstellen Sie einen Ordner für das Projekt, und navigieren Sie zu diesem Ordner.

1. Erstellen Sie eine q #-Datei mit dem Namen `Operation.qs` , und fügen Sie Ihr den q #-Code hinzu. Beispiel:

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. Erstellen Sie eine python-Hostdatei namens `host.py` , um den Q #-Vorgang aufzurufen. Beispiel:

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. Führen Sie das Programm aus:

    ```
    python host.py
    ```

1. Überprüfen Sie die Ausgabe. Ihr Programm sollte die folgenden Zeilen ausgeben:

    ```
    Hello from quantum world!
    0
    ```

Sie können nun mit der Entwicklung des Quantums Programm fortfahren.

## <a name="create-a-q-jupyter-notebook-project"></a>Erstellen eines Q # Jupyter Notebook-Projekts

1. Voraussetzungen

    * Installieren des [quantumentwicklungskit für jupyter-Notebooks](xref:microsoft.quantum.install.jupyter)

1. Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:

    ```
    jupyter notebook
    ```

1. Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird. Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]

1. Eine jupyter-Seite wird im Browser angezeigt. Wählen Sie auf der Registerkarte **Dateien** die Option **New**  >  **Q #** aus, um eine Jupyter Notebook mit einem Q #-Kernel zu erstellen. Fügen Sie den folgenden Code in die erste Notebook-Zelle ein:

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. Wählen Sie **Zelle**Zellen  >  **Ausführen** aus, um das Notebook auszuführen. `SayHello`wird in Kürze in der Zellen Ausgabe angezeigt:

    ![Jupyter Notebook Zelle mit Q #-Code](~/media/install-guide-jupyter.png)

    Bei der Ausführung in jupyter-Notebooks wird der Q #-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.

1. Simulieren Sie auf einem Quantencomputer in einer neuen Zelle die Ausführung des gerade erstellten Vorgangs mithilfe der `%simulate`-Magic:

    ![Jupyter Notebook Zelle mit "% simulieren" Magic](~/media/install-guide-jupyter-simulate.png)

    Auf dem Bildschirm sollte die Nachricht zusammen mit dem Ergebnis des von Ihnen aufgerufenen Vorgangs angezeigt werden (in diesem Fall: leer).

Sie können jetzt weitere Q #-Vorgänge hinzufügen, um die Quantum-Entwicklung fortzusetzen.

## <a name="create-a-c-project-on-windows-using-visual-studio"></a>Erstellen eines c#-Projekts unter Windows mit Visual Studio

1. Voraussetzungen

    * Installieren der [Quantum Development Kit-Erweiterung für Visual Studio](xref:microsoft.quantum.install.cs)

1. Erstellen einer neuen Q#-Anwendung

    * Wechseln Sie zu **Datei**  ->  **Neues**  ->  **Projekt** .
    * Geben Sie im Suchfeld als Suchbegriff `Q#` ein.
    * Wählen Sie **Q#-Anwendung** aus.
    * Wählen Sie **Weiter** aus.
    * Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.
    * Klicken Sie auf **Erstellen**

1. Untersuchen des Projekts

    Es sollten zwei Dateien erstellt worden sein: `Driver.cs` (C#-Hostanwendung) und `Operation.qs` (Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung auf der Konsole definiert wird).

1. Ausführen der Anwendung

    * **Debuggen**  ->  **Starten ohne Debugging** auswählen
    * Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.

Sie können jetzt die Quantum-Entwicklung mit Visual Studio fortsetzen.

> [!NOTE]
> * Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.  

## <a name="create-a-c-project-using-vs-code"></a>Erstellen eines c#-Projekts mit vs Code

1. Voraussetzungen

    * Installieren Sie die [Quantum Development Kit-Erweiterung für vs Code](xref:microsoft.quantum.install.cs)

1. Erstellen eines neuen Projekts:

    * Gehe zu **Anzeige**-  ->  **Befehls Palette**
    * Wählen Sie **Q #: Neues Projekt erstellen** aus.
    * **Eigenständige Konsolenanwendung** auswählen
    * Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.
    * Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).

1. Führen Sie die Anwendung aus.

    * Zum **Terminal**  ->  **neuen Terminal** wechseln
    * Geben Sie `dotnet run` ein.
    * Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.

Nun können Sie die Quantum-Entwicklung mit Visual Studio Code fortsetzen.

> [!NOTE]
> * Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a>Erstellen eines c#-Projekts mit dem `dotnet` Befehlszeilen Tool

1. Voraussetzungen

    * Installieren des [quantumentwicklungskit für die Befehlszeile](xref:microsoft.quantum.install.standalone)

1. Erstellen einer neuen Anwendung

    ```dotnetcli
    dotnet new console -lang Q# -o <project name>
    ```

1. Navigieren Sie zum neuen Anwendungsverzeichnis.

    ```
    cd <project name>
    ```

    Es sollten zwei Dateien und die Projektdateien der Anwendung erstellt worden sein: eine Q#-Datei (`Operation.qs`) und eine C#-Hostdatei (`Driver.cs`).

1. Ausführen der Anwendung

    ```dotnetcli
    dotnet run
    ```

    Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`.

Mit Befehlszeilen Tools können Sie nun die Quantum-Entwicklung fortsetzen.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie ein Projekt in Ihrer bevorzugten Umgebung erstellt haben, können Sie die Quantum-Entwicklung fortsetzen.
