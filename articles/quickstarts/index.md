---
title: Einrichten des Microsoft Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für verschiedene Umgebungen einrichten.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834481"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="8eb7c-103">Einrichten des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="8eb7c-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="8eb7c-104">Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für Ihre Umgebung einrichten, um mit der Quantenprogrammierung beginnen zu können.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="8eb7c-105">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8eb7c-105">The QDK consists of:</span></span>

- <span data-ttu-id="8eb7c-106">Die Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="8eb7c-106">The Q# programming language</span></span>
- <span data-ttu-id="8eb7c-107">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="8eb7c-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="8eb7c-108">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="8eb7c-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="8eb7c-109">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="8eb7c-109">Tools to facilitate your development</span></span>

<span data-ttu-id="8eb7c-110">Q#-Programme können als eigenständige Anwendungen unter Verwendung von Visual Studio Code oder Visual Studio oder über Jupyter Notebook-Instanzen mit dem IQ#-Jupyter-Kernel ausgeführt werden. Alternativ können sie mit einem in Python oder in einer .NET-Sprache (C#, F#) geschriebenen Hostprogramm kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="8eb7c-111">Darüber hinaus können Sie Q#-Programme auch online unter Verwendung von [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) oder [Docker](#use-the-qdk-with-docker) ausführen.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="8eb7c-112">Optionen für die QDK-Einrichtung</span><span class="sxs-lookup"><span data-stu-id="8eb7c-112">Options for setting up the QDK</span></span>

<span data-ttu-id="8eb7c-113">Das QDK kann auf drei Arten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="8eb7c-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="8eb7c-114">Lokales Installieren des QDK</span><span class="sxs-lookup"><span data-stu-id="8eb7c-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="8eb7c-115">Verwenden des QDK online</span><span class="sxs-lookup"><span data-stu-id="8eb7c-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="8eb7c-116">Verwenden eines QDK-Docker-Images</span><span class="sxs-lookup"><span data-stu-id="8eb7c-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="8eb7c-117">Lokales Installieren des QDK</span><span class="sxs-lookup"><span data-stu-id="8eb7c-117">Install the QDK locally</span></span>

<span data-ttu-id="8eb7c-118">Sie können Q#-Code in den meisten gängigen IDEs entwickeln und Q# in andere Sprachen wie Python und .NET (C#, F#) integrieren.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

|&nbsp; | <span data-ttu-id="8eb7c-119">**VS Code<br>(ab 2019)**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-119">**VS Code<br>(2019 or later)**</span></span>| <span data-ttu-id="8eb7c-120">**Visual Studio<br>(ab 2019)**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-120">**Visual Studio<br>(2019 or later)**</span></span> | <span data-ttu-id="8eb7c-121">**Jupyter-Notebooks**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-121">**Jupyter Notebooks**</span></span> | <span data-ttu-id="8eb7c-122">**Befehlszeile**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-122">**Command line**</span></span>|
|:-----|:-----:|:-----:|:-----:|:-----:|
|<span data-ttu-id="8eb7c-123">**Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-123">**OS**</span></span> |<span data-ttu-id="8eb7c-124">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="8eb7c-124">Windows, macOS, Linux</span></span> |<span data-ttu-id="8eb7c-125">Nur Windows</span><span class="sxs-lookup"><span data-stu-id="8eb7c-125">Windows only</span></span> |<span data-ttu-id="8eb7c-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="8eb7c-126">Windows, macOS, Linux</span></span> |<span data-ttu-id="8eb7c-127">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="8eb7c-127">Windows, macOS, Linux</span></span> |
|<br><span data-ttu-id="8eb7c-128">**Q# (eigenständig)**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-128">**Q# standalone**</span></span> |<br>[<span data-ttu-id="8eb7c-129">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-129">Install</span></span>](xref:microsoft.quantum.install.standalone) |<br> [<span data-ttu-id="8eb7c-130">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-130">Install</span></span>](xref:microsoft.quantum.install.standalone)  |<br> [<span data-ttu-id="8eb7c-131">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-131">Install</span></span>](xref:microsoft.quantum.install.jupyter) |<br>[<span data-ttu-id="8eb7c-132">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-132">Install</span></span>](xref:microsoft.quantum.install.standalone)|
|<span data-ttu-id="8eb7c-133">**Q# und Python**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-133">**Q#  and Python**</span></span> |[<span data-ttu-id="8eb7c-134">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-134">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="8eb7c-135">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-135">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="8eb7c-136">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-136">Install</span></span>](xref:microsoft.quantum.install.jupyter) |[<span data-ttu-id="8eb7c-137">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-137">Install</span></span>](xref:microsoft.quantum.install.python) |
|<span data-ttu-id="8eb7c-138">**Q# und .NET (C#, F#)**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-138">**Q# and .NET (C#, F#)**</span></span>|[<span data-ttu-id="8eb7c-139">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-139">Install</span></span>](xref:microsoft.quantum.install.cs) |[<span data-ttu-id="8eb7c-140">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-140">Install</span></span>](xref:microsoft.quantum.install.cs)|<span data-ttu-id="8eb7c-141">&#10006;</span><span class="sxs-lookup"><span data-stu-id="8eb7c-141">&#10006;</span></span> |[<span data-ttu-id="8eb7c-142">Installieren</span><span class="sxs-lookup"><span data-stu-id="8eb7c-142">Install</span></span>](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a><span data-ttu-id="8eb7c-143">Verwenden des QDK online</span><span class="sxs-lookup"><span data-stu-id="8eb7c-143">Use the QDK Online</span></span>

