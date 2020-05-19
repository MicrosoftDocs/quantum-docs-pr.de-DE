---
title: Installieren des Microsoft Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für verschiedene Umgebungen installieren.
author: natke
ms.author: nakersha
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2041b90ba021b7640615d73c35841cc21f025ac0
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426473"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="2b7b4-103">Installieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="2b7b4-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="2b7b4-104">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="2b7b4-105">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b7b4-105">The QDK consists of:</span></span>

- <span data-ttu-id="2b7b4-106">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="2b7b4-106">The Q# programming language</span></span>
- <span data-ttu-id="2b7b4-107">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="2b7b4-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="2b7b4-108">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="2b7b4-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="2b7b4-109">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="2b7b4-109">Tools to facilitate your development</span></span>

<span data-ttu-id="2b7b4-110">Q#-Programme können als eigenständige Anwendungen unter Verwendung von Visual Studio Code oder Visual Studio oder über Jupyter Notebook-Instanzen mit dem IQ#-Jupyter-Kernel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="2b7b4-111">Darüber hinaus können sie mit einem in einer .NET-Sprache (in der Regel C#) oder in Python geschriebenen Hostprogramm kombiniert werden, um das Aufrufen von Quantenvorgängen in einem klassischen Programm zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="2b7b4-112">Das QDK ist für mehrere Entwicklungsumgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="2b7b4-113">Wählen Sie Ihr bevorzugtes Setup aus:</span><span class="sxs-lookup"><span data-stu-id="2b7b4-113">Select your preferred setup from:</span></span>

<span data-ttu-id="2b7b4-114">[**Entwickeln mit Q#-Befehlszeilenanwendungen:** ](xref:microsoft.quantum.install.standalone) Verwenden Sie diesen Ansatz, wenn Sie Q# über die Befehlszeile nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-114">[**Develop with Q# command line applications**](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="2b7b4-115">Dies erfordert im Gegensatz zu den folgenden Optionen keinen Treiber und kein Hostprogramm.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="2b7b4-116">[**Entwickeln mit Q#-Jupyter Notebook-Instanzen:** ](xref:microsoft.quantum.install.jupyter) Verwenden Sie diese Umgebung, um Q#-Code in Zellen mit eingebettetem Text auszuführen oder interaktive Tutorials zum Thema Quantencomputing zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-116">[**Develop with Q# Jupyter Notebooks**](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="2b7b4-117">[**Entwickeln mit Q# und Python:** ](xref:microsoft.quantum.install.python) Verwenden Sie diese Option, wenn Sie Python und Q# miteinander kombinieren möchten, um ein Python-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-117">[**Develop with Q# and Python**](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="2b7b4-118">[**Entwickeln mit Q# und .NET:** ](xref:microsoft.quantum.install.cs) Kombinieren Sie C#, F# oder VB.NET mit Q#, um ein .NET-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b7b4-118">[**Develop with Q# and .NET**](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
