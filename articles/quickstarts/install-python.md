---
title: Entwickeln mit Q# und Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 6513acd5b9cdce15ce61ed2c0454f46e6a6d9bd0
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274085"
---
# <a name="develop-with-q-and-python"></a>Entwickeln mit Q# und Python

Installieren Sie das QDK, um Python-Hostprogramme zum Aufrufen von Q#-Vorgängen zu entwickeln.

1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3.6 oder höher
    - Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Installieren Sie das `qsharp`-Paket. Hierbei handelt es sich um ein Python-Paket, das die Interoperabilität zwischen Q# und Python ermöglicht.

    ```
    pip install qsharp
    ```

1. Installieren Sie IQ#. Dies ist ein von Jupyter und Python verwendeter Kernel, der die Kernfunktionen zum Kompilieren und Ausführen von Q#-Vorgängen bereitstellt.

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
  
1. Sie können Q# mit Python zwar in einer beliebigen IDE verwenden, aber wir empfehlen Ihnen dringend die Nutzung von Visual Studio Code (VS Code) als IDE für Ihre Q#/Python-Anwendungen. Wenn Sie Visual Studio Code und die QDK-Erweiterung für Visual Studio Code verwenden, haben Sie Zugriff auf einen größeren Funktionsumfang.

    - Führen Sie die Installation von [VS Code](https://code.visualstudio.com/download) durch (Windows, Linux und Mac).
    - Installieren Sie die [QDK-Erweiterung für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

    - Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
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

        ```
        python hello_world.py
        ```

    - Überprüfen Sie die Ausgabe. Ihr Programm sollte die folgenden Zeilen ausgeben:

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * Sie können auch Python-Jupyter Notebooks verwenden, um klassische Python-Programme zu schreiben und Q#-Vorgänge aus den Zellen aufzurufen. Beim Python-Code handelt es sich nur um ein normales Python-Programm.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