<span data-ttu-id="8eb7c-144">Die Entwicklung von Q#-Code ist auch ganz ohne lokale Installation möglich. Hierzu stehen folgende Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="8eb7c-144">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="8eb7c-145">Resource</span><span class="sxs-lookup"><span data-stu-id="8eb7c-145">Resource</span></span>|<span data-ttu-id="8eb7c-146">Vorteile</span><span class="sxs-lookup"><span data-stu-id="8eb7c-146">Advantages</span></span>|<span data-ttu-id="8eb7c-147">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="8eb7c-147">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="8eb7c-148">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-148">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="8eb7c-149">Umfangreiche Onlineentwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="8eb7c-149">A rich online development environment</span></span>  |<span data-ttu-id="8eb7c-150">Azure-Abonnement und entsprechender Tarif erforderlich</span><span class="sxs-lookup"><span data-stu-id="8eb7c-150">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="8eb7c-151">**Binder**</span><span class="sxs-lookup"><span data-stu-id="8eb7c-151">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="8eb7c-152">Kostenlose onlinebasierte Notebookumgebung</span><span class="sxs-lookup"><span data-stu-id="8eb7c-152">Free online notebook experience</span></span> |<span data-ttu-id="8eb7c-153">Keine Persistenz</span><span class="sxs-lookup"><span data-stu-id="8eb7c-153">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="8eb7c-154">Verwenden des QDK mit Docker</span><span class="sxs-lookup"><span data-stu-id="8eb7c-154">Use the QDK with Docker</span></span>

<span data-ttu-id="8eb7c-155">Sie können unser QDK-Docker-Image in Ihrer lokalen Docker-Installation oder in der Cloud über einen beliebigen Dienst nutzen, der Docker-Images unterstützt. Ein Beispiel wäre etwa ACI.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-155">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="8eb7c-156">Das IQ#-Docker-Image steht unter https://github.com/microsoft/iqsharp/#using-iq-as-a-container zum Download bereit.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-156">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="8eb7c-157">Docker kann auch mit einem Visual Studio Code-Remoteentwicklungscontainer verwendet werden, um schnell Entwicklungsumgebungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-157">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="8eb7c-158">Weitere Informationen zu VS Code-Entwicklungscontainern finden Sie unter https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-158">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8eb7c-159">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8eb7c-159">Next steps</span></span>

<span data-ttu-id="8eb7c-160">Die Workflows für jede dieser Einrichtungen werden in [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs) beschrieben und verglichen.</span><span class="sxs-lookup"><span data-stu-id="8eb7c-160">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
