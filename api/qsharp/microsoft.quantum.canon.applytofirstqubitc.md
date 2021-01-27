---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Applydefirstqubitc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: a36d20e03ebed82435d1d4136f4ce777eb468926
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850714"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="719c4-102">Applydefirstqubitc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="719c4-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="719c4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="719c4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="719c4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="719c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="719c4-105">Wendet Operation op auf das erste Qubit im Register an.</span><span class="sxs-lookup"><span data-stu-id="719c4-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="719c4-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="719c4-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="719c4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="719c4-107">Input</span></span>

### <a name="op--qubit--unit--is-ctl"></a><span data-ttu-id="719c4-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="719c4-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="719c4-109">Ein Vorgang, der auf das erste Qubit angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="719c4-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="719c4-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="719c4-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="719c4-111">Qubit-Array bis zum ersten Qubit, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="719c4-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="719c4-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="719c4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="719c4-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="719c4-113">See Also</span></span>

- [<span data-ttu-id="719c4-114">Microsoft. Quantum. Canon. applyjefirstqubit</span><span class="sxs-lookup"><span data-stu-id="719c4-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)