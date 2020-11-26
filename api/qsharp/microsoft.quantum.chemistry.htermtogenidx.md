---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: Htermabgenidx-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: 59391a882fdbc55172ee93a7428c1735bbb29500
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216029"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="e7d8f-102">Htermabgenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7d8f-102">HTermToGenIdx function</span></span>

<span data-ttu-id="e7d8f-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e7d8f-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="e7d8f-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e7d8f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="e7d8f-105">Konvertiert einen hamiltona-Begriff im `HTerm` Datenformat in einen generatorindex.</span><span class="sxs-lookup"><span data-stu-id="e7d8f-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="e7d8f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e7d8f-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="e7d8f-107">Begriff: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="e7d8f-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="e7d8f-108">Eingabedaten im- `HTerm` Format.</span><span class="sxs-lookup"><span data-stu-id="e7d8f-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="e7d8f-109">Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e7d8f-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e7d8f-110">Zusätzliche Informationen, die generatorindex hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e7d8f-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="e7d8f-111">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e7d8f-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e7d8f-112">Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `term` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .</span><span class="sxs-lookup"><span data-stu-id="e7d8f-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>