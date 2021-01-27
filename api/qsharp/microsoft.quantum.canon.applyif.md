---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Applyif-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: 109a5c4748d183f199e420b4b1aef687613d220c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841870"
---
# <a name="applyif-operation"></a><span data-ttu-id="81208-102">Applyif-Vorgang</span><span class="sxs-lookup"><span data-stu-id="81208-102">ApplyIf operation</span></span>

<span data-ttu-id="81208-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="81208-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="81208-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81208-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81208-105">Wendet einen Vorgang an, der von einem klassischen Bit abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="81208-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="81208-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81208-106">Description</span></span>

<span data-ttu-id="81208-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="81208-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="81208-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="81208-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="81208-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81208-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="81208-110">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81208-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="81208-111">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="81208-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="81208-112">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="81208-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="81208-113">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="81208-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="81208-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="81208-114">target : 'T</span></span>

<span data-ttu-id="81208-115">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="81208-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="81208-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81208-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="81208-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="81208-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="81208-118">GIF</span><span class="sxs-lookup"><span data-stu-id="81208-118">'T</span></span>

<span data-ttu-id="81208-119">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="81208-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="81208-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="81208-120">Example</span></span>

<span data-ttu-id="81208-121">Im folgenden wird ein Register von Qubits auf einen Berechnungs Status vorbereitet, der durch eine klassische Bitzeichenfolge dargestellt wird, die als Array von Werten angegeben ist `Bool` :</span><span class="sxs-lookup"><span data-stu-id="81208-121">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="81208-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81208-122">See Also</span></span>

- [<span data-ttu-id="81208-123">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="81208-123">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="81208-124">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="81208-124">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="81208-125">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="81208-125">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)