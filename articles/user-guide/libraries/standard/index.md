---
title: Einführung in Q#-Standardbibliotheken von Microsoft
description: Hier finden Sie Informationen zu den Q#-Standardbibliotheken von Microsoft, mit denen die Vorgänge, Funktionen und Datentypen definiert werden, die in Quantenprogrammen zum Einsatz kommen.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 58e271fefba84e45c5558eeee066bc37c22bf63b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858317"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a><span data-ttu-id="a0e74-103">Einführung in die Q#-Standardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="a0e74-103">Introduction to the Q# Standard Libraries</span></span>

<span data-ttu-id="a0e74-104">Q# wird von verschiedenen praktischen Vorgängen, Funktionen und benutzerdefinierten Typen unterstützt, die die Q#-*Standardbibliotheken* umfassen.</span><span class="sxs-lookup"><span data-stu-id="a0e74-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard libraries*.</span></span>
<span data-ttu-id="a0e74-105">Das bei der [Installation und Überprüfung](xref:microsoft.quantum.install) installierte [`Microsoft.Quantum.Development.Kit`-NuGet-Paket](https://www.nuget.org/packages/microsoft.quantum.development.kit) stellt den Q#-Compiler sowie Teile der Standardbibliothek bereit, die vom Zielcomputer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0e74-105">The [`Microsoft.Quantum.Development.Kit` NuGet package](https://www.nuget.org/packages/microsoft.quantum.development.kit) installed during [installation and validation](xref:microsoft.quantum.install) provides the Q# compiler, and parts of the standard library that are implemented by the target machines.</span></span>
<span data-ttu-id="a0e74-106">Das [`Microsoft.Quantum.Standard`-Paket](https://www.nuget.org/packages/microsoft.quantum.standard) stellt den Teil der Q#-Standardbibliotheken bereit, der auf mehrere Zielcomputer übertragbar ist.</span><span class="sxs-lookup"><span data-stu-id="a0e74-106">The [`Microsoft.Quantum.Standard` package](https://www.nuget.org/packages/microsoft.quantum.standard) provides the portion of the Q# standard libraries that are portable across target machines.</span></span>

<span data-ttu-id="a0e74-107">Die durch die Q#-Standardbibliotheken definierten Symbole werden in der [API-Dokumentation](xref:microsoft.quantum.apiref-intro) wesentlich ausführlicher definiert.</span><span class="sxs-lookup"><span data-stu-id="a0e74-107">The symbols defined by the Q# standard libraries are defined in much greater and more exhaustive detail in the [API documentation](xref:microsoft.quantum.apiref-intro).</span></span>

<span data-ttu-id="a0e74-108">In den folgenden Abschnitten werden die wichtigsten Funktionen der einzelnen Teile der Standardbibliothek beschrieben. Außerdem wird erläutert, wie die einzelnen Funktionen in der Praxis verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a0e74-108">In the following sections, we will outline the most salient features of each part of the standard library and provide some context about how each feature might be used in practice.</span></span>
