---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Codierte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 6b9d21969ee90f3928b65a1c97a5b0f15157e381
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725202"
---
# <a name="encoded-function"></a><span data-ttu-id="4c91e-102">Codierte Funktion</span><span class="sxs-lookup"><span data-stu-id="4c91e-102">Encoded function</span></span>

<span data-ttu-id="4c91e-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="4c91e-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="4c91e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4c91e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4c91e-105">Wahrheitstabelle beim {1,-1} Codieren codieren</span><span class="sxs-lookup"><span data-stu-id="4c91e-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="4c91e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4c91e-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="4c91e-107">Tabelle: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="4c91e-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="4c91e-108">Wahrheitstabelle als Array von Wahrheits Werten</span><span class="sxs-lookup"><span data-stu-id="4c91e-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="4c91e-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4c91e-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4c91e-110">Wahrheitstabelle als {1,-1} Array von ganzen Zahlen</span><span class="sxs-lookup"><span data-stu-id="4c91e-110">Truth table as array of {1,-1} integers</span></span>