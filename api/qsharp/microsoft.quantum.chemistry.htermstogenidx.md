---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Htermstogenidx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 73324a48cc4b42de0d5d8618ad9e833d289125f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703560"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="fc03a-102">Htermstogenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="fc03a-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="fc03a-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fc03a-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="fc03a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fc03a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fc03a-105">Konvertiert einen Index in einen hamiltona-Begriff im `HTerm[]` Datenformat in einen generatorindex.</span><span class="sxs-lookup"><span data-stu-id="fc03a-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="fc03a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fc03a-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="fc03a-107">Daten: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="fc03a-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="fc03a-108">Eingabedaten im- `HTerm[]` Format.</span><span class="sxs-lookup"><span data-stu-id="fc03a-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="fc03a-109">Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fc03a-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="fc03a-110">Zusätzliche Informationen, die generatorindex hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fc03a-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="fc03a-111">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fc03a-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fc03a-112">Index für einen Begriff von hamiltonan</span><span class="sxs-lookup"><span data-stu-id="fc03a-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="fc03a-113">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="fc03a-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="fc03a-114">Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `data[idx]` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .</span><span class="sxs-lookup"><span data-stu-id="fc03a-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>