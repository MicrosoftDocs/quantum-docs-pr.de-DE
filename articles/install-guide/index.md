---
title: Installieren des Microsoft Quantum Development Kit (QDK)
description: Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit für C#-, Python- und Jupyter Notebook-Umgebungen installieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: bca700660094b91f1c0dfa03f9bce1336073ca51
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680192"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="c9baf-103">Installieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="c9baf-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="c9baf-104">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können.</span><span class="sxs-lookup"><span data-stu-id="c9baf-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="c9baf-105">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c9baf-105">The QDK consists of:</span></span>

- <span data-ttu-id="c9baf-106">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="c9baf-106">the Q# programming language</span></span>
- <span data-ttu-id="c9baf-107">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="c9baf-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="c9baf-108">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="c9baf-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="c9baf-109">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="c9baf-109">tools to facilitate your development</span></span>

<span data-ttu-id="c9baf-110">Q#-Programme sind häufig mit einem Hostprogramm gekoppelt, das in einer .NET-Sprache (normalerweise C#) oder Python geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="c9baf-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="c9baf-111">Dies ermöglicht es uns, Quantenvorgänge aus einem klassischen Programm aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9baf-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="c9baf-112">Zusätzlich wird über das QDK die Q#-Unterstützung für Jupyter Notebooks mit dem IQ#-Jupyter-Kernel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9baf-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="c9baf-113">Das QDK ist für mehrere Entwicklungsumgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9baf-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="c9baf-114">Wählen Sie in den folgenden Abschnitten Ihre bevorzugte Option aus:</span><span class="sxs-lookup"><span data-stu-id="c9baf-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="c9baf-115">[Q#-Befehlszeilenanwendung:](xref:microsoft.quantum.install.standalone) Wählen Sie diesen Ansatz, wenn Sie in der Befehlszeile mit Q# arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="c9baf-115">[Q# command line application:](xref:microsoft.quantum.install.standalone) choose this approach if you want to work with Q# from the command line.</span></span> <span data-ttu-id="c9baf-116">Dies erfordert im Gegensatz zu den folgenden Optionen keinen Treiber und kein Hostprogramm.</span><span class="sxs-lookup"><span data-stu-id="c9baf-116">This does not require a driver or a host program like the below options.</span></span>
- <span data-ttu-id="c9baf-117">[Installation von Q# für Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) Wählen Sie diese Umgebung aus, um Q#-Code in Zellen mit eingebettetem Text auszuführen oder interaktive Tutorials zum Thema Quantencomputing zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9baf-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 
- <span data-ttu-id="c9baf-118">[Entwickeln mit Q# und Python:](xref:microsoft.quantum.install.python) Wählen Sie diese Option, wenn Sie Python und Q# kombinieren möchten, um ein Python-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9baf-118">[Develop with Q# and Python:](xref:microsoft.quantum.install.python) if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="c9baf-119">[Entwickeln mit Q# und C# oder F#:](xref:microsoft.quantum.install.cs) Wählen Sie diese Option, wenn Sie C# oder F# und Q# kombinieren möchten, um ein .NET-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9baf-119">[Develop with Q# and C# or F#:](xref:microsoft.quantum.install.cs) if you want to combine C# or F# and Q# to create a .NET host program that calls Q# operations.</span></span>
