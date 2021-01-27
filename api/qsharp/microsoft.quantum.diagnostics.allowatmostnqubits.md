---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Vorgang "Zuordnung"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 3aa80767ac0f752e7be0efa2966c580ca3cb8f19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830916"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="09258-102">Vorgang "Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="09258-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="09258-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="09258-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="09258-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09258-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09258-105">Bei einem Aufrufe dieses Vorgangs und seines Adjoint-Vorgangs wird von bestätigt, dass höchstens eine angegebene Anzahl zusätzlicher Qubits mit using-Anweisungen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="09258-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="09258-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="09258-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="09258-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="09258-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="09258-108">Die maximale Anzahl von Qubits, die zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="09258-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="09258-109">Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="09258-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="09258-110">Eine Meldung, die bei einem Fehler angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="09258-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="09258-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09258-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="09258-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="09258-112">Example</span></span>

<span data-ttu-id="09258-113">Der folgende Code Ausschnitt schlägt fehl, wenn er auf Computern ausgeführt wird, die diese Diagnose unterstützen:</span><span class="sxs-lookup"><span data-stu-id="09258-113">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
within {
    AllowAtMostNQubits(3, "Too many qubits allocated.");
} apply {
    // Fails since this allocates four qubits.
    using (register = Qubit[4]) {
    }
}
```

## <a name="remarks"></a><span data-ttu-id="09258-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09258-114">Remarks</span></span>

<span data-ttu-id="09258-115">Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="09258-115">This operation may be replaced by a no-op on targets which do not support it.</span></span>