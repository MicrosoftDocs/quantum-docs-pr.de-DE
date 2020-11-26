---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: Sizeadjustedtruthtable-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202922"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="d43f3-102">Sizeadjustedtruthtable-Funktion</span><span class="sxs-lookup"><span data-stu-id="d43f3-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="d43f3-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="d43f3-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="d43f3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d43f3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d43f3-105">Passt die Wahrheitstabelle anhand der Anzahl von Variablen aus einem Array von booleschen Werten an.</span><span class="sxs-lookup"><span data-stu-id="d43f3-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="d43f3-106">Ein neues Array wird von der Länge zurückgegeben. es ist `2^numVars` möglicherweise erforderlich, `table` die Größe durch Einträge zu erweitern `false` oder Sie auf Elemente zu kürzen `2^numVars` .</span><span class="sxs-lookup"><span data-stu-id="d43f3-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="d43f3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d43f3-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="d43f3-108">Tabelle: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d43f3-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="d43f3-109">Wahrheitstabelle als Array von Wahrheits Werten</span><span class="sxs-lookup"><span data-stu-id="d43f3-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="d43f3-110">numvars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d43f3-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d43f3-111">Anzahl von Variablen</span><span class="sxs-lookup"><span data-stu-id="d43f3-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="d43f3-112">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d43f3-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="d43f3-113">Größe der angepassten Wahrheitstabelle</span><span class="sxs-lookup"><span data-stu-id="d43f3-113">Size adjusted truth table</span></span>