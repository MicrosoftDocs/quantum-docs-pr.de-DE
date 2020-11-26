---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Applydefirstqubita-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 4f0b209988c01076bdd0429d36d98c8060141618
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208838"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="d329e-102">Applydefirstqubita-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d329e-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="d329e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d329e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d329e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d329e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d329e-105">Wendet einen Vorgang auf das erste Qubit im Register an.</span><span class="sxs-lookup"><span data-stu-id="d329e-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="d329e-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="d329e-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="d329e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d329e-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="d329e-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="d329e-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d329e-109">Ein Vorgang, der auf das erste Qubit angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d329e-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="d329e-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d329e-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d329e-111">Qubit-Array bis zum ersten Qubit, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d329e-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="d329e-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d329e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d329e-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d329e-113">See Also</span></span>

- [<span data-ttu-id="d329e-114">Microsoft. Quantum. Canon. applyjefirstqubit</span><span class="sxs-lookup"><span data-stu-id="d329e-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)