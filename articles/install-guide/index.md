---
title: Installieren des Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 0e9dd1c74316eeb1fa7bbbf657d2e78231ee4294
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036507"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="2f3d9-102">Installieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="2f3d9-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="2f3d9-103">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="2f3d9-104">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2f3d9-104">The QDK consists of:</span></span>

- <span data-ttu-id="2f3d9-105">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="2f3d9-105">the Q# programming language</span></span>
- <span data-ttu-id="2f3d9-106">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="2f3d9-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="2f3d9-107">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="2f3d9-107">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="2f3d9-108">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="2f3d9-108">tools to facilitate your development</span></span>

<span data-ttu-id="2f3d9-109">Q#-Programme sind häufig mit einem Hostprogramm gekoppelt, das in einer .NET-Sprache (normalerweise C#) oder Python geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-109">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="2f3d9-110">Dies ermöglicht es uns, Quantenvorgänge aus einem klassischen Programm aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-110">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="2f3d9-111">Zusätzlich wird über das QDK die Q#-Unterstützung für Jupyter Notebooks mit dem IQ#-Jupyter-Kernel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-111">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="2f3d9-112">Das QDK ist für mehrere Entwicklungsumgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="2f3d9-113">Wählen Sie in den folgenden Abschnitten Ihre bevorzugte Option aus:</span><span class="sxs-lookup"><span data-stu-id="2f3d9-113">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="2f3d9-114">[Installation von Q# für C#:](xref:microsoft.quantum.install.cs) Wählen Sie diese Umgebung aus, wenn Sie C# und Q# kombinieren möchten, um ein C#-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-114">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="2f3d9-115">[Installation von Q# für Python:](xref:microsoft.quantum.install.python) Wählen Sie diese Umgebung aus, wenn Sie Python und Q# kombinieren möchten, um ein Python-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-115">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="2f3d9-116">[Installation von Q# für Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) Wählen Sie diese Umgebung aus, um Q#-Code in Zellen mit eingebettetem Text auszuführen oder interaktive Tutorials zum Thema Quantencomputing zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-116">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="2f3d9-117">Wählen Sie diese Umgebung nicht aus, wenn Sie Q# mit einem externen klassischen Hostprogramm kombinieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2f3d9-117">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
