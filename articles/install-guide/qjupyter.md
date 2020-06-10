---
title: Entwickeln mit Q#-Jupyter-Notebooks
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630332"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Entwickeln mit Q#-Jupyter-Notebooks

Installieren Sie das QDK zum Entwickeln von q #-Vorgängen für q # jupyter-Notebooks.

Jupyter-Notebooks ermöglichen die direkte Codeausführung neben Anweisungen, Notizen und anderem Inhalt. Diese Umgebung eignet sich ideal zum Schreiben von f #-Code mit eingebetteten Erläuterungen oder interaktiven Lernprogrammen für Quantum Computing. Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.

IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.

> [!NOTE]
> * In q # jupyter Notebooks können Sie nur q #-Code ausführen, und die Vorgänge können nicht von externen Host Programmen (z. b. python-oder c#-Dateien) aufgerufen werden. Diese Umgebung ist nicht geeignet, wenn Sie ein externes klassisches Host Programm mit dem Quantum-Programm kombinieren möchten.

1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3,6 oder höher
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.Net Core SDK 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Installieren Sie das Paket `iqsharp`.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Wenn Sie während des Schritts einen Fehler erhalten `dotnet iqsharp install` , öffnen Sie ein neues Terminalfenster, und versuchen Sie es erneut.
    > Wenn dies immer noch nicht funktioniert, versuchen Sie, das installierte `dotnet-iqsharp` Tool (unter Windows) zu suchen `dotnet-iqsharp.exe` und Folgendes auszuführen:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > `/path/to/dotnet-iqsharp`dabei sollte durch den absoluten Pfad zum `dotnet-iqsharp` Tool in Ihrem Dateisystem ersetzt werden.
    > In der Regel wird dies `.dotnet/tools` in Ihrem Benutzerprofil Ordner unterliegen.

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:

        ```
        jupyter notebook
        ```

    - Um das Jupyter Notebook zu öffnen, kopieren Sie die von der Befehlszeile bereitgestellte URL in Ihren Browser, und fügen Sie Sie ein.

    - Erstellen Sie eine Jupyter Notebook mit einem Q #-Kernel, und fügen Sie der ersten Notebook-Zelle den folgenden Code hinzu:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Führen Sie diese Zelle des Notebooks aus:

        ![Jupyter Notebook Zelle mit Q #-Code](~/media/install-guide-jupyter.png)

        In der Ausgabe der Zelle sollte `SayHello` angezeigt werden. Bei Ausführung in Jupyter Notebook wird der Q #-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.


    - Führen Sie in einer neuen Zelle den soeben erstellten Vorgang (in einem Simulator) mithilfe des Befehls aus `%simulate` :

        ![Jupyter Notebook Zelle mit "% simulieren" Magic](~/media/install-guide-jupyter-simulate.png)

        Die Meldung sollte zusammen mit dem Ergebnis des aufgerufenen Vorgangs auf dem Bildschirm angezeigt werden (hier sehen wir das leere Tupel, `()` da der Vorgang einfach einen Typ zurückgibt `Unit` ).

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das QDK für Q # jupyter Notebooks installiert haben, können Sie [Ihr erstes Quantum-Programm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen, indem Sie den Q #-Code direkt in die Jupyter Notebook Umgebung schreiben.

Weitere Beispiele für das, was Sie mit Q # jupyter-Notebooks tun können, finden Sie unter:
- Einführung [in Q # und Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Dort finden Sie eine q #-Jupyter Notebook, die zeigt, wie q # in dieser Umgebung verwendet wird.
- [Quantum Katas](xref:microsoft.quantum.overview.katas), eine Open Source-Sammlung von Lernprogrammen für das Selbststudium und Sätze von programmierübungen in Form von Q # jupyter-Notebooks. Das [Quantum Katas Tutorial](https://github.com/microsoft/QuantumKatas#tutorial-topics) ist ein guter Ausgangspunkt. Die Quantum-Katas sind darauf ausgerichtet, Ihnen Elemente von Quantum Computing und Q #-Programmierung gleichzeitig zu vermitteln. Sie sind ein gutes Beispiel für die Art von Inhalten, die Sie mit Q # jupyter Notebooks erstellen können.
