---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Mcmtmask-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725496"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="8c876-102">Mcmtmask-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="8c876-102">MCMTMask user defined type</span></span>

<span data-ttu-id="8c876-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="8c876-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="8c876-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8c876-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8c876-105">Ein Typ, der ein mehrfach kontrolliertes multitarget-"deffoli"-Gate darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c876-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="8c876-106">Die erste ganze Zahl ist eine Bitmaske für Steuer Zeilen.</span><span class="sxs-lookup"><span data-stu-id="8c876-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="8c876-107">Bitindizes, die festgelegt werden, entsprechen Steuer Zeilen Indizes.</span><span class="sxs-lookup"><span data-stu-id="8c876-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="8c876-108">Die zweite Ganzzahl ist eine Bitmaske für die Ziellinien.</span><span class="sxs-lookup"><span data-stu-id="8c876-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="8c876-109">Bitindizes, die festgelegt werden, entsprechen Ziel Zeilen Indizes.</span><span class="sxs-lookup"><span data-stu-id="8c876-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="8c876-110">Die bitindizes beider Ganzzahlen müssen zusammen hanglos sein.</span><span class="sxs-lookup"><span data-stu-id="8c876-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="8c876-111">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="8c876-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="8c876-112">Controlmask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8c876-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="8c876-113">Targetmask: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8c876-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

