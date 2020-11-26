---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Wiederherstellungs Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: bdf09decc3705d3285f4eb605c176d7764a994d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200576"
---
# <a name="recover-operation"></a><span data-ttu-id="f3999-102">Wiederherstellungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3999-102">Recover operation</span></span>

<span data-ttu-id="f3999-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f3999-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f3999-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f3999-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f3999-105">Führt eine einzelne Fehlerkorrektur durch einen von einem-Typ beschriebenen quantumcode aus `QECC` .</span><span class="sxs-lookup"><span data-stu-id="f3999-105">Performs a single round of error correction by a quantum code described by a `QECC` type.</span></span>

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="f3999-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3999-106">Input</span></span>

### <a name="code--qecc"></a><span data-ttu-id="f3999-107">Code: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="f3999-107">code : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="f3999-108">Bei einem Fehler in der Quantum-Korrektur `QECC` , der als Typ verpackt wird, werden das Codieren und Decodieren von Quantum-Daten beschrieben, und es wird beschrieben, wie Fehler Syndrome gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="f3999-108">A quantum error-correcting code packaged as a `QECC` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fn--recoveryfn"></a><span data-ttu-id="f3999-109">FN: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="f3999-109">fn : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="f3999-110">Eine `RecoveryFn` , die jedes Fehler-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler beheben.</span><span class="sxs-lookup"><span data-stu-id="f3999-110">A `RecoveryFn` that maps each error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="f3999-111">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="f3999-111">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="f3999-112">Ein Array von Qubits, in denen der stabilikocodecode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3999-112">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f3999-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f3999-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f3999-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3999-114">See Also</span></span>

- [<span data-ttu-id="f3999-115">Microsoft. Quantum. errorcorrection. qecc</span><span class="sxs-lookup"><span data-stu-id="f3999-115">Microsoft.Quantum.ErrorCorrection.QECC</span></span>](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [<span data-ttu-id="f3999-116">Microsoft. Quantum. errorcorrection. wiederherstellungfn</span><span class="sxs-lookup"><span data-stu-id="f3999-116">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="f3999-117">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="f3999-117">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)