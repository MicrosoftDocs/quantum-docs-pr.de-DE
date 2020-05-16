---
title: Entwickeln mit Q# und .Net
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 155367dbb1373f00e2b0bd732a5319b32462c9f9
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426499"
---
# <a name="develop-with-q-and-net"></a><span data-ttu-id="df97d-102">Entwickeln mit Q# und .Net</span><span class="sxs-lookup"><span data-stu-id="df97d-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="df97d-103">F # ist für .NET-Sprachen wie c# und F # konzipiert.</span><span class="sxs-lookup"><span data-stu-id="df97d-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="df97d-104">In dieser Anleitung erfahren Sie, wie Sie Q # mit einem in einer .NET-Sprache geschriebenen Host Programm verwenden.</span><span class="sxs-lookup"><span data-stu-id="df97d-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df97d-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="df97d-105">Prerequisites</span></span>

- <span data-ttu-id="df97d-106">Installieren Sie das Quantum Development Kit [für die Verwendung mit f #-Befehlszeilen Projekten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="df97d-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="df97d-107">Erstellen einer Q #-Bibliothek und eines .NET-Hosts</span><span class="sxs-lookup"><span data-stu-id="df97d-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="df97d-108">Der erste Schritt besteht im Erstellen von Projekten für die q #-Bibliothek und für den .NET-Host, der die in der q #-Bibliothek definierten Vorgänge und Funktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="df97d-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="df97d-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="df97d-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="df97d-110">Erstellen einer neuen Q #-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df97d-110">Create a new Q# library</span></span>
  - <span data-ttu-id="df97d-111">Wechseln Sie zu **Datei**  ->  **Neues**  ->  **Projekt** .</span><span class="sxs-lookup"><span data-stu-id="df97d-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="df97d-112">Geben Sie "Q #" in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="df97d-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="df97d-113">**Q #-Bibliothek** auswählen</span><span class="sxs-lookup"><span data-stu-id="df97d-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="df97d-114">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="df97d-114">Select **Next**</span></span>
  - <span data-ttu-id="df97d-115">Auswählen eines Namens und eines Speicher Orts für die Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df97d-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="df97d-116">Stellen Sie sicher, dass "Projekt und Projekt Mappe in demselben Verzeichnis platzieren" nicht **aktiviert** ist.</span><span class="sxs-lookup"><span data-stu-id="df97d-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="df97d-117">Klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="df97d-117">Select **Create**</span></span>
- <span data-ttu-id="df97d-118">Erstellen eines neuen c#-oder F #-Host Programms</span><span class="sxs-lookup"><span data-stu-id="df97d-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="df97d-119">Gehe zu **Datei** → **neu** → **Projekt**</span><span class="sxs-lookup"><span data-stu-id="df97d-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="df97d-120">Wählen Sie "Konsolen-app (.net Core") "für c# oder F aus. #</span><span class="sxs-lookup"><span data-stu-id="df97d-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="df97d-121">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="df97d-121">Select **Next**</span></span>
  - <span data-ttu-id="df97d-122">Wählen *Sie Unterprojekt*Mappe die Option zur Projekt Mappe hinzufügen aus.</span><span class="sxs-lookup"><span data-stu-id="df97d-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="df97d-123">Wählen Sie einen Namen für das Host Programm aus.</span><span class="sxs-lookup"><span data-stu-id="df97d-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="df97d-124">Klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="df97d-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="df97d-125">Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="df97d-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="df97d-126">Erstellen einer neuen Q #-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df97d-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="df97d-127">Neues c#-oder F #-Konsolen Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="df97d-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="df97d-128">Hinzufügen der Q #-Bibliothek als Verweis von Ihrem Host Programm</span><span class="sxs-lookup"><span data-stu-id="df97d-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="df97d-129">Optionale Erstellen einer Projekt Mappe für beide Projekte</span><span class="sxs-lookup"><span data-stu-id="df97d-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="df97d-130">Aufrufen von f # aus .net</span><span class="sxs-lookup"><span data-stu-id="df97d-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="df97d-131">Nachdem Sie Ihre Projekte gemäß den obigen Anweisungen eingerichtet haben, können Sie in der .NET-Konsolenanwendung Q # anrufen.</span><span class="sxs-lookup"><span data-stu-id="df97d-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="df97d-132">Der f #-Compiler erstellt .NET-Klassen für jeden q #-Vorgang und jede Funktion, die es Ihnen ermöglichen, die Quantum-Programme in einem Simulator auszuführen.</span><span class="sxs-lookup"><span data-stu-id="df97d-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="df97d-133">Beispielsweise enthält das [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) Beispiel das folgende Beispiel für einen Q #-Vorgang:</span><span class="sxs-lookup"><span data-stu-id="df97d-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="df97d-134">Um diesen Vorgang von .net in einem Quantum-Simulator aufzurufen, können Sie die- `Run` Methode der .NET-Klasse verwenden, die `RunAlgorithm` vom Q #-Compiler generiert wird:</span><span class="sxs-lookup"><span data-stu-id="df97d-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="df97d-135">C#</span><span class="sxs-lookup"><span data-stu-id="df97d-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="df97d-136">F#</span><span class="sxs-lookup"><span data-stu-id="df97d-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="df97d-137">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="df97d-137">Next steps</span></span>

<span data-ttu-id="df97d-138">Nun, da Sie das Quantum Development Kit sowohl für Q #-Befehlszeilen Programme als auch für die Interoperabilität mit .net eingerichtet haben, können Sie [Ihr erstes Quantum-Programm](xref:microsoft.quantum.quickstarts.qrng)schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="df97d-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
