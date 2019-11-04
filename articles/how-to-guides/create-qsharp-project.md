---
title: 'Erfahren Sie, wie Sie ein Q #-Projekt mit dem Quantum Development Kit (QDK) erstellen.'
description: 'Initialisieren eines Projekts für die Quantum-Entwicklung mit dem QDK und f # in der von Ihnen ausgewählten Entwicklungsumgebung'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: b4bec5e7a174b7e2d588331dd2093c7b23a728b0
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444173"
---
# <a name="create-a-q-project-in-your-development-environment"></a>Erstellen eines Q #-Projekts in Ihrer Entwicklungsumgebung

Erfahren Sie, wie Sie ein Q #-Projekt mit dem QDK erstellen.

Ein q #-Projekt enthält q #-Dateien, die den Quantum-Code enthalten, sowie ein Host Programm zum Ausführen des Quantum-Programms. Sie können das Host Programm in .NET-Sprachen wie C#oder in Python schreiben. Sie können auch Q #-Code in einem jupyter-Notebook mithilfe des IQ #-Kernels ausführen.

Wählen Sie in den folgenden Abschnitten Ihre Entwicklungsumgebung und Sprache aus:

* [Python](#create-a-python-project)
* [Jupyter-Notebooks](#create-a-jupyter-notebook-project)
* [C#mit Visual Studio](#create-a-c-project-on-windows-using-visual-studio)
* [C#mit vs Code](#create-a-c-project-using-vs-code)
* [C#mit der Befehlszeile](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a>Erstellen eines python-Projekts

1. Voraussetzungen

     * Das [Quantum Development Kit für python](xref:microsoft.quantum.install#develop-with-python)

1. Erstellen Sie einen Ordner für das Projekt, und navigieren Sie zu diesem Ordner.

1. Erstellen Sie eine q #-Datei mit dem Namen `Operation.qs`, und fügen Sie Ihr den q #-Code hinzu. Beispiel:

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

1. Erstellen Sie eine python-Hostdatei mit dem Namen `host.py`, um den Q #-Vorgang aufzurufen Beispiel:

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. Führen Sie das Programm aus:

    ```bash
    python host.py
    ```

1. Überprüfen Sie die Ausgabe. Ihr Programm sollte die folgenden Zeilen ausgeben:

    ```bash
    Hello from quantum world!
    0
    ```

Sie können nun mit der Entwicklung des Quantums Programm fortfahren.

## <a name="create-a-jupyter-notebook-project"></a>Erstellen eines Jupyter Notebook Projekts

1. Voraussetzungen

    * Das [Quantum Development Kit für jupyter-Notebooks](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)

1. Führen Sie den folgenden Befehl aus, um den Notebook-Server zu starten:

    ```bash
    jupyter notebook
    ```

1. Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird. Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

1. Eine jupyter-Seite wird im Browser angezeigt. Wählen Sie auf der Registerkarte **Dateien** die Option **neu** > **Q #** aus, um ein jupyter-Notebook mit einem Q #-Kernel zu erstellen. Fügen Sie den folgenden Code in die erste Notebook-Zelle ein:

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. Wählen Sie **Cell** > **Zellen ausführen** aus, um das Notebook auszuführen. `SayHello` wird in Kürze in der Zellen Ausgabe angezeigt:

    ![Jupyter Notebook-Zelle mit Q #-Code](~/media/install-guide-jupyter.png)

    Bei der Ausführung in jupyter-Notebooks wird der Q #-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.

1. Simulieren Sie in einer neuen Zelle die Ausführung auf einem Quantum-Computer des gerade erstellten Vorgangs mithilfe der `%simulate` Magic:

    ![Jupyter Notebook-Zelle mit "% simulieren" Magic](~/media/install-guide-jupyter-simulate.png)

    Es sollte angezeigt werden, dass die Meldung auf dem Bildschirm angezeigt wird, und das Ergebnis des Vorgangs, den Sie aufgerufen haben (in diesem Fall leer).

Sie können jetzt weitere Q #-Vorgänge hinzufügen, um die Quantum-Entwicklung fortzusetzen.

## <a name="create-a-c-project-on-windows-using-visual-studio"></a>Erstellen eines C# Projekts unter Windows mit Visual Studio

1. Voraussetzungen

    * Das [Quantum Development Kit für Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)

1. Erstellen einer neuen f #-Anwendung

    * Gehe zu **Datei** -> **Neues** -> **Projekt**
    * Geben Sie `Q#` in das Suchfeld ein.
    * **F #-Anwendung** auswählen
    * Wählen Sie **Weiter** aus
    * Auswählen eines Namens und eines Speicher Orts für die Anwendung
    * Klicken Sie auf **Erstellen**

1. Überprüfen des Projekts

    Sie sollten sehen, dass zwei Dateien erstellt wurden: `Driver.cs`, die die C# Host Anwendung ist. und `Operation.qs`. dabei handelt es sich um ein Q #-Programm, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.

1. Ausführen der Anwendung

    * Wählen Sie **Debuggen** -> **Starten ohne Debugging**
    * Sie sollten sehen, dass der Text in einem Konsolenfenster gedruckt `Hello quantum world!`.

Sie können jetzt die Quantum-Entwicklung mit Visual Studio fortsetzen.

> [!NOTE]
> * Wenn Sie mehrere Projekte in einer Visual Studio-Projekt Mappe haben, müssen sich alle in der Projekt Mappe enthaltenen Projekte im selben Ordner wie die Projekt Mappe oder in einem ihrer Unterordner befinden.  

## <a name="create-a-c-project-using-vs-code"></a>Erstellen eines C# Projekts mit vs Code

1. Voraussetzungen

    * Das [Quantum Development Kit für vs Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)

1. Erstellen eines neuen Projekts:

    * Gehe zu **Ansicht** -> **Befehls Palette**
    * Wählen Sie **Q #: Neues Projekt erstellen** aus.
    * Navigieren Sie zu dem Speicherort im Dateisystem, in dem Sie die Anwendung erstellen möchten.
    * Klicken Sie auf die Schaltfläche **Neues Projekt öffnen...** , nachdem das Projekt erstellt wurde.

1. Führen Sie die Anwendung aus.

    * Gehe zu **Debuggen** -> **Starten ohne Debugging**
    * Der folgende Text sollte im Ausgabefenster angezeigt werden `Hello quantum world!`

Nun können Sie die Quantum-Entwicklung mit Visual Studio Code fortsetzen.

> [!NOTE]
> * Arbeitsbereiche mit mehreren Stamm Ordnern werden zurzeit von der Visual Studio Code Erweiterung nicht unterstützt. Wenn Sie über mehrere Projekte in einem vs Code Arbeitsbereich verfügen, müssen alle Projekte im selben Stamm Ordner enthalten sein.

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a>Erstellen eines C# Projekts mit dem Befehlszeilen Tool "`dotnet`"

1. Voraussetzungen

    * Das [Quantum Development Kit für die Befehlszeile](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)

1. Erstellen einer neuen Anwendung

    ```bash
    dotnet new console -lang Q# -o <project name>
    ```

1. Navigieren Sie zum neuen Anwendungsverzeichnis.

    ```bash
    cd <project name>
    ```

    Sie sollten sehen, dass zwei Dateien erstellt wurden, zusammen mit den Projektdateien der Anwendung: eine Q #-Datei (`Operation.qs`) und eine C# Hostdatei (`Driver.cs`).

1. Ausführen der Anwendung

    ```bash
    dotnet run
    ```

    Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`

Mit Befehlszeilen Tools können Sie nun die Quantum-Entwicklung fortsetzen.

## <a name="whats-next"></a>Wie geht es weiter?

Nachdem Sie ein Projekt in Ihrer bevorzugten Umgebung erstellt haben, können Sie die Quantum-Entwicklung fortsetzen.
