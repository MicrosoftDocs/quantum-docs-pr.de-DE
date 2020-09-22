---
title: Quantum Development Kit-Bibliotheken
description: Enthält eine Übersicht über die Bibliotheken für die Bereiche Standard, Chemie und Numerik, die im Microsoft Quantum Development Kit enthalten sind.
author: cgranade
ms.author: chgranad
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries
no-loc:
- Q#
- $$v
ms.openlocfilehash: 90672b6ec78bf8305bdb3ab8326002cf8ce34bfe
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835722"
---
# <a name="overview-of-no-locq-libraries"></a><span data-ttu-id="eaf42-103">Übersicht über Q#-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="eaf42-103">Overview of Q# Libraries</span></span>
<span data-ttu-id="eaf42-104">Das Quantum Development Kit wird mit mehreren Bibliotheken bereitgestellt, um die Entwicklung von Quantenanwendungen in Q# zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="eaf42-104">The Quantum Development Kit is provided with several libraries to make it easier to develop quantum applications in Q#.</span></span>
<span data-ttu-id="eaf42-105">In diesem Abschnitt der Dokumentation werden diese Bibliotheken und ihre Verwendung in Programmen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eaf42-105">In this section of the documentation, we describe these libraries and how to use them in your programs.</span></span>

- <span data-ttu-id="eaf42-106">[**Standardbibliotheken:** ](xref:microsoft.quantum.libraries.standard.intro) In diesem Abschnitt werden das Präludium (definiert die Schnittstelle zwischen Q#-Programmen und Zielcomputern) und der Kanon (eine Q#-Bibliothek mit universellen Operationen und Funktionen zum Schreiben von Q#-Programmen) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eaf42-106">[**Standard libraries**](xref:microsoft.quantum.libraries.standard.intro): This section describes the prelude, which defines the interface between Q# programs and target machines, and the canon, a Q# library that provides general-purpose operations and functions for use in writing Q# programs.</span></span>
- <span data-ttu-id="eaf42-107">[**Quantenchemiebibliothek:** ](xref:microsoft.quantum.chemistry.concepts.intro) In diesem Abschnitt wird die Quantenchemiebibliothek beschrieben, die ein Datenmodell zum Laden von Darstellungen von Fermion-Hamiltonoperatoren sowie Vorgänge und Funktionen der Quantensimulation bereitstellt, die mit diesen Darstellungen interagieren können.</span><span class="sxs-lookup"><span data-stu-id="eaf42-107">[**Quantum chemistry library**](xref:microsoft.quantum.chemistry.concepts.intro): This section describes the quantum chemistry library, which provides a data model for loading representations of fermionic Hamiltonians and quantum simulation operations and functions which act on these representations.</span></span>
- <span data-ttu-id="eaf42-108">[**Numerische Quantenbibliothek:** ](xref:microsoft.quantum.numerics.intro) In diesem Abschnitt wird die numerische Quantenbibliothek beschrieben, die Implementierungen für eine große Anzahl mathematischer Funktionen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="eaf42-108">[**Quantum numerics library**](xref:microsoft.quantum.numerics.intro): This section describes the quantum numerics library, which provides implementations for a host of mathematical functions.</span></span> <span data-ttu-id="eaf42-109">Sie unterstützt (signierte und nicht signierte) Integer und Festkommadarstellungen.</span><span class="sxs-lookup"><span data-stu-id="eaf42-109">It supports integer (signed & unsigned) and fixed-point representations.</span></span>
- <span data-ttu-id="eaf42-110">[**Quantum Machine Learning-Bibliothek**](xref:microsoft.quantum.machine-learning.concepts.intro): In diesem Abschnitt wird die Quantum Machine Learning-Bibliothek beschrieben. Sie verfügt über eine Implementierung der sequenziellen Klassifizierer, die Quantencomputing nutzen, um Daten zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="eaf42-110">[**Quantum machine learning library**](xref:microsoft.quantum.machine-learning.concepts.intro): This section describes the quantum machine learning library, which provides an implementation of the sequential classifiers that take advantage of quantum computing to understand data.</span></span>

<span data-ttu-id="eaf42-111">Quellen für diese Bibliotheken und Codebeispiele finden Sie auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="eaf42-111">Sources of the libraries as well as code samples can be obtained from GitHub.</span></span>
<span data-ttu-id="eaf42-112">Weitere Informationen finden Sie unter [Lizenzierung](xref:microsoft.quantum.libraries.licensing).</span><span class="sxs-lookup"><span data-stu-id="eaf42-112">See [Licensing](xref:microsoft.quantum.libraries.licensing) for further information.</span></span> <span data-ttu-id="eaf42-113">Beachten Sie, dass Paketverweise („Binärdateien“) ebenfalls für die Bibliotheken zur Verfügung stehen und eine weitere Möglichkeit zum Einschließen der Bibliotheken in Projekte darstellen.</span><span class="sxs-lookup"><span data-stu-id="eaf42-113">Note that package references ("binaries") are available also for the libraries and offer another way of including the libraries in projects.</span></span>
<span data-ttu-id="eaf42-114">Die Verwendung von [NuGet](https://nuget.org) ist eine praktische Option, um sie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eaf42-114">A convenient way of obtaining them is via [NuGet](https://nuget.org).</span></span>
