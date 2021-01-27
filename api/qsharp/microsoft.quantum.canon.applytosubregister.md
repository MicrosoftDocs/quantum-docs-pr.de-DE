---
uid: Microsoft.Quantum.Canon.ApplyToSubregister
title: Applydesubregister-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToSubregister
qsharp.summary: Applies an operation to a subregister of a register, with qubits specified by an array of their indices.
ms.openlocfilehash: be820c87ee19230713d6c3e5681bbe3678040e95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850468"
---
# <a name="applytosubregister-operation"></a><span data-ttu-id="4fa82-102">Applydesubregister-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4fa82-102">ApplyToSubregister operation</span></span>

<span data-ttu-id="4fa82-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4fa82-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4fa82-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4fa82-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4fa82-105">Wendet einen Vorgang auf ein unter Register eines Register mit Qubits an, die durch ein Array ihrer Indizes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fa82-105">Applies an operation to a subregister of a register, with qubits specified by an array of their indices.</span></span>

```qsharp
operation ApplyToSubregister (op : (Qubit[] => Unit), idxs : Int[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4fa82-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4fa82-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="4fa82-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4fa82-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4fa82-108">Der für die unter Registrierung anzuwendende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4fa82-108">Operation to apply to subregister.</span></span>


### <a name="idxs--int"></a><span data-ttu-id="4fa82-109">idxs: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4fa82-109">idxs : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4fa82-110">Ein Array von Indizes, das angibt, auf welche Qubits der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fa82-110">Array of indices, indicating to which qubits the operation will be applied.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="4fa82-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4fa82-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4fa82-112">Registrieren Sie sich für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4fa82-112">Register on which the operation acts.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4fa82-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4fa82-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="4fa82-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4fa82-114">Example</span></span>

<span data-ttu-id="4fa82-115">Erstellen Sie drei Qubit-Status $ \frac {1} {\sqrt {2} } \ket {0} \_ 2 (\ket {0} \_ 1 \ Ket {0} _3 + \ket {1} \_ 1 \ Ket {1} _3) $:</span><span class="sxs-lookup"><span data-stu-id="4fa82-115">Create three qubit state $\frac{1}{\sqrt{2}}\ket{0}\_2(\ket{0}\_1\ket{0}_3+\ket{1}\_1\ket{1}_3)$:</span></span>

```qsharp
    using (register = Qubit[3]) {
        ApplyToSubregister(Exp([PauliX,PauliY],PI() / 4.0,_), [1,3], register);
    }
```

## <a name="see-also"></a><span data-ttu-id="4fa82-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4fa82-116">See Also</span></span>

- [<span data-ttu-id="4fa82-117">Microsoft. Quantum. Canon. ApplyTo subregistera</span><span class="sxs-lookup"><span data-stu-id="4fa82-117">Microsoft.Quantum.Canon.ApplyToSubregisterA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterA)
- [<span data-ttu-id="4fa82-118">Microsoft. Quantum. Canon. ApplyTo subregisterc</span><span class="sxs-lookup"><span data-stu-id="4fa82-118">Microsoft.Quantum.Canon.ApplyToSubregisterC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterC)
- [<span data-ttu-id="4fa82-119">Microsoft. Quantum. Canon. ApplyTo subregisterca</span><span class="sxs-lookup"><span data-stu-id="4fa82-119">Microsoft.Quantum.Canon.ApplyToSubregisterCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToSubregisterCA)