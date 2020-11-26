---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Codierte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 803f35b9e7af547bc34f21de74684fba885bfda9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203177"
---
# <a name="encoded-function"></a><span data-ttu-id="148db-102">Codierte Funktion</span><span class="sxs-lookup"><span data-stu-id="148db-102">Encoded function</span></span>

<span data-ttu-id="148db-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="148db-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="148db-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="148db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="148db-105">Wahrheitstabelle beim {1,-1} Codieren codieren</span><span class="sxs-lookup"><span data-stu-id="148db-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="148db-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="148db-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="148db-107">Tabelle: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="148db-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="148db-108">Wahrheitstabelle als Array von Wahrheits Werten</span><span class="sxs-lookup"><span data-stu-id="148db-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="148db-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="148db-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="148db-110">Wahrheitstabelle als {1,-1} Array von ganzen Zahlen</span><span class="sxs-lookup"><span data-stu-id="148db-110">Truth table as array of {1,-1} integers</span></span>