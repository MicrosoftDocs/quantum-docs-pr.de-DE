---
title: Entwickeln mit Q# und Python
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: e1b8a0c68b3ac0c059c6de6e478593321764ff88
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680149"
---
# <a name="develop-with-q--python"></a>Entwickeln mit Q# und Python

Installieren Sie das QDK, um python-Host Programme zum Abrufen von Q #-Vorgängen zu entwickeln.

1. Voraussetzungen

    - [Python](https://www.python.org/downloads/) 3,6 oder höher
    - Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager
    - [.NET Core SDK 3.1 oder höher](https://www.microsoft.com/net/download)


1. Installieren Sie `qsharp` das Paket, ein Python-Paket, das Interop zwischen Q # und python ermöglicht.

    ```bash
    pip install qsharp
    ```

1. Installieren Sie IQ #, einen von jupyter und Python verwendeten Kernel, der die Kernfunktionen für das Kompilieren und Ausführen von Q #-Vorgängen bereitstellt.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. Obwohl Sie q # mit python in jeder IDE verwenden können, wird dringend empfohlen, Visual Studio Code (vs Code)-IDE für Ihre Q # + python-Anwendungen zu verwenden. Wenn Sie Visual Studio Code und die QDK-Visual Studio Code Erweiterung verwenden, erhalten Sie Zugriff auf umfangreichere Funktionen.

    - Installieren von [vs Code](https://code.visualstudio.com/download) (Windows, Linux und Mac)
    - Installieren Sie die [QDK-Erweiterung für vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

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

        ```bash
        python hello_world.py
        ```

    - Überprüfen Sie die Ausgabe. Ihr Programm sollte die folgenden Zeilen ausgeben:

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * Sie können auch python jupyter Notebooks verwenden, um das klassische python-Programm zu schreiben und Q #-Vorgänge aus den Zellen aufzurufen. Der Python-Code ist nur ein normales python-Programm.

## <a name="whats-next"></a>Ausblick

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.
