---
uid: Microsoft.Quantum.Diagnostics.DumpReferenceAndTarget
title: Dumpreferendceandtarget-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpReferenceAndTarget
qsharp.summary: Uses DumpRegister to provide diagnostics on the state of a reference and target register. Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.
ms.openlocfilehash: ef7e59b1561be04cba5839ebc397702b6c1df5bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202038"
---
# <a name="dumpreferenceandtarget-operation"></a><span data-ttu-id="340f8-102">Dumpreferendceandtarget-Vorgang</span><span class="sxs-lookup"><span data-stu-id="340f8-102">DumpReferenceAndTarget operation</span></span>

<span data-ttu-id="340f8-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="340f8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="340f8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="340f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="340f8-105">Verwendet dumpregister, um die Diagnose für den Status eines Verweis-und Ziel Registers bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="340f8-105">Uses DumpRegister to provide diagnostics on the state of a reference and target register.</span></span> <span data-ttu-id="340f8-106">Wird als separater Vorgang geschrieben, um das Überschreiben und interpretieren als getrennte Register zuzulassen, anstatt als einzelnes kombiniertes Register.</span><span class="sxs-lookup"><span data-stu-id="340f8-106">Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.</span></span>

```qsharp
operation DumpReferenceAndTarget (reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="340f8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="340f8-107">Input</span></span>

### <a name="reference--qubit"></a><span data-ttu-id="340f8-108">Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="340f8-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="340f8-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="340f8-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="340f8-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="340f8-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

