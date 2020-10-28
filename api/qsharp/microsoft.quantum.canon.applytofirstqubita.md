---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Applydefirstqubita-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 00dbff0b562f90653c8569589e838f11e6c938e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704874"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="5e7be-102">Applydefirstqubita-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5e7be-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="5e7be-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5e7be-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5e7be-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5e7be-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5e7be-105">Wendet einen Vorgang auf das erste Qubit im Register an.</span><span class="sxs-lookup"><span data-stu-id="5e7be-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="5e7be-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="5e7be-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5e7be-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e7be-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="5e7be-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="5e7be-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5e7be-109">Ein Vorgang, der auf das erste Qubit angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e7be-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="5e7be-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5e7be-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5e7be-111">Qubit-Array bis zum ersten Qubit, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e7be-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="5e7be-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5e7be-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5e7be-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e7be-113">See Also</span></span>

- [<span data-ttu-id="5e7be-114">Microsoft. Quantum. Canon. applyjefirstqubit</span><span class="sxs-lookup"><span data-stu-id="5e7be-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)