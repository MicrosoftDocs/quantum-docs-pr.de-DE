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
# <a name="develop-with-q-and-python"></a><span data-ttu-id="e3c97-102">Entwickeln mit Q# und Python</span><span class="sxs-lookup"><span data-stu-id="e3c97-102">Develop with Q# and Python</span></span>

<span data-ttu-id="e3c97-103">Installieren Sie das QDK, um Python-Hostprogramme zum Aufrufen von Q#-Vorgängen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="e3c97-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="e3c97-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e3c97-104">Prerequisites</span></span>

    - <span data-ttu-id="e3c97-105">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="e3c97-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="e3c97-106">Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="e3c97-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="e3c97-107">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="e3c97-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="e3c97-108">Installieren Sie das `qsharp`-Paket. Hierbei handelt es sich um ein Python-Paket, das die Interoperabilität zwischen Q# und Python ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e3c97-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="e3c97-109">Installieren Sie IQ#. Dies ist ein von Jupyter und Python verwendeter Kernel, der die Kernfunktionen zum Kompilieren und Ausführen von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e3c97-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="e3c97-110">Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.</span><span class="sxs-lookup"><span data-stu-id="e3c97-110">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="e3c97-111">Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="e3c97-111">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="e3c97-112">Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="e3c97-112">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="e3c97-113">Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.</span><span class="sxs-lookup"><span data-stu-id="e3c97-113">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
  
1. <span data-ttu-id="e3c97-114">Sie können Q# mit Python zwar in einer beliebigen IDE verwenden, aber wir empfehlen Ihnen dringend die Nutzung von Visual Studio Code (VS Code) als IDE für Ihre Q#/Python-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e3c97-114">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="e3c97-115">Wenn Sie Visual Studio Code und die QDK-Erweiterung für Visual Studio Code verwenden, haben Sie Zugriff auf einen größeren Funktionsumfang.</span><span class="sxs-lookup"><span data-stu-id="e3c97-115">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="e3c97-116">Führen Sie die Installation von [VS Code](https://code.visualstudio.com/download) durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="e3c97-116">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="e3c97-117">Installieren Sie die [QDK-Erweiterung für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="e3c97-117">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="e3c97-118">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="e3c97-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="e3c97-119">Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="e3c97-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="e3c97-120">Erstellen Sie ein Python-Programm mit dem Namen `hello_world.py`, um den Q#-Vorgang `SayHello()` aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="e3c97-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="e3c97-121">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="e3c97-121">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="e3c97-122">Überprüfen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3c97-122">Verify the output.</span></span> <span data-ttu-id="e3c97-123">Ihr Programm sollte die folgenden Zeilen ausgeben:</span><span class="sxs-lookup"><span data-stu-id="e3c97-123">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="e3c97-124">Sie können auch Python-Jupyter Notebooks verwenden, um klassische Python-Programme zu schreiben und Q#-Vorgänge aus den Zellen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3c97-124">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="e3c97-125">Beim Python-Code handelt es sich nur um ein normales Python-Programm.</span><span class="sxs-lookup"><span data-stu-id="e3c97-125">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e3c97-126">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e3c97-126">Next steps</span></span>

<span data-ttu-id="e3c97-127">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3c97-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
