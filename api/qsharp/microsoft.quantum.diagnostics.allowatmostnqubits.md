---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Vorgang "Zuordnung"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 5376b6f39d12d664342fbf71e67442c6ef8a0827
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202548"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="286d4-102">Vorgang "Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="286d4-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="286d4-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="286d4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="286d4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="286d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="286d4-105">Bei einem Aufrufe dieses Vorgangs und seines Adjoint-Vorgangs wird von bestätigt, dass höchstens eine angegebene Anzahl zusätzlicher Qubits mit using-Anweisungen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="286d4-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="286d4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="286d4-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="286d4-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="286d4-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="286d4-108">Die maximale Anzahl von Qubits, die zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="286d4-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="286d4-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="286d4-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="286d4-110">Eine Meldung, die bei einem Fehler angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="286d4-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="286d4-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="286d4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="286d4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="286d4-112">Remarks</span></span>

<span data-ttu-id="286d4-113">Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="286d4-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>