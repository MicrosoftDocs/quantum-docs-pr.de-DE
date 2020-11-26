---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Applydefirstqubitca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: bc2b1275b4258b9cc2db45c9e5cfe14f7eee0c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208804"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="7f372-102">Applydefirstqubitca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7f372-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="7f372-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7f372-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7f372-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7f372-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7f372-105">Wendet Operation op auf das erste Qubit im Register an.</span><span class="sxs-lookup"><span data-stu-id="7f372-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="7f372-106">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="7f372-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7f372-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7f372-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="7f372-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7f372-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="7f372-109">Ein Vorgang, der auf das erste Qubit angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f372-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="7f372-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7f372-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7f372-111">Qubit-Array bis zum ersten Qubit, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f372-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="7f372-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7f372-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="7f372-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f372-113">See Also</span></span>

- [<span data-ttu-id="7f372-114">Microsoft. Quantum. Canon. applyjefirstqubit</span><span class="sxs-lookup"><span data-stu-id="7f372-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)