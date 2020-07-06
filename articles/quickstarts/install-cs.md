---
title: Entwickeln mit Q# und .Net
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 714c15d9589095f0fe395fcd6941672167879dca
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885503"
---
# <a name="develop-with-q-and-net"></a><span data-ttu-id="e8f66-102">Entwickeln mit Q# und .Net</span><span class="sxs-lookup"><span data-stu-id="e8f66-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="e8f66-103">Q# ist auf die Verwendung mit .NET-Sprachen wie C# und F# ausgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8f66-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="e8f66-104">In diesem Leitfaden wird veranschaulicht, wie Sie Q# mit einem in einer .NET-Sprache geschriebenen Hostprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8f66-104">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="e8f66-105">Zunächst erstellen wir die Q#-Anwendung und den .NET-Host und veranschaulichen dann, wie Q# über den Host aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e8f66-105">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8f66-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e8f66-106">Prerequisites</span></span>

- <span data-ttu-id="e8f66-107">Installieren Sie das Quantum Development Kit [für die Nutzung mit Q#-Befehlszeilenprojekten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="e8f66-107">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="e8f66-108">Erstellen einer Q#-Bibliothek und eines .NET-Hosts</span><span class="sxs-lookup"><span data-stu-id="e8f66-108">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="e8f66-109">Der erste Schritt ist die Erstellung von Projekten für Ihre Q#-Bibliothek und für den .NET-Host, von dem Aufrufe für die in Ihrer Q#-Bibliothek definierten Vorgänge und Funktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e8f66-109">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="e8f66-110">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Entwicklungsumgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="e8f66-110">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="e8f66-111">Wenn Sie einen anderen Editor als Visual Studio oder VS Code verwenden, befolgen Sie einfach die Schritte für die Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="e8f66-111">If you are using an editor other than Visual Studio or VS Code, simply follow the command line steps.</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="e8f66-112">Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="e8f66-112">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="e8f66-113">Erstellen einer neuen Q#-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8f66-113">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="e8f66-114">Erstellen Sie ein neues C#- oder F#-Konsolenprojekt.</span><span class="sxs-lookup"><span data-stu-id="e8f66-114">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="e8f66-115">Fügen Sie Ihre Q#-Bibliothek als Verweis aus Ihrem Hostprogramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8f66-115">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="e8f66-116">[Optional] Erstellen Sie eine Projektmappe für beide Projekte.</span><span class="sxs-lookup"><span data-stu-id="e8f66-116">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="e8f66-117">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="e8f66-117">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="e8f66-118">Erstellen einer neuen Q#-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8f66-118">Create a new Q# library</span></span>
  - <span data-ttu-id="e8f66-119">Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e8f66-119">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="e8f66-120">Geben Sie im Suchfeld als Suchbegriff „Q#“ ein.</span><span class="sxs-lookup"><span data-stu-id="e8f66-120">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="e8f66-121">Wählen Sie **Q#-Bibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-121">Select **Q# Library**</span></span>
  - <span data-ttu-id="e8f66-122">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-122">Select **Next**</span></span>
  - <span data-ttu-id="e8f66-123">Wählen Sie einen Namen und Speicherort für Ihre Bibliothek aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-123">Choose a name and location for your library</span></span>
  - <span data-ttu-id="e8f66-124">Stellen Sie sicher, dass die Option „Place project and solution in same directory“ (Projekt und Projektmappe in demselben Verzeichnis anordnen) **deaktiviert** ist.</span><span class="sxs-lookup"><span data-stu-id="e8f66-124">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="e8f66-125">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="e8f66-125">Select **Create**</span></span>
- <span data-ttu-id="e8f66-126">Erstellen eines neuen C#- oder F#-Hostprogramms</span><span class="sxs-lookup"><span data-stu-id="e8f66-126">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="e8f66-127">Navigieren Sie zu **Datei** > **Neu** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e8f66-127">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="e8f66-128">Wählen Sie für C# bzw. F# die Option „Konsolen-App (.NET Core)“ aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-128">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="e8f66-129">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-129">Select **Next**</span></span>
  - <span data-ttu-id="e8f66-130">Wählen Sie unter *Projektmappe* die Option „Zur Projektmappe hinzufügen“ aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-130">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="e8f66-131">Wählen Sie einen Namen für Ihr Hostprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="e8f66-131">Choose a name for your host program</span></span>
  - <span data-ttu-id="e8f66-132">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="e8f66-132">Select **Create**</span></span>

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="e8f66-133">Durchführen von Q#-Aufrufen aus .NET</span><span class="sxs-lookup"><span data-stu-id="e8f66-133">Calling into Q# from .NET</span></span>

<span data-ttu-id="e8f66-134">Nachdem Sie Ihre Projekte gemäß der obigen Anleitung eingerichtet haben, können Sie aus Ihrer .NET-Konsolenanwendung Q#-Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="e8f66-134">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="e8f66-135">Der Q#-Compiler erstellt .NET-Klassen für alle Q#-Vorgänge und -Funktionen, die Ihnen das Ausführen Ihrer Quantenprogramme in einem Simulator ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e8f66-135">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="e8f66-136">Das [Beispiel zur .NET-Interoperabilität](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) enthält das folgende Beispiel für einen Q#-Vorgang:</span><span class="sxs-lookup"><span data-stu-id="e8f66-136">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="e8f66-137">Um diesen Vorgang aus .NET in einem Quantensimulator aufzurufen, können Sie die Methode `Run` der .NET-Klasse `RunAlgorithm` verwenden, die vom Q#-Compiler generiert wird:</span><span class="sxs-lookup"><span data-stu-id="e8f66-137">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="e8f66-138">C#</span><span class="sxs-lookup"><span data-stu-id="e8f66-138">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="e8f66-139">F#</span><span class="sxs-lookup"><span data-stu-id="e8f66-139">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="e8f66-140">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e8f66-140">Next steps</span></span>

<span data-ttu-id="e8f66-141">Nachdem Sie das Quantum Development Kit nun sowohl für Q#-Befehlszeilenprogramme als auch für die Interoperabilität mit .NET eingerichtet haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8f66-141">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
