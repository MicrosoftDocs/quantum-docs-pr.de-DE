---
title: Einrichten des Microsoft Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für verschiedene Umgebungen einrichten.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: quickstart
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15067f1762f4468345beee38c98e1b943081fc1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859023"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="02ce3-103">Einrichten des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="02ce3-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="02ce3-104">Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für Ihre Umgebung einrichten, um mit der Quantenprogrammierung beginnen zu können.</span><span class="sxs-lookup"><span data-stu-id="02ce3-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="02ce3-105">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02ce3-105">The QDK consists of:</span></span>

- <span data-ttu-id="02ce3-106">Die Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="02ce3-106">The Q# programming language</span></span>
- <span data-ttu-id="02ce3-107">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="02ce3-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="02ce3-108">API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind</span><span class="sxs-lookup"><span data-stu-id="02ce3-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="02ce3-109">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="02ce3-109">Tools to facilitate your development</span></span>

<span data-ttu-id="02ce3-110">Q#-Programme können als eigenständige Anwendungen unter Verwendung von Visual Studio Code oder Visual Studio oder über Jupyter Notebook-Instanzen mit dem IQ#-Jupyter-Kernel ausgeführt werden. Alternativ können sie mit einem in Python oder in einer .NET-Sprache (C#, F#) geschriebenen Hostprogramm kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="02ce3-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="02ce3-111">Darüber hinaus können Sie Q#-Programme auch online unter Verwendung von [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) oder [Docker](#use-the-qdk-with-docker) ausführen.</span><span class="sxs-lookup"><span data-stu-id="02ce3-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="02ce3-112">Optionen für die QDK-Einrichtung</span><span class="sxs-lookup"><span data-stu-id="02ce3-112">Options for setting up the QDK</span></span>

<span data-ttu-id="02ce3-113">Das QDK kann auf drei Arten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="02ce3-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="02ce3-114">Lokales Installieren des QDK</span><span class="sxs-lookup"><span data-stu-id="02ce3-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="02ce3-115">Verwenden des QDK online</span><span class="sxs-lookup"><span data-stu-id="02ce3-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="02ce3-116">Verwenden eines QDK-Docker-Images</span><span class="sxs-lookup"><span data-stu-id="02ce3-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="02ce3-117">Lokales Installieren des QDK</span><span class="sxs-lookup"><span data-stu-id="02ce3-117">Install the QDK locally</span></span>

<span data-ttu-id="02ce3-118">Sie können Q#-Code in den meisten gängigen IDEs entwickeln und Q# in andere Sprachen wie Python und .NET (C#, F#) integrieren.</span><span class="sxs-lookup"><span data-stu-id="02ce3-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><span data-ttu-id="02ce3-119"><b>VS-Code</span><span class="sxs-lookup"><span data-stu-id="02ce3-119"><b>VS Code</span></span><br><span data-ttu-id="02ce3-120">(2019 oder höher)</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-120">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><span data-ttu-id="02ce3-121"><b>Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02ce3-121"><b>Visual Studio</span></span><br><span data-ttu-id="02ce3-122">(2019 oder höher)</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-122">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><span data-ttu-id="02ce3-123"><b>Jupyter-Notebooks</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-123"><b>Jupyter Notebooks</b></span></span></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><span data-ttu-id="02ce3-124"><b>Befehlszeile</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-124"><b>Command line</b></span></span></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><span data-ttu-id="02ce3-125"><b>Betriebssystemunterstützung :</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-125"><b>OS support:</b></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="02ce3-126">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="02ce3-127">Nur Windows</span><span class="sxs-lookup"><span data-stu-id="02ce3-127">Windows only</span></span></td>
        <td align="center"><span data-ttu-id="02ce3-128">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="02ce3-128">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="02ce3-129">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="02ce3-129">Windows, macOS, Linux</span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><span data-ttu-id="02ce3-130"><b>Q# (eigenständig)</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-130"><b>Q# standalone</b></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-131"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-131"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-132"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-132"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-133"><a href="xref:microsoft.quantum.install.jupyter">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-133"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-134"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-134"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><span data-ttu-id="02ce3-135"><b>Q# und Python</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-135"><b>Q# and Python</b></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-136"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-136"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-137"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-137"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-138"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-138"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-139"><a href="xref:microsoft.quantum.install.python">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-139"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><span data-ttu-id="02ce3-140"><b>Q# und .NET (C#, F#)</b></span><span class="sxs-lookup"><span data-stu-id="02ce3-140"><b>Q# and .NET (C#, F#)</b></span></span></td> 
        <td align="center"><span data-ttu-id="02ce3-141"><a href="xref:microsoft.quantum.install.cs">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-141"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-142"><a href="xref:microsoft.quantum.install.cs">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-142"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="02ce3-143">&#10006;</span><span class="sxs-lookup"><span data-stu-id="02ce3-143">&#10006;</span></span></td>
        <td align="center"><span data-ttu-id="02ce3-144"><a href="xref:microsoft.quantum.install.cs">Installieren</a></span><span class="sxs-lookup"><span data-stu-id="02ce3-144"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a><span data-ttu-id="02ce3-145">Verwenden des QDK online</span><span class="sxs-lookup"><span data-stu-id="02ce3-145">Use the QDK Online</span></span>

