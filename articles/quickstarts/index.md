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
ms.openlocfilehash: f0c3df1998f9b64ff6544867b83a7afe52b6f46d
ms.sourcegitcommit: fd57a845d013ae4578715d04b1ed1edc1c8ff6b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "94870820"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="474bc-103">Einrichten des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="474bc-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="474bc-104">Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für Ihre Umgebung einrichten, um mit der Quantenprogrammierung beginnen zu können.</span><span class="sxs-lookup"><span data-stu-id="474bc-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="474bc-105">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="474bc-105">The QDK consists of:</span></span>

- <span data-ttu-id="474bc-106">Die Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="474bc-106">The Q# programming language</span></span>
- <span data-ttu-id="474bc-107">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="474bc-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="474bc-108">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="474bc-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="474bc-109">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="474bc-109">Tools to facilitate your development</span></span>

<span data-ttu-id="474bc-110">Q#-Programme können als eigenständige Anwendungen unter Verwendung von Visual Studio Code oder Visual Studio oder über Jupyter Notebook-Instanzen mit dem IQ#-Jupyter-Kernel ausgeführt werden. Alternativ können sie mit einem in Python oder in einer .NET-Sprache (C#, F#) geschriebenen Hostprogramm kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="474bc-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="474bc-111">Darüber hinaus können Sie Q#-Programme auch online unter Verwendung von [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) oder [Docker](#use-the-qdk-with-docker) ausführen.</span><span class="sxs-lookup"><span data-stu-id="474bc-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="474bc-112">Optionen für die QDK-Einrichtung</span><span class="sxs-lookup"><span data-stu-id="474bc-112">Options for setting up the QDK</span></span>

<span data-ttu-id="474bc-113">Das QDK kann auf drei Arten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="474bc-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="474bc-114">Lokales Installieren des QDK</span><span class="sxs-lookup"><span data-stu-id="474bc-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="474bc-115">Verwenden des QDK online</span><span class="sxs-lookup"><span data-stu-id="474bc-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="474bc-116">Verwenden eines QDK-Docker-Images</span><span class="sxs-lookup"><span data-stu-id="474bc-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="474bc-117">Lokales Installieren des QDK</span><span class="sxs-lookup"><span data-stu-id="474bc-117">Install the QDK locally</span></span>

<span data-ttu-id="474bc-118">Sie können Q#-Code in den meisten gängigen IDEs entwickeln und Q# in andere Sprachen wie Python und .NET (C#, F#) integrieren.</span><span class="sxs-lookup"><span data-stu-id="474bc-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><span data-ttu-id="474bc-119"><b>VS-Code</span><span class="sxs-lookup"><span data-stu-id="474bc-119"><b>VS Code</span></span><br><span data-ttu-id="474bc-120">(2019 oder höher)</b></span><span class="sxs-lookup"><span data-stu-id="474bc-120">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="VS Studio" width="50"/><br><span data-ttu-id="474bc-121"><b>VS Studio</span><span class="sxs-lookup"><span data-stu-id="474bc-121"><b>VS Studio</span></span><br><span data-ttu-id="474bc-122">(2019 oder höher)</b></span><span class="sxs-lookup"><span data-stu-id="474bc-122">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><span data-ttu-id="474bc-123"><b>Jupyter-Notebooks</b></span><span class="sxs-lookup"><span data-stu-id="474bc-123"><b>Jupyter Notebooks</b></span></span></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><span data-ttu-id="474bc-124"><b>Befehlszeile</b></span><span class="sxs-lookup"><span data-stu-id="474bc-124"><b>Command line</b></span></span></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><span data-ttu-id="474bc-125"><b>Betriebssystemunterstützung :</b></span><span class="sxs-lookup"><span data-stu-id="474bc-125"><b>OS support:</b></span></span></td>
        <td align="center"><span data-ttu-id="474bc-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="474bc-126">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="474bc-127">Nur Windows</span><span class="sxs-lookup"><span data-stu-id="474bc-127">Windows only</span></span></td>
        <td align="center"><span data-ttu-id="474bc-128">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="474bc-128">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="474bc-129">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="474bc-129">Windows, macOS, Linux</span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><span data-ttu-id="474bc-130"><b>Q# (eigenständig)</b></span><span class="sxs-lookup"><span data-stu-id="474bc-130"><b>Q# standalone</b></span></span></td>
        <td align="center"><span data-ttu-id="474bc-131"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-131"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-132"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-132"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-133"><a href="xref:microsoft.quantum.install.jupyter">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-133"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-134"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-134"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><span data-ttu-id="474bc-135"><b>Q# und Python</b></span><span class="sxs-lookup"><span data-stu-id="474bc-135"><b>Q# and Python</b></span></span></td>
        <td align="center"><span data-ttu-id="474bc-136"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-136"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-137"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-137"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-138"><a href="xref:microsoft.quantum.install.jupyter">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-138"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-139"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-139"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><span data-ttu-id="474bc-140"><b>Q# und .NET (C#, F#)</b></span><span class="sxs-lookup"><span data-stu-id="474bc-140"><b>Q# and .NET (C#, F#)</b></span></span></td> 
        <td align="center"><span data-ttu-id="474bc-141"><a href="xref:microsoft.quantum.install.cs">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-141"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-142"><a href="xref:microsoft.quantum.install.cs">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-142"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="474bc-143">&#10006;</span><span class="sxs-lookup"><span data-stu-id="474bc-143">&#10006;</span></span></td>
        <td align="center"><span data-ttu-id="474bc-144"><a href="xref:microsoft.quantum.install.cs">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="474bc-144"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a><span data-ttu-id="474bc-145">Verwenden des QDK online</span><span class="sxs-lookup"><span data-stu-id="474bc-145">Use the QDK Online</span></span>

