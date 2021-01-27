---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Applydefirstqubita-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 2f96c2a8ed31d295bc127c568e0ca24c267638b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841445"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="909ea-102">Applydefirstqubita-Vorgang</span><span class="sxs-lookup"><span data-stu-id="909ea-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="909ea-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="909ea-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="909ea-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="909ea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="909ea-105">Wendet einen Vorgang auf das erste Qubit im Register an.</span><span class="sxs-lookup"><span data-stu-id="909ea-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="909ea-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="909ea-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="909ea-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="909ea-107">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="909ea-108">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="909ea-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="909ea-109">Ein Vorgang, der auf das erste Qubit angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="909ea-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="909ea-110">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="909ea-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="909ea-111">Qubit-Array bis zum ersten Qubit, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="909ea-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="909ea-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="909ea-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="909ea-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="909ea-113">See Also</span></span>

- [<span data-ttu-id="909ea-114">Microsoft. Quantum. Canon. applyjefirstqubit</span><span class="sxs-lookup"><span data-stu-id="909ea-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)