<span data-ttu-id="02ce3-146">Die Entwicklung von Q#-Code ist auch ganz ohne lokale Installation möglich. Hierzu stehen folgende Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="02ce3-146">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="02ce3-147">Resource</span><span class="sxs-lookup"><span data-stu-id="02ce3-147">Resource</span></span>|<span data-ttu-id="02ce3-148">Vorteile</span><span class="sxs-lookup"><span data-stu-id="02ce3-148">Advantages</span></span>|<span data-ttu-id="02ce3-149">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="02ce3-149">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="02ce3-150">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="02ce3-150">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="02ce3-151">Umfangreiche Onlineentwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="02ce3-151">A rich online development environment</span></span>  |<span data-ttu-id="02ce3-152">Azure-Abonnement und entsprechender Tarif erforderlich</span><span class="sxs-lookup"><span data-stu-id="02ce3-152">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="02ce3-153">**Binder**</span><span class="sxs-lookup"><span data-stu-id="02ce3-153">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="02ce3-154">Kostenlose onlinebasierte Notebookumgebung</span><span class="sxs-lookup"><span data-stu-id="02ce3-154">Free online notebook experience</span></span> |<span data-ttu-id="02ce3-155">Keine Persistenz</span><span class="sxs-lookup"><span data-stu-id="02ce3-155">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="02ce3-156">Verwenden des QDK mit Docker</span><span class="sxs-lookup"><span data-stu-id="02ce3-156">Use the QDK with Docker</span></span>

<span data-ttu-id="02ce3-157">Sie können unser QDK-Docker-Image in Ihrer lokalen Docker-Installation oder in der Cloud über einen beliebigen Dienst nutzen, der Docker-Images unterstützt. Ein Beispiel wäre etwa ACI.</span><span class="sxs-lookup"><span data-stu-id="02ce3-157">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="02ce3-158">Das IQ#-Docker-Image steht unter https://github.com/microsoft/iqsharp/#using-iq-as-a-container zum Download bereit.</span><span class="sxs-lookup"><span data-stu-id="02ce3-158">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="02ce3-159">Docker kann auch mit einem Visual Studio Code-Remoteentwicklungscontainer verwendet werden, um schnell Entwicklungsumgebungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="02ce3-159">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="02ce3-160">Weitere Informationen zu VS Code-Entwicklungscontainern finden Sie unter https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="02ce3-160">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="02ce3-161">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="02ce3-161">Next steps</span></span>

<span data-ttu-id="02ce3-162">Die Workflows für jede dieser Einrichtungen werden in [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs) beschrieben und verglichen.</span><span class="sxs-lookup"><span data-stu-id="02ce3-162">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
