---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Mcmtmask-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 3c2debbb1f2019c7188dcb00f8ac09154fd4fd4f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203015"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="0e04c-102">Mcmtmask-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="0e04c-102">MCMTMask user defined type</span></span>

<span data-ttu-id="0e04c-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="0e04c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="0e04c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0e04c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0e04c-105">Ein Typ, der ein mehrfach kontrolliertes multitarget-"deffoli"-Gate darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e04c-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="0e04c-106">Die erste ganze Zahl ist eine Bitmaske für Steuer Zeilen.</span><span class="sxs-lookup"><span data-stu-id="0e04c-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="0e04c-107">Bitindizes, die festgelegt werden, entsprechen Steuer Zeilen Indizes.</span><span class="sxs-lookup"><span data-stu-id="0e04c-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="0e04c-108">Die zweite Ganzzahl ist eine Bitmaske für die Ziellinien.</span><span class="sxs-lookup"><span data-stu-id="0e04c-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="0e04c-109">Bitindizes, die festgelegt werden, entsprechen Ziel Zeilen Indizes.</span><span class="sxs-lookup"><span data-stu-id="0e04c-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="0e04c-110">Die bitindizes beider Ganzzahlen müssen zusammen hanglos sein.</span><span class="sxs-lookup"><span data-stu-id="0e04c-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="0e04c-111">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="0e04c-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="0e04c-112">Controlmask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0e04c-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="0e04c-113">Targetmask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0e04c-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

