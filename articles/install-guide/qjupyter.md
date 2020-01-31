---
title: 'Entwickeln mit Q # jupyter Notebooks'
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
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="b8559-102">Entwickeln mit Q # jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="b8559-102">Develop with Q# Jupyter notebooks</span></span>

<span data-ttu-id="b8559-103">Installieren Sie das QDK zum Entwickeln von q #-Vorgängen für q # jupyter-Notebooks.</span><span class="sxs-lookup"><span data-stu-id="b8559-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="b8559-104">Jupyter-Notebooks ermöglichen die direkte Codeausführung neben Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="b8559-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="b8559-105">Diese Umgebung eignet sich ideal zum Schreiben von f #-Code mit eingebetteten Erläuterungen oder interaktiven Lernprogrammen für Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="b8559-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="b8559-106">Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="b8559-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="b8559-107">IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b8559-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="b8559-108">In q # jupyter Notebooks können Sie nur q #-Code ausführen, und die Vorgänge können nicht von externen Host Programmen (z. b. C# python oder Dateien) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b8559-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="b8559-109">Diese Umgebung ist nicht geeignet, wenn Sie ein externes klassisches Host Programm mit dem Quantum-Programm kombinieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b8559-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="b8559-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b8559-110">Pre-requisites</span></span>

    - <span data-ttu-id="b8559-111">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8559-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="b8559-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="b8559-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="b8559-113">.Net Core SDK 3,1 oder höher</span><span class="sxs-lookup"><span data-stu-id="b8559-113">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="b8559-114">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="b8559-114">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="b8559-115">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="b8559-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="b8559-116">Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:</span><span class="sxs-lookup"><span data-stu-id="b8559-116">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="b8559-117">Um das jupyter Notebook zu öffnen, und fügen Sie die von der Befehlszeile bereitgestellte URL in Ihren Browser ein.</span><span class="sxs-lookup"><span data-stu-id="b8559-117">To open the Jupyter notebook copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="b8559-118">Erstellen Sie ein Jupyter-Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="b8559-118">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="b8559-119">Führen Sie diese Zelle des Notebooks aus:</span><span class="sxs-lookup"><span data-stu-id="b8559-119">Run this cell of the notebook:</span></span>

        ![Zelle im Jupyter-Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

        <span data-ttu-id="b8559-121">In der Ausgabe der Zelle sollte `SayHello` angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8559-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="b8559-122">Bei der Ausführung in Jupyter-Notebooks wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="b8559-122">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="b8559-123">Führen Sie in einer neuen Zelle den soeben erstellten Vorgang (in einem Simulator) mit dem Befehl `%simulate` aus:</span><span class="sxs-lookup"><span data-stu-id="b8559-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Zelle im Jupyter-Notebook mit %simulate-Magic](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="b8559-125">Es sollte angezeigt werden, dass die Meldung auf dem Bildschirm angezeigt wird, und das Ergebnis des Vorgangs, den Sie aufgerufen haben (hier sehen wir das leere Tupel `()`, da der Vorgang einfach einen `Unit` Typ zurückgibt).</span><span class="sxs-lookup"><span data-stu-id="b8559-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="whats-next"></a><span data-ttu-id="b8559-126">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="b8559-126">What's next?</span></span>

<span data-ttu-id="b8559-127">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8559-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
