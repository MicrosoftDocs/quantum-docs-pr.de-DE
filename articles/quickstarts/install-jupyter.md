---
title: Entwickeln mit Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274097"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Entwickeln mit Q#-Jupyter Notebooks

Installieren Sie das QDK für die Entwicklung von Q#-Vorgängen auf Q#-Jupyter Notebooks.

Jupyter Notebooks ermöglichen die direkte Codeausführung parallel zu Anweisungen, Notizen und anderem Inhalt. Diese Umgebung eignet sich ideal zum Schreiben von Q#-Code mit eingebetteten Erläuterungen oder interaktiven Tutorials zum Quantencomputing. Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.

IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.

> [!NOTE]
> * In Q#-Jupyter Notebooks können Sie nur Q#-Code ausführen, und die Vorgänge können nicht über externe Hostprogramme (z. B. Python- oder C#-Dateien) aufgerufen werden. Diese Umgebung ist nicht geeignet, wenn Ihr Ziel die Kombination eines externen klassischen Hostprogramms mit dem Quantenprogramm ist.

1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3.6 oder höher
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Installieren Sie das Paket `iqsharp`.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.
    > Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.
    > Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:

        ```
        jupyter notebook
        ```

    - Kopieren Sie zum Öffnen des Jupyter Notebooks die URL aus der Befehlszeile in Ihren Browser.

    - Erstellen Sie ein Jupyter Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Führen Sie diese Zelle des Notebooks aus:

        ![Zelle im Jupyter Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

        In der Ausgabe der Zelle sollte `SayHello` angezeigt werden. Bei der Ausführung im Jupyter Notebook wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.


    - Führen Sie in einer neuen Zelle den soeben erstellten Vorgang aus (in einem Simulator), indem Sie den Befehl `%simulate` verwenden:

        ![Jupyter Notebook-Zelle mit %simulate-Magic-Befehl](~/media/install-guide-jupyter-simulate.png)

        Auf dem Bildschirm sollte die Meldung mit dem Ergebnis des von Ihnen aufgerufenen Vorgangs angezeigt werden (hier ist dies das leere Tupel `()`, weil bei unserem Vorgang lediglich der Typ `Unit` zurückgegeben wird).

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das QDK für Q#-Jupyter Notebooks nun installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen. Schreiben Sie Ihren Q#-Code hierfür direkt in der Jupyter Notebook-Umgebung.

Weitere Beispiele für die Nutzung von Q#-Jupyter Notebooks finden Sie unter:
- [Einführung in Q# und Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Enthält ein Q#-Jupyter Notebook, mit dem veranschaulicht wird, wie Sie Q# in dieser Umgebung verwenden.
- [Quanten-Katas](xref:microsoft.quantum.overview.katas), eine Open-Source-Sammlung mit eigenverantwortlich zu absolvierenden Tutorials und Programmierübungen in Form von Q#-Jupyter Notebooks. Die [Tutorial-Notebooks der Quanten-Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) sind ein guter Ausgangspunkt. Die Quanten-Katas sind so ausgelegt, dass Ihnen gleichzeitig Elemente des Quantencomputings und der Q#-Programmierung vermittelt werden. Sie sind ein hervorragendes Beispiel dafür, welche Arten von Inhalt Sie mit Q#-Jupyter Notebooks erstellen können.