<span data-ttu-id="474bc-146">Die Entwicklung von Q#-Code ist auch ganz ohne lokale Installation möglich. Hierzu stehen folgende Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="474bc-146">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="474bc-147">Resource</span><span class="sxs-lookup"><span data-stu-id="474bc-147">Resource</span></span>|<span data-ttu-id="474bc-148">Vorteile</span><span class="sxs-lookup"><span data-stu-id="474bc-148">Advantages</span></span>|<span data-ttu-id="474bc-149">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="474bc-149">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="474bc-150">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="474bc-150">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="474bc-151">Umfangreiche Onlineentwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="474bc-151">A rich online development environment</span></span>  |<span data-ttu-id="474bc-152">Azure-Abonnement und entsprechender Tarif erforderlich</span><span class="sxs-lookup"><span data-stu-id="474bc-152">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="474bc-153">**Binder**</span><span class="sxs-lookup"><span data-stu-id="474bc-153">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="474bc-154">Kostenlose onlinebasierte Notebookumgebung</span><span class="sxs-lookup"><span data-stu-id="474bc-154">Free online notebook experience</span></span> |<span data-ttu-id="474bc-155">Keine Persistenz</span><span class="sxs-lookup"><span data-stu-id="474bc-155">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="474bc-156">Verwenden des QDK mit Docker</span><span class="sxs-lookup"><span data-stu-id="474bc-156">Use the QDK with Docker</span></span>

<span data-ttu-id="474bc-157">Sie können unser QDK-Docker-Image in Ihrer lokalen Docker-Installation oder in der Cloud über einen beliebigen Dienst nutzen, der Docker-Images unterstützt. Ein Beispiel wäre etwa ACI.</span><span class="sxs-lookup"><span data-stu-id="474bc-157">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="474bc-158">Das IQ#-Docker-Image steht unter https://github.com/microsoft/iqsharp/#using-iq-as-a-container zum Download bereit.</span><span class="sxs-lookup"><span data-stu-id="474bc-158">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="474bc-159">Docker kann auch mit einem Visual Studio Code-Remoteentwicklungscontainer verwendet werden, um schnell Entwicklungsumgebungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="474bc-159">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="474bc-160">Weitere Informationen zu VS Code-Entwicklungscontainern finden Sie unter https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="474bc-160">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="474bc-161">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="474bc-161">Next steps</span></span>

<span data-ttu-id="474bc-162">Die Workflows für jede dieser Einrichtungen werden in [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs) beschrieben und verglichen.</span><span class="sxs-lookup"><span data-stu-id="474bc-162">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
