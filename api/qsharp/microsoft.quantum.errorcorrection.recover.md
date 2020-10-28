---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Wiederherstellungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: a659399f51794a4edc1d2ff43da84e46797103fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702426"
---
# <a name="recover-operation"></a><span data-ttu-id="244e6-102">Wiederherstellungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="244e6-102">Recover operation</span></span>

<span data-ttu-id="244e6-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="244e6-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="244e6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="244e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="244e6-105">Führt eine einzelne Fehlerkorrektur durch einen von einem-Typ beschriebenen quantumcode aus `QECC` .</span><span class="sxs-lookup"><span data-stu-id="244e6-105">Performs a single round of error correction by a quantum code described by a `QECC` type.</span></span>

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="244e6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="244e6-106">Input</span></span>

### <a name="code--qecc"></a><span data-ttu-id="244e6-107">Code: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="244e6-107">code : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="244e6-108">Bei einem Fehler in der Quantum-Korrektur `QECC` , der als Typ verpackt wird, werden das Codieren und Decodieren von Quantum-Daten beschrieben, und es wird beschrieben, wie Fehler Syndrome gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="244e6-108">A quantum error-correcting code packaged as a `QECC` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fn--recoveryfn"></a><span data-ttu-id="244e6-109">FN: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="244e6-109">fn : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="244e6-110">Eine `RecoveryFn` , die jedes Fehler-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler beheben.</span><span class="sxs-lookup"><span data-stu-id="244e6-110">A `RecoveryFn` that maps each error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="244e6-111">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="244e6-111">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="244e6-112">Ein Array von Qubits, in denen der stabilikocodecode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="244e6-112">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="244e6-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="244e6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="244e6-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="244e6-114">See Also</span></span>

- [<span data-ttu-id="244e6-115">Microsoft. Quantum. errorcorrection. qecc</span><span class="sxs-lookup"><span data-stu-id="244e6-115">Microsoft.Quantum.ErrorCorrection.QECC</span></span>](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [<span data-ttu-id="244e6-116">Microsoft. Quantum. errorcorrection. wiederherstellungfn</span><span class="sxs-lookup"><span data-stu-id="244e6-116">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="244e6-117">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="244e6-117">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)