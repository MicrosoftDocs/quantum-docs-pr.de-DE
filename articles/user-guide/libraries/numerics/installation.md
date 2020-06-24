---
title: Microsoft Quantum-Numerics-Bibliothek-Installation und Validierung
description: Erfahren Sie, wie Sie die Microsoft Quantum-Numerics-Bibliothek zu Ihrer Installation von Visual Studio 2019 oder höher hinzufügen.
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: 60ee91a552fad5becf8eda437406b6e0dfba0eb4
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275190"
---
# <a name="numerics-library-installation-and-validation"></a><span data-ttu-id="5afb3-103">Installation und Validierung der Numerics-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5afb3-103">Numerics Library Installation and Validation</span></span>

<span data-ttu-id="5afb3-104">Das Quantum Development Kit bietet Unterstützung für die Numerics-Funktionalität durch das [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) nuget-Paket.</span><span class="sxs-lookup"><span data-stu-id="5afb3-104">The Quantum Development Kit provides support for numerics functionality through the [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet package.</span></span>

<span data-ttu-id="5afb3-105">**Visual Studio >= 2019:** Wenn Sie Visual Studio 2019 oder höher verwenden, können Sie das Numerics-Paket mit dem nuget-Paket-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5afb3-105">**Visual Studio >=2019:** If you are using Visual Studio 2019 or later, you can add the numerics package using the NuGet Package Manager.</span></span>
<span data-ttu-id="5afb3-106">Wählen Sie hierzu "nuget-Pakete verwalten..." aus. aus dem Menü Element "Projekt" in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5afb3-106">To do so, select "Manage NuGet Packages..." from the "Project" menu item in Visual Studio.</span></span>

<span data-ttu-id="5afb3-107">Suchen Sie auf der Registerkarte Durchsuchen nach dem Paketnamen "Microsoft. Quantum. Numerics".</span><span class="sxs-lookup"><span data-stu-id="5afb3-107">From the Browse tab, search for the package name "Microsoft.Quantum.Numerics"</span></span>

> [!NOTE]
> <span data-ttu-id="5afb3-108">Stellen Sie sicher, dass Sie "incluelease einschließen" aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5afb3-108">Make sure to tick "Include prerelease"</span></span>

<span data-ttu-id="5afb3-109">Dadurch werden die Pakete aufgelistet, die zum Herunterladen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="5afb3-109">This will list the packages available for download.</span></span>
<span data-ttu-id="5afb3-110">Wenn Sie mit dem Mauszeiger auf "Microsoft. Quantum. Numerics" zeigen, wird rechts neben der Versionsnummer ein nach unten zeigender Pfeil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5afb3-110">Hovering over "Microsoft.Quantum.Numerics" reveals a downward-pointing arrow to the right of the version number.</span></span>
<span data-ttu-id="5afb3-111">Klicken Sie auf den Pfeil, um das Numerics-Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5afb3-111">Click on the arrow in order to install the numerics package.</span></span>

<span data-ttu-id="5afb3-112">Weitere Informationen finden Sie im Leitfaden für die [Benutzeroberfläche des Paket-Managers](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="5afb3-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="5afb3-113">Alternativ können Sie die Numerics-Bibliothek mithilfe der Paket-Manager-Konsole über die Befehlszeilenschnittstelle dem Projekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5afb3-113">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Verwenden der Paket-Manager-Konsole über die Befehlszeile](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="5afb3-115">Führen Sie in der Paket-Manager-Konsole Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="5afb3-115">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="5afb3-116">Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="5afb3-116">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="5afb3-117">**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie dem `dotnet` Projekt den nuget-Paket Verweis hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="5afb3-117">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a><span data-ttu-id="5afb3-118">Überprüfen der Installation</span><span class="sxs-lookup"><span data-stu-id="5afb3-118">Verifying your installation</span></span>

<span data-ttu-id="5afb3-119">Wie das restliche Quantum Development Kit enthält die Numerics-Bibliothek Beispiele, mit deren Hilfe Sie so schnell wie möglich loslegen können.</span><span class="sxs-lookup"><span data-stu-id="5afb3-119">Like the rest of the Quantum Development Kit, the numerics library comes with samples that help you get started as quickly as possible.</span></span>
<span data-ttu-id="5afb3-120">Zum Testen Ihrer Installation mithilfe dieser Beispiele Klonen Sie das [hauptbeispielrepository](https://github.com/Microsoft/Quantum) , und führen Sie dann eines der Beispiele aus.</span><span class="sxs-lookup"><span data-stu-id="5afb3-120">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum) and then run one of the samples.</span></span>

<span data-ttu-id="5afb3-121">So führen Sie das [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="5afb3-121">To run the [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
