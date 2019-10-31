---
title: 'Q#-Standardbibliotheken: Einführung | Microsoft-Dokumentation'
description: 'Q#-Standardbibliotheken: Einführung'
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
ms.openlocfilehash: 547f4f6066e3ead627cd2a5970b1555999e988bb
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73056378"
---
# <a name="introduction-to-the-q-standard-libraries"></a><span data-ttu-id="e4f73-103">Einführung in die Q#-Standardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="e4f73-103">Introduction to the Q# Standard Libraries</span></span> #

<span data-ttu-id="e4f73-104">Q# wird von einer Reihe nützlicher Vorgänge, Funktionen und benutzerdefinierten Typen unterstützt, die die *Q#-Standardbibliotheken* umfassen.</span><span class="sxs-lookup"><span data-stu-id="e4f73-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard libraries*.</span></span>
<span data-ttu-id="e4f73-105">Das bei der [Installation und Überprüfung](xref:microsoft.quantum.install) installierte [`Microsoft.Quantum.Development.Kit`-NuGet-Paket](https://www.nuget.org/packages/microsoft.quantum.development.kit) stellt den Q#-Compiler sowie Teile der Standardbibliothek bereit, die vom Zielcomputer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4f73-105">The [`Microsoft.Quantum.Development.Kit` NuGet package](https://www.nuget.org/packages/microsoft.quantum.development.kit) installed during [installation and validation](xref:microsoft.quantum.install) provides the Q# compiler, and parts of the standard library that are implemented by the target machines.</span></span>
<span data-ttu-id="e4f73-106">Das [`Microsoft.Quantum.Standard`-Paket](https://www.nuget.org/packages/microsoft.quantum.standard) stellt den Teil der Q#-Standardbibliotheken bereit, der auf mehrere Zielcomputer übertragbar ist.</span><span class="sxs-lookup"><span data-stu-id="e4f73-106">The [`Microsoft.Quantum.Standard` package](https://www.nuget.org/packages/microsoft.quantum.standard) provides the portion of the Q# standard libraries that are portable across target machines.</span></span>

<span data-ttu-id="e4f73-107">Die durch die Q#-Standardbibliotheken definierten Symbole werden in der [API-Dokumentation](xref:microsoft.quantum.standardlibsintro) wesentlich ausführlicher definiert.</span><span class="sxs-lookup"><span data-stu-id="e4f73-107">The symbols defined by the Q# standard libraries are defined in much greater and more exhaustive detail in the [API documentation](xref:microsoft.quantum.standardlibsintro).</span></span>

<span data-ttu-id="e4f73-108">In den folgenden Abschnitten werden die wichtigsten Funktionen der einzelnen Teile der Standardbibliothek beschrieben. Außerdem wird erläutert, wie die einzelnen Funktionen in der Praxis verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e4f73-108">In the following sections, we will outline the most salient features of each part of the standard library and provide some context about how each feature might be used in practice.</span></span>
