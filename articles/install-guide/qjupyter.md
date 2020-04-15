---
title: 'Entwickeln mit Q# jupyter Notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b7276f9b273f601f30e4938018398353b6a9102d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831068"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Entwickeln mit Q# jupyter Notebooks

Installieren Sie das QDK zum Entwickeln von Q#-Vorgängen für Q# jupyter-Notebooks.

Jupyter-Notebooks ermöglichen die direkte Codeausführung neben Anweisungen, Notizen und anderem Inhalt. Diese Umgebung eignet sich ideal zum Schreiben von Q#-Code mit eingebetteten Erläuterungen oder interaktiven Lernprogrammen für Quantum Computing. Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.

IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.

> [!NOTE]
> * In Q# jupyter Notebooks können Sie nur Q#-Code ausführen, und die Vorgänge können nicht von externen Host Programmen (z. b. C# python oder Dateien) aufgerufen werden. Diese Umgebung ist nicht geeignet, wenn Sie ein externes klassisches Host Programm mit dem Quantum-Programm kombinieren möchten.

1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3.6 oder höher
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.Net Core SDK 3,1 oder höher](https://www.microsoft.com/net/download)

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

    - Um das jupyter Notebook zu öffnen, und fügen Sie die von der Befehlszeile bereitgestellte URL in Ihren Browser ein.

    - Erstellen Sie ein Jupyter-Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Führen Sie diese Zelle des Notebooks aus:

        ![Zelle im Jupyter-Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

        In der Ausgabe der Zelle sollte `SayHello` angezeigt werden. Bei der Ausführung in Jupyter-Notebooks wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.


    - Führen Sie in einer neuen Zelle den soeben erstellten Vorgang (in einem Simulator) mit dem Befehl `%simulate` aus:

        ![Zelle im Jupyter-Notebook mit %simulate-Magic](~/media/install-guide-jupyter-simulate.png)

        Es sollte angezeigt werden, dass die Meldung auf dem Bildschirm angezeigt wird, und das Ergebnis des Vorgangs, den Sie aufgerufen haben (hier sehen wir das leere Tupel `()`, da der Vorgang einfach einen `Unit` Typ zurückgibt).

## <a name="whats-next"></a>Wie geht es weiter?

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.
