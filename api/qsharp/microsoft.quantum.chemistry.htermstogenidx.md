---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: Htermstogenidx-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 84dc132528f8fd1c45fb2f7345111a05626ee686
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839630"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="8c332-102">Htermstogenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c332-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="8c332-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8c332-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="8c332-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8c332-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="8c332-105">Konvertiert einen Index in einen hamiltona-Begriff im `HTerm[]` Datenformat in einen generatorindex.</span><span class="sxs-lookup"><span data-stu-id="8c332-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="8c332-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8c332-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="8c332-107">Daten: [hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="8c332-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="8c332-108">Eingabedaten im- `HTerm[]` Format.</span><span class="sxs-lookup"><span data-stu-id="8c332-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="8c332-109">Termtype: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8c332-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8c332-110">Zusätzliche Informationen, die generatorindex hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8c332-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="8c332-111">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8c332-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8c332-112">Index für einen Begriff von hamiltonan</span><span class="sxs-lookup"><span data-stu-id="8c332-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="8c332-113">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8c332-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8c332-114">Ein generatorindex, der einen von dargestellten hamiltona-Begriff darstellt `data[idx]` , sowie zusätzliche Informationen, die von hinzugefügt werden `termType` .</span><span class="sxs-lookup"><span data-stu-id="8c332-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>