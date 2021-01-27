---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Applyifc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: ef16b23349b604d174e72d9ae06d2052e2ab60f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841856"
---
# <a name="applyifc-operation"></a><span data-ttu-id="9e146-102">Applyifc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9e146-102">ApplyIfC operation</span></span>

<span data-ttu-id="9e146-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e146-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e146-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e146-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e146-105">Wendet eine steuerbare Operation an, die auf einem klassischen Bit bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="9e146-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="9e146-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e146-106">Description</span></span>

<span data-ttu-id="9e146-107">Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="9e146-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="9e146-108">Gibt `false` an, dass nichts passiert `target` .</span><span class="sxs-lookup"><span data-stu-id="9e146-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="9e146-109">Das-Suffix `C` gibt an, dass der anzuwendende Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="9e146-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="9e146-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e146-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="9e146-111">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="9e146-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9e146-112">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e146-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="9e146-113">Bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9e146-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9e146-114">ein boolescher Wert, der steuert, ob op angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e146-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="9e146-115">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="9e146-115">target : 'T</span></span>

<span data-ttu-id="9e146-116">Die Eingabe, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e146-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9e146-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9e146-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9e146-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9e146-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e146-119">GIF</span><span class="sxs-lookup"><span data-stu-id="9e146-119">'T</span></span>

<span data-ttu-id="9e146-120">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e146-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="9e146-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e146-121">Example</span></span>

<span data-ttu-id="9e146-122">Im folgenden wird ein Register von Qubits auf einen Berechnungs Status vorbereitet, der durch eine klassische Bitzeichenfolge dargestellt wird, die als Array von Werten angegeben ist `Bool` :</span><span class="sxs-lookup"><span data-stu-id="9e146-122">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="9e146-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e146-123">See Also</span></span>

- [<span data-ttu-id="9e146-124">Microsoft. Quantum. Canon. applyifc</span><span class="sxs-lookup"><span data-stu-id="9e146-124">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="9e146-125">Microsoft. Quantum. Canon. applyifa</span><span class="sxs-lookup"><span data-stu-id="9e146-125">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="9e146-126">Microsoft. Quantum. Canon. applyifca</span><span class="sxs-lookup"><span data-stu-id="9e146-126">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)