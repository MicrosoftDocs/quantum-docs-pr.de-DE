---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Wiederherstellungsvorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: c192abbdfd02b26fbdba7b11f51ed08bb1a2030f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853038"
---
# <a name="recovercss-operation"></a><span data-ttu-id="1db75-102">Wiederherstellungsvorgang</span><span class="sxs-lookup"><span data-stu-id="1db75-102">RecoverCSS operation</span></span>

<span data-ttu-id="1db75-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="1db75-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="1db75-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1db75-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1db75-105">Führt eine einzelne Fehlerkorrektur durch einen von einem-Typ beschriebenen quantumcode aus `CSS` .</span><span class="sxs-lookup"><span data-stu-id="1db75-105">Performs a single round of error correction by a quantum code described by a `CSS` type.</span></span>

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a><span data-ttu-id="1db75-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1db75-106">Input</span></span>

### <a name="code--css"></a><span data-ttu-id="1db75-107">Code: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="1db75-107">code : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="1db75-108">Ein Quantum CSS-Fehler Behebungs Code `CSS` , der als Typ verpackt ist, beschreibt die Codierung und Decodierung von Quantum-Daten und die Art und Weise, wie Fehler-Syndrome gemessen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1db75-108">A quantum CSS error-correcting code packaged as a `CSS` type describes the encoding and decoding of quantum data, and how error syndromes are to be measured.</span></span>


### <a name="fnx--recoveryfn"></a><span data-ttu-id="1db75-109">fnx: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="1db75-109">fnX : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="1db75-110">Ein `RecoveryFn` , der die einzelnen $X $ Error-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler korrigieren.</span><span class="sxs-lookup"><span data-stu-id="1db75-110">A `RecoveryFn` that maps each $X$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="fnz--recoveryfn"></a><span data-ttu-id="1db75-111">fnz: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="1db75-111">fnZ : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="1db75-112">Ein `RecoveryFn` , der die einzelnen $Z $ Error-Syndrom den `Pauli[]` Vorgängen zuordnet, die den erkannten Fehler korrigieren.</span><span class="sxs-lookup"><span data-stu-id="1db75-112">A `RecoveryFn` that maps each $Z$ error syndrome to the `Pauli[]` operations that correct the detected error.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="1db75-113">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="1db75-113">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="1db75-114">Ein Array von Qubits, in denen der stabilikocodecode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1db75-114">An array of qubits where the stabilizer code is defined.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1db75-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1db75-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1db75-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1db75-116">See Also</span></span>

- [<span data-ttu-id="1db75-117">Microsoft. Quantum. errorcorrection. CSS</span><span class="sxs-lookup"><span data-stu-id="1db75-117">Microsoft.Quantum.ErrorCorrection.CSS</span></span>](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [<span data-ttu-id="1db75-118">Microsoft. Quantum. errorcorrection. wiederherstellungfn</span><span class="sxs-lookup"><span data-stu-id="1db75-118">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [<span data-ttu-id="1db75-119">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="1db75-119">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)