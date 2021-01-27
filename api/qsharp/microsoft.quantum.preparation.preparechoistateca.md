---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateCA
title: Preparechoistatueca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateCA
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.
ms.openlocfilehash: 6398a875923e03adcb31533dadd881d3c0744840
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856885"
---
# <a name="preparechoistateca-operation"></a><span data-ttu-id="4581c-102">Preparechoistatueca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4581c-102">PrepareChoiStateCA operation</span></span>

<span data-ttu-id="4581c-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="4581c-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="4581c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4581c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4581c-105">Bereitet den Status "Choi – jamiołkowski" für einen bestimmten Vorgang mit sowohl kontrollierten als auch Adjoint-Varianten auf angegebene Verweis-und Ziel Register vor.</span><span class="sxs-lookup"><span data-stu-id="4581c-105">Prepares the Choi–Jamiołkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiStateCA (op : (Qubit[] => Unit is Adj + Ctl), reference : Qubit[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4581c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4581c-106">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="4581c-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4581c-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="reference--qubit"></a><span data-ttu-id="4581c-108">Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4581c-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="4581c-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4581c-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="4581c-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4581c-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="4581c-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4581c-111">See Also</span></span>

- [<span data-ttu-id="4581c-112">Microsoft. Quantum. Preparation. preparechoistate</span><span class="sxs-lookup"><span data-stu-id="4581c-112">Microsoft.Quantum.Preparation.PrepareChoiState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiState)