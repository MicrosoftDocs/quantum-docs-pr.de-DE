---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Dumpoperation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: cde188806506c586c4c77a7f9b2b43ad0e10ef1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829274"
---
# <a name="dumpoperation-operation"></a><span data-ttu-id="486ff-102">Dumpoperation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="486ff-102">DumpOperation operation</span></span>

<span data-ttu-id="486ff-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="486ff-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="486ff-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="486ff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="486ff-105">Zeigt bei einem Vorgang Diagnoseinformationen zu dem Vorgang an, der vom aktuellen Ausführungs Ziel verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="486ff-105">Given an operation, displays diagnostics about the operation that are made available by the current execution target.</span></span>

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="486ff-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="486ff-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="486ff-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="486ff-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="486ff-108">Die Anzahl der Qubits, auf die der angegebene Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="486ff-108">The number of qubits on which the given operation acts.</span></span>


### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="486ff-109">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="486ff-109">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="486ff-110">Der Vorgang, der diagnostiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="486ff-110">The operation that is to be diagnosed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="486ff-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="486ff-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="486ff-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="486ff-112">Example</span></span>

<span data-ttu-id="486ff-113">Wenn der folgende Code Ausschnitt auf dem Quantum-simulatorziel ausgeführt wird, wird die Matrix $ $ \begin{aligned} \left ausgegeben (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \end{Matrix}\right) \end{aligned}.</span><span class="sxs-lookup"><span data-stu-id="486ff-113">When run on the quantum simulator target, the following snippet will output the matrix $$ \begin{aligned} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \end{matrix}\right) \end{aligned}.</span></span>
$$

```qsharp
operation DumpCnot() : Unit {
    DumpOperation(2, ApplyToFirstTwoQubitsCA(CNOT, _));
}
```

## <a name="remarks"></a><span data-ttu-id="486ff-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="486ff-114">Remarks</span></span>

<span data-ttu-id="486ff-115">Das Aufrufen dieses Vorgangs hat keine Observable-Auswirkung in Q #.</span><span class="sxs-lookup"><span data-stu-id="486ff-115">Calling this operation has no observable effect from within Q#.</span></span> <span data-ttu-id="486ff-116">Die genaue Diagnose, die ggf. angezeigt wird, hängt vom aktuellen Ausführungs Ziel und der Editor Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="486ff-116">The exact diagnostics that are displayed, if any, are dependent on the current execution target and editor environment.</span></span>
<span data-ttu-id="486ff-117">Wenn z. b. für den vollständigen Quantum-Simulator verwendet wird, wird eine einheitliche Matrix, die zur Darstellung von verwendet wird, `op` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="486ff-117">For example, when used on the full-state quantum simulator, a unitary matrix used to represent `op` is displayed.</span></span>

<span data-ttu-id="486ff-118">Beachten Sie, dass bei der Durchführung von Simulatoren, die eine globale Phasen Mehrdeutigkeit zulassen (z. b. der voll Zustands Simulator), die zurückgegebenen Darstellungen bis zu einer globalen Phase variieren können.</span><span class="sxs-lookup"><span data-stu-id="486ff-118">Note that, when run on simulators that admit a global phase ambiguity (e.g.: the full-state simulator), returned representations may vary up to a global phase.</span></span>

<span data-ttu-id="486ff-119">Ebenso kann die Reihenfolge der Zeilen-und Spalten Matrizen von den Konventionen abweichen, die von den einzelnen Simulatoren verwendet werden, die diesen Vorgang unterstützen.</span><span class="sxs-lookup"><span data-stu-id="486ff-119">Similarly, the ordering of rows and columns matrix representations may vary with the conventions used by each simulator supporting this operation.</span></span>