---
title: Entwickeln mit Q# und .NET
description: Hier erfahren Sie, wie Sie mithilfe von .NET-Sprachen eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: e8733918daa02afaea0fc1994d5f0851d4be9b93
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834328"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="e3ed3-103">Entwickeln mit Q# und .NET</span><span class="sxs-lookup"><span data-stu-id="e3ed3-103">Develop with Q# and .NET</span></span>

<span data-ttu-id="e3ed3-104">Q# ist auf die Verwendung mit .NET-Sprachen wie C# und F# ausgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-104">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="e3ed3-105">In diesem Leitfaden wird veranschaulicht, wie Sie Q# mit einem in einer .NET-Sprache geschriebenen Hostprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-105">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="e3ed3-106">Zunächst erstellen wir die Q#-Anwendung und den .NET-Host und veranschaulichen dann, wie Q# über den Host aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-106">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3ed3-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e3ed3-107">Prerequisites</span></span>

- <span data-ttu-id="e3ed3-108">Installieren Sie das Quantum Development Kit [für die Nutzung mit Q#-Projekten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="e3ed3-108">Install the Quantum Development Kit [for use with Q# projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="e3ed3-109">Erstellen einer Q#-Bibliothek und eines .NET-Hosts</span><span class="sxs-lookup"><span data-stu-id="e3ed3-109">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="e3ed3-110">Der erste Schritt ist die Erstellung von Projekten für Ihre Q#-Bibliothek und für den .NET-Host, von dem Aufrufe für die in Ihrer Q#-Bibliothek definierten Vorgänge und Funktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-110">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="e3ed3-111">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Entwicklungsumgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-111">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="e3ed3-112">Wenn Sie einen anderen Editor als Visual Studio oder VS Code verwenden, befolgen Sie einfach die Schritte für die Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-112">If you are using an editor other than Visual Studio or VS Code, simply follow the command prompt steps.</span></span>

### <a name="visual-studio-code-or-command-prompt"></a>[<span data-ttu-id="e3ed3-113">Visual Studio Code oder Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="e3ed3-113">Visual Studio Code or command prompt</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="e3ed3-114">Erstellen Sie eine neue Q#-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-114">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="e3ed3-115">Erstellen Sie ein neues C#- oder F#-Konsolenprojekt.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-115">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="e3ed3-116">Fügen Sie Ihre Q#-Bibliothek als Verweis aus Ihrem Hostprogramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-116">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="e3ed3-117">[Optional] Erstellen Sie eine Projektmappe für beide Projekte.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-117">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="e3ed3-118">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="e3ed3-118">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="e3ed3-119">Erstellen Sie eine neue Q#-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-119">Create a new Q# library</span></span>
  - <span data-ttu-id="e3ed3-120">Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-120">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="e3ed3-121">Geben Sie „Q#“ in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-121">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="e3ed3-122">Wählen Sie **Q#-Bibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-122">Select **Q# Library**</span></span>
  - <span data-ttu-id="e3ed3-123">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-123">Select **Next**</span></span>
  - <span data-ttu-id="e3ed3-124">Wählen Sie einen Namen und Speicherort für Ihre Bibliothek aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-124">Choose a name and location for your library</span></span>
  - <span data-ttu-id="e3ed3-125">Stellen Sie sicher, dass die Option „Place project and solution in same directory“ (Projekt und Projektmappe im selben Verzeichnis anordnen) **deaktiviert** ist.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-125">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="e3ed3-126">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="e3ed3-126">Select **Create**</span></span>
- <span data-ttu-id="e3ed3-127">Erstellen eines neuen C#- oder F#-Hostprogramms</span><span class="sxs-lookup"><span data-stu-id="e3ed3-127">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="e3ed3-128">Navigieren Sie zu **Datei** > **Neu** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-128">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="e3ed3-129">Wählen Sie für C# bzw. F# die Option „Konsolen-App (.NET Core)“ aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-129">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="e3ed3-130">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-130">Select **Next**</span></span>
  - <span data-ttu-id="e3ed3-131">Wählen Sie unter *Projektmappe* die Option „Zur Projektmappe hinzufügen“ aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-131">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="e3ed3-132">Wählen Sie einen Namen für Ihr Hostprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-132">Choose a name for your host program</span></span>
  - <span data-ttu-id="e3ed3-133">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="e3ed3-133">Select **Create**</span></span>

***

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="e3ed3-134">Durchführen von Q#-Aufrufen über .NET</span><span class="sxs-lookup"><span data-stu-id="e3ed3-134">Calling into Q# from .NET</span></span>

<span data-ttu-id="e3ed3-135">Nachdem Sie Ihre Projekte gemäß der obigen Anleitung eingerichtet haben, können Sie über Ihre .NET-Konsolenanwendung Q#-Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-135">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="e3ed3-136">Der Q#-Compiler erstellt .NET-Klassen für alle Q#-Vorgänge und -Funktionen, die das Ausführen von Quantenprogrammen in einem Simulator ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-136">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="e3ed3-137">Das [Beispiel zur .NET-Interoperabilität](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) enthält das folgende Beispiel für einen Q#-Vorgang:</span><span class="sxs-lookup"><span data-stu-id="e3ed3-137">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="e3ed3-138">Um diesen Vorgang über .NET in einem Quantensimulator aufzurufen, können Sie die Methode `Run` der .NET-Klasse `RunAlgorithm` verwenden, die vom Q#-Compiler generiert wird:</span><span class="sxs-lookup"><span data-stu-id="e3ed3-138">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="e3ed3-139">C#</span><span class="sxs-lookup"><span data-stu-id="e3ed3-139">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="e3ed3-140">F#</span><span class="sxs-lookup"><span data-stu-id="e3ed3-140">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="e3ed3-141">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e3ed3-141">Next steps</span></span>

<span data-ttu-id="e3ed3-142">Nachdem Sie das Quantum Development Kit nun sowohl für Q#-Anwendungen als auch für die Interoperabilität mit .NET eingerichtet haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3ed3-142">Now that you have the Quantum Development Kit set up for both Q# applications and interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
