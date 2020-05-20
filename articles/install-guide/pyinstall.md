---
title: 'Entwickeln mit Q # und python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 35499daae0cd0ae329e39b43b0d8dd5a00183871
ms.sourcegitcommit: 328f45a0b64cb6b325fa9d3b3ddb74a6a7a97ee9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "83660731"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="2ee8a-102">Entwickeln mit Q # und python</span><span class="sxs-lookup"><span data-stu-id="2ee8a-102">Develop with Q# and Python</span></span>

<span data-ttu-id="2ee8a-103">Installieren Sie das QDK, um python-Host Programme zum Abrufen von Q #-Vorgängen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="2ee8a-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2ee8a-104">Pre-requisites</span></span>

    - <span data-ttu-id="2ee8a-105">[Python](https://www.python.org/downloads/) 3,6 oder höher</span><span class="sxs-lookup"><span data-stu-id="2ee8a-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="2ee8a-106">Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="2ee8a-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="2ee8a-107">.Net Core SDK 3,1</span><span class="sxs-lookup"><span data-stu-id="2ee8a-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="2ee8a-108">Installieren Sie das `qsharp` Paket, ein Python-Paket, das Interop zwischen Q # und python ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="2ee8a-109">Installieren Sie IQ #, einen von jupyter und Python verwendeten Kernel, der die Kernfunktionen für das Kompilieren und Ausführen von Q #-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="2ee8a-110">Obwohl Sie q # mit python in jeder IDE verwenden können, wird dringend empfohlen, Visual Studio Code (vs Code)-IDE für Ihre Q # + python-Anwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="2ee8a-111">Wenn Sie Visual Studio Code und die QDK-Visual Studio Code Erweiterung verwenden, erhalten Sie Zugriff auf umfangreichere Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="2ee8a-112">Installieren von [vs Code](https://code.visualstudio.com/download) (Windows, Linux und Mac)</span><span class="sxs-lookup"><span data-stu-id="2ee8a-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="2ee8a-113">Installieren Sie die [QDK-Erweiterung für vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="2ee8a-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="2ee8a-114">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2ee8a-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="2ee8a-115">Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="2ee8a-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="2ee8a-116">Erstellen Sie ein Python-Programm mit dem Namen `hello_world.py`, um den Q#-Vorgang `SayHello()` aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="2ee8a-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="2ee8a-117">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="2ee8a-117">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="2ee8a-118">Überprüfen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-118">Verify the output.</span></span> <span data-ttu-id="2ee8a-119">Ihr Programm sollte die folgenden Zeilen ausgeben:</span><span class="sxs-lookup"><span data-stu-id="2ee8a-119">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * <span data-ttu-id="2ee8a-120">Sie können auch python jupyter Notebooks verwenden, um das klassische python-Programm zu schreiben und Q #-Vorgänge aus den Zellen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="2ee8a-121">Der Python-Code ist nur ein normales python-Programm.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-121">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2ee8a-122">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="2ee8a-122">Next steps</span></span>

<span data-ttu-id="2ee8a-123">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
