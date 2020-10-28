---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateCA
title: Preparechoistatueca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateCA
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.
ms.openlocfilehash: b9d2cdaea1ebc957719d92bf12901c54a55a56aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701243"
---
# <a name="preparechoistateca-operation"></a><span data-ttu-id="7a9aa-102">Preparechoistatueca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7a9aa-102">PrepareChoiStateCA operation</span></span>

<span data-ttu-id="7a9aa-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7a9aa-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7a9aa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7a9aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7a9aa-105">Bereitet den Status "Choi – jamiłkowski" für einen bestimmten Vorgang mit sowohl kontrollierten als auch Adjoint-Varianten auf angegebene Verweis-und Ziel Register vor.</span><span class="sxs-lookup"><span data-stu-id="7a9aa-105">Prepares the Choi–Jamiłkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiStateCA (op : (Qubit[] => Unit is Adj + Ctl), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="7a9aa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a9aa-106">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="7a9aa-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7a9aa-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="reference--qubit"></a><span data-ttu-id="7a9aa-108">Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7a9aa-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="7a9aa-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7a9aa-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="7a9aa-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7a9aa-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="7a9aa-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a9aa-111">See Also</span></span>

- [<span data-ttu-id="7a9aa-112">Microsoft. Quantum. Preparation. preparechoistate</span><span class="sxs-lookup"><span data-stu-id="7a9aa-112">Microsoft.Quantum.Preparation.PrepareChoiState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiState)