---
title: Verwenden zusätzlicher Q# Bibliotheken
description: Erfahren Sie, wie Sie Q# ihren Quantum-Anwendungen weitere Bibliotheken hinzufügen.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: ef88ca765a394a7092eb0a60bf6f3615c082ef6a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869578"
---
# <a name="using-additional-no-locq-libraries"></a><span data-ttu-id="81a0e-103">Verwenden zusätzlicher Q# Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="81a0e-103">Using Additional Q# Libraries</span></span>

<span data-ttu-id="81a0e-104">Das Quantum Development Kit bietet zusätzliche domänenspezifische Funktionen über _nuget-Pakete_ , die zu Ihren Projekten hinzugefügt werden können Q# .</span><span class="sxs-lookup"><span data-stu-id="81a0e-104">The Quantum Development Kit provides additional domain-specific functionality through _NuGet packages_ that can be added to your Q# projects.</span></span>

| <span data-ttu-id="81a0e-105">Q#Fern</span><span class="sxs-lookup"><span data-stu-id="81a0e-105">Q# Library</span></span>  | <span data-ttu-id="81a0e-106">NuGet-Paket</span><span class="sxs-lookup"><span data-stu-id="81a0e-106">NuGet package</span></span> | <span data-ttu-id="81a0e-107">Notizen</span><span class="sxs-lookup"><span data-stu-id="81a0e-107">Notes</span></span> |
|---------|---------|--------|
| [<span data-ttu-id="81a0e-108">Q#Standardbibliothek</span><span class="sxs-lookup"><span data-stu-id="81a0e-108">Q# standard library</span></span>](xref:microsoft.quantum.libraries.standard.intro) | [<span data-ttu-id="81a0e-109">**Microsoft. Quantum. Standard**</span><span class="sxs-lookup"><span data-stu-id="81a0e-109">**Microsoft.Quantum.Standard**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | <span data-ttu-id="81a0e-110">Standardmäßig inbegriffen</span><span class="sxs-lookup"><span data-stu-id="81a0e-110">Included by default</span></span> |
| [<span data-ttu-id="81a0e-111">Quantenchemiebibliothek</span><span class="sxs-lookup"><span data-stu-id="81a0e-111">Quantum chemistry library</span></span>](xref:microsoft.quantum.chemistry.concepts.intro) | [<span data-ttu-id="81a0e-112">**Microsoft.Quantum.Chemistry**</span><span class="sxs-lookup"><span data-stu-id="81a0e-112">**Microsoft.Quantum.Chemistry**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [<span data-ttu-id="81a0e-113">Numerische Quantenbibliothek</span><span class="sxs-lookup"><span data-stu-id="81a0e-113">Quantum numerics library</span></span>](xref:microsoft.quantum.numerics.intro) | [<span data-ttu-id="81a0e-114">**Microsoft. Quantum. Numerics**</span><span class="sxs-lookup"><span data-stu-id="81a0e-114">**Microsoft.Quantum.Numerics**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [<span data-ttu-id="81a0e-115">Quantum Machine Learning-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81a0e-115">Quantum machine learning library</span></span>](xref:microsoft.quantum.libraries.machine-learning.intro) | [<span data-ttu-id="81a0e-116">**Microsoft.Quantum.MachineLearning**</span><span class="sxs-lookup"><span data-stu-id="81a0e-116">**Microsoft.Quantum.MachineLearning**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

<span data-ttu-id="81a0e-117">Nachdem Sie das Quantum Development Kit zur Verwendung mit Ihrer bevorzugten Umgebung und Host Sprache installiert haben, können Sie ohne weitere Installation problemlos Bibliotheken zu einzelnen Projekten hinzufügen Q# .</span><span class="sxs-lookup"><span data-stu-id="81a0e-117">Once you have installed the Quantum Development Kit for use with your preferred environment and host language, you can easily add libraries to individual Q# projects without any further installation.</span></span>

> [!NOTE]
> <span data-ttu-id="81a0e-118">Einige Q# Bibliotheken funktionieren möglicherweise gut mit zusätzlichen Tools, die zusammen mit Ihren Q# Programmen verwendet werden, oder die in Ihre Host Anwendungen integriert werden.</span><span class="sxs-lookup"><span data-stu-id="81a0e-118">Some Q# libraries may work well with additional tools that work alongside your Q# programs, or that integrate with your host applications.</span></span>
> <span data-ttu-id="81a0e-119">Beispielsweise wird in den [Installationsanweisungen für die Chemie Bibliothek](xref:microsoft.quantum.chemistry.concepts.installation) beschrieben, wie Sie das [ **Microsoft. Quantum. Chemistry** -Paket](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) zusammen mit der nwchem-computegrafieplattform verwenden und wie Sie die `qdk-chem` Befehlszeilen Tools zum Arbeiten mit Quantum-Chemie-Daten installieren.</span><span class="sxs-lookup"><span data-stu-id="81a0e-119">For example, the [chemistry library installation instructions](xref:microsoft.quantum.chemistry.concepts.installation) describe how to use the [**Microsoft.Quantum.Chemistry** package](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) together with the NWChem computational chemistry platform, and how to install the `qdk-chem` command-line tools for working with quantum chemistry data.</span></span>

## <a name="no-locq-command-line-applications-or-net-interopability"></a>[<span data-ttu-id="81a0e-120">Q#Befehlszeilen Anwendungen oder .NET-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="81a0e-120">Q# command-line applications or .NET interopability</span></span>](#tab/tabid-csproj)

<span data-ttu-id="81a0e-121">**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie dem `dotnet` Projekt einen nuget-Paket Verweis hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81a0e-121">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add a NuGet package reference to your project.</span></span>
<span data-ttu-id="81a0e-122">Wenn Sie z [**. b. das Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) -Paket hinzufügen möchten, führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="81a0e-122">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package, run the following command:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

<span data-ttu-id="81a0e-123">**Visual Studio:** Wenn Sie Visual Studio 2019 oder höher verwenden, können Sie Q# mit dem nuget-Paket-Manager weitere Pakete hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81a0e-123">**Visual Studio:** If you are using Visual Studio 2019 or later, you can add additional Q# packages using the NuGet Package Manager.</span></span>
<span data-ttu-id="81a0e-124">So laden Sie ein Paket:</span><span class="sxs-lookup"><span data-stu-id="81a0e-124">To load a package:</span></span> 
1. <span data-ttu-id="81a0e-125">Wenn ein Projekt in Visual Studio geöffnet ist, wählen Sie im Menü **Projekt** die Option **nuget-Pakete verwalten...** aus.</span><span class="sxs-lookup"><span data-stu-id="81a0e-125">With a project open in Visual Studio, select **Manage NuGet Packages...** from the **Project** menu.</span></span>

2. <span data-ttu-id="81a0e-126">Klicken Sie auf **Durchsuchen**, wählen Sie **Vorabversion einschließen** aus, und suchen Sie nach dem Paketnamen "Microsoft. Quantum. Numerics".</span><span class="sxs-lookup"><span data-stu-id="81a0e-126">Click **Browse**, select **Include prerelease** and search for the package name "Microsoft.Quantum.Numerics".</span></span> <span data-ttu-id="81a0e-127">Dadurch werden die Pakete aufgelistet, die zum Herunterladen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="81a0e-127">This will list the packages available for download.</span></span>

3. <span data-ttu-id="81a0e-128">Zeigen Sie auf **Microsoft. Quantum. Numerics** , und klicken Sie auf den nach unten zeigenden Pfeil rechts neben der Versionsnummer, um das Numerics-Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="81a0e-128">Hover over **Microsoft.Quantum.Numerics** and click the downward-pointing arrow to the right of the version number to install the numerics package.</span></span>

<span data-ttu-id="81a0e-129">Weitere Informationen finden Sie im Leitfaden für die [Benutzeroberfläche des Paket-Managers](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="81a0e-129">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="81a0e-130">Alternativ können Sie die Numerics-Bibliothek mithilfe der Paket-Manager-Konsole über die Befehlszeilenschnittstelle dem Projekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81a0e-130">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Verwenden der Paket-Manager-Konsole über die Befehlszeile](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="81a0e-132">Führen Sie in der Paket-Manager-Konsole Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="81a0e-132">From the Package Manager Console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="81a0e-133">Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="81a0e-133">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

## <a name="ino-locq-notebooks"></a>[<span data-ttu-id="81a0e-134">I Q# Notebooks</span><span class="sxs-lookup"><span data-stu-id="81a0e-134">IQ# Notebooks</span></span>](#tab/tabid-notebook)

<span data-ttu-id="81a0e-135">Q#Mithilfe des [ `%package` Magic-Befehls](xref:microsoft.quantum.iqsharp.magic-ref.package)können Sie zusätzliche Pakete zur Verwendung in einem I-Notebook verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="81a0e-135">You can make additional packages available for use in an IQ# Notebook by using the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="81a0e-136">Um z. b. das [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) -Paket für die Verwendung in einem I Notebook hinzuzufügen Q# , führen Sie den folgenden Befehl in einer Notebook-Zelle aus:</span><span class="sxs-lookup"><span data-stu-id="81a0e-136">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following command in a notebook cell:</span></span>

```
%package Microsoft.Quantum.Numerics
```

<span data-ttu-id="81a0e-137">Nach diesem Befehl ist das Paket für alle Zellen im Notebook verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81a0e-137">Following this command, the package is available to any cells within the notebook.</span></span>
<span data-ttu-id="81a0e-138">Um das Paket über Q# den Code im aktuellen Arbeitsbereich verfügbar zu machen, laden Sie den Arbeitsbereich nach dem Hinzufügen des Pakets neu:</span><span class="sxs-lookup"><span data-stu-id="81a0e-138">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```
%workspace reload
```

## <a name="python-interoperability"></a>[<span data-ttu-id="81a0e-139">Interoperabilität mit Python</span><span class="sxs-lookup"><span data-stu-id="81a0e-139">Python interoperability</span></span>](#tab/tabid-python)


<span data-ttu-id="81a0e-140">Mithilfe der-Methode können Sie zusätzliche Pakete zur Verwendung in einem python-Host Programm verfügbar machen [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) .</span><span class="sxs-lookup"><span data-stu-id="81a0e-140">You can make additional packages available for use in a Python host program by using the [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) method.</span></span>
<span data-ttu-id="81a0e-141">Um z. b. das [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) -Paket für die Verwendung in einem I Notebook hinzuzufügen Q# , führen Sie den folgenden Python-Code aus:</span><span class="sxs-lookup"><span data-stu-id="81a0e-141">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following Python code:</span></span>

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

<span data-ttu-id="81a0e-142">Nach diesem Befehl wird das Paket allen Q# mit kompilierten Code zur Verfügung gestellt `qsharp.compile` .</span><span class="sxs-lookup"><span data-stu-id="81a0e-142">Following this command, the package will be made available to any Q# code compiled using `qsharp.compile`.</span></span>
<span data-ttu-id="81a0e-143">Um das Paket über Q# den Code im aktuellen Arbeitsbereich verfügbar zu machen, laden Sie den Arbeitsbereich nach dem Hinzufügen des Pakets neu:</span><span class="sxs-lookup"><span data-stu-id="81a0e-143">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```python
qsharp.reload()
```

***
