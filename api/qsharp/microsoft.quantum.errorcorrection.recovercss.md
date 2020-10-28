---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Wiederherstellungsvorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: 48d3cd3d5f6aea265fac2f50b913ab855a31accf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702425"
---
# <a name="recovercss-operation"></a><span data-ttu-id="64bd9-102">Wiederherstellungsvorgang</span><span class="sxs-lookup"><span data-stu-id="64bd9-102">RecoverCSS operation</span></span>

<span data-ttu-id="64bd9-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="64bd9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="64bd9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="64bd9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="64bd9-105">Führt eine einzelne Fehlerkorrektur durch einen von einem-Typ beschriebenen quantumcode aus `CSS` .</span><span class="sxs-lookup"><span data-stu-id="64bd9-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="64bd9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bd9-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="64bd9-107">Code: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="64bd9-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="64bd9-108">Ein Quantum CSS-Fehler Behebungs Code `CSS` , der als Typ verpackt ist, beschreibt die Codierung und Decodierung von Quantum-Daten und die Art und Weise, wie Fehler-Syndrome gemessen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64bd9-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="64bd9-109">fnx: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="64bd9-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="64bd9-110">Ein `RecoveryFn` , der die einzelnen $X $ Error-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler korrigieren.</span><span class="sxs-lookup"><span data-stu-id="64bd9-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="64bd9-111">fnz: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="64bd9-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="64bd9-112">Ein `RecoveryFn` , der die einzelnen $Z $ Error-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler korrigieren.</span><span class="sxs-lookup"><span data-stu-id="64bd9-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="64bd9-113">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="64bd9-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="64bd9-114">Ein Array von Qubits, in denen der stabilikocodecode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="64bd9-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="64bd9-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64bd9-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="64bd9-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64bd9-116">See Also</span></span>

- [<span data-ttu-id="64bd9-117">Microsoft. Quantum. errorcorrection. CSS</span><span class="sxs-lookup"><span data-stu-id="64bd9-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="64bd9-118">Microsoft. Quantum. errorcorrection. wiederherstellungfn</span><span class="sxs-lookup"><span data-stu-id="64bd9-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="64bd9-119">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="64bd9-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)