---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Htermstogenidx-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: dbe0718fa3b5439a2987d455fdad73731c988678
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216012"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="dc750-102">Htermstogenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc750-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="dc750-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="dc750-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="dc750-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="dc750-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="dc750-105">Konvertiert einen Index in einen hamiltona-Begriff im `HTerm[]` Datenformat in einen generatorindex.</span><span class="sxs-lookup"><span data-stu-id="dc750-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="dc750-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dc750-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="dc750-107">Daten: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="dc750-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="dc750-108">Eingabedaten im- `HTerm[]` Format.</span><span class="sxs-lookup"><span data-stu-id="dc750-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="dc750-109">Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dc750-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dc750-110">Zusätzliche Informationen, die generatorindex hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dc750-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="dc750-111">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc750-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc750-112">Index für einen Begriff von hamiltonan</span><span class="sxs-lookup"><span data-stu-id="dc750-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="dc750-113">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="dc750-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="dc750-114">Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `data[idx]` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .</span><span class="sxs-lookup"><span data-stu-id="dc750-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>