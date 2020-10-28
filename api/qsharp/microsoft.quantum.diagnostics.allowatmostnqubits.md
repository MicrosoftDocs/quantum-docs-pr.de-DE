---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Vorgang "Zuordnung"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: ddbed96df0d95cfd78730c091a6a81ee6e49c349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702791"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="584a3-102">Vorgang "Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="584a3-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="584a3-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="584a3-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="584a3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="584a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="584a3-105">Bei einem Aufrufe dieses Vorgangs und seines Adjoint-Vorgangs wird von bestätigt, dass höchstens eine angegebene Anzahl zusätzlicher Qubits mit using-Anweisungen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="584a3-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="584a3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="584a3-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="584a3-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="584a3-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="584a3-108">Die maximale Anzahl von Qubits, die zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="584a3-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="584a3-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="584a3-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="584a3-110">Eine Meldung, die bei einem Fehler angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="584a3-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="584a3-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="584a3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="584a3-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="584a3-112">Remarks</span></span>

<span data-ttu-id="584a3-113">Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="584a3-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>