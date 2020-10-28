---
uid: Microsoft.Quantum.Diagnostics.DumpReferenceAndTarget
title: Dumpreferendceandtarget-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpReferenceAndTarget
qsharp.summary: Uses DumpRegister to provide diagnostics on the state of a reference and target register. Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.
ms.openlocfilehash: f791f6f1e3c1b1da14ac3548a4bd78bb4f24ff83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702702"
---
# <a name="dumpreferenceandtarget-operation"></a><span data-ttu-id="b6a47-102">Dumpreferendceandtarget-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b6a47-102">DumpReferenceAndTarget operation</span></span>

<span data-ttu-id="b6a47-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b6a47-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b6a47-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6a47-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6a47-105">Verwendet dumpregister, um die Diagnose für den Status eines Verweis-und Ziel Registers bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b6a47-105">Uses DumpRegister to provide diagnostics on the state of a reference and target register.</span></span> <span data-ttu-id="b6a47-106">Wird als separater Vorgang geschrieben, um das Überschreiben und interpretieren als getrennte Register zuzulassen, anstatt als einzelnes kombiniertes Register.</span><span class="sxs-lookup"><span data-stu-id="b6a47-106">Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.</span></span>

```qsharp
operation DumpReferenceAndTarget (reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b6a47-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6a47-107">Input</span></span>

### <a name="reference--qubit"></a><span data-ttu-id="b6a47-108">Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b6a47-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="b6a47-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b6a47-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="b6a47-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b6a47-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

