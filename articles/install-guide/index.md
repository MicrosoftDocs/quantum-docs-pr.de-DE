---
title: Installieren des Microsoft Quantum Development Kit (QDK)
description: Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit für C#-, Python- und Jupyter Notebook-Umgebungen installieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 5fafb736f34d27f9233370a0a8a66c0613606048
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904773"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="5610b-103">Installieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="5610b-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="5610b-104">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können.</span><span class="sxs-lookup"><span data-stu-id="5610b-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="5610b-105">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5610b-105">The QDK consists of:</span></span>

- <span data-ttu-id="5610b-106">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="5610b-106">the Q# programming language</span></span>
- <span data-ttu-id="5610b-107">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="5610b-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="5610b-108">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="5610b-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="5610b-109">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="5610b-109">tools to facilitate your development</span></span>

<span data-ttu-id="5610b-110">Q#-Programme sind häufig mit einem Hostprogramm gekoppelt, das in einer .NET-Sprache (normalerweise C#) oder Python geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="5610b-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="5610b-111">Dies ermöglicht es uns, Quantenvorgänge aus einem klassischen Programm aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5610b-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="5610b-112">Zusätzlich wird über das QDK die Q#-Unterstützung für Jupyter Notebooks mit dem IQ#-Jupyter-Kernel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5610b-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="5610b-113">Das QDK ist für mehrere Entwicklungsumgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5610b-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="5610b-114">Wählen Sie in den folgenden Abschnitten Ihre bevorzugte Option aus:</span><span class="sxs-lookup"><span data-stu-id="5610b-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="5610b-115">[Installation von Q# für C#:](xref:microsoft.quantum.install.cs) Wählen Sie diese Umgebung aus, wenn Sie C# und Q# kombinieren möchten, um ein C#-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5610b-115">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="5610b-116">[Installation von Q# für Python:](xref:microsoft.quantum.install.python) Wählen Sie diese Umgebung aus, wenn Sie Python und Q# kombinieren möchten, um ein Python-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5610b-116">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="5610b-117">[Installation von Q# für Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) Wählen Sie diese Umgebung aus, um Q#-Code in Zellen mit eingebettetem Text auszuführen oder interaktive Tutorials zum Thema Quantencomputing zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5610b-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="5610b-118">Wählen Sie diese Umgebung nicht aus, wenn Sie Q# mit einem externen klassischen Hostprogramm kombinieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5610b-118">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
