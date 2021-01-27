---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubit
title: Applydefirstqubit-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubit
qsharp.summary: Applies an operation to the first qubit in the register.
ms.openlocfilehash: 381f8d689fba1984ba7fa287d658578bd5b6c48c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850730"
---
# <a name="applytofirstqubit-operation"></a><span data-ttu-id="709ff-102">Applydefirstqubit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="709ff-102">ApplyToFirstQubit operation</span></span>

<span data-ttu-id="709ff-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="709ff-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="709ff-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="709ff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="709ff-105">Wendet einen Vorgang auf das erste Qubit im Register an.</span><span class="sxs-lookup"><span data-stu-id="709ff-105">Applies an operation to the first qubit in the register.</span></span>

```qsharp
operation ApplyToFirstQubit (op : (Qubit => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="709ff-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="709ff-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="709ff-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="709ff-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="709ff-108">Ein Vorgang, der auf das erste Qubit angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="709ff-108">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="709ff-109">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="709ff-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="709ff-110">Qubit-Array bis zum ersten Qubit, auf das der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="709ff-110">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="709ff-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="709ff-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="709ff-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="709ff-112">See Also</span></span>

- [<span data-ttu-id="709ff-113">Microsoft. Quantum. Canon. applyjefirstqubita</span><span class="sxs-lookup"><span data-stu-id="709ff-113">Microsoft.Quantum.Canon.ApplyToFirstQubitA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitA)
- [<span data-ttu-id="709ff-114">Microsoft. Quantum. Canon. applyjefirstqubitc</span><span class="sxs-lookup"><span data-stu-id="709ff-114">Microsoft.Quantum.Canon.ApplyToFirstQubitC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitC)
- [<span data-ttu-id="709ff-115">Microsoft. Quantum. Canon. applyjefirstqubitca</span><span class="sxs-lookup"><span data-stu-id="709ff-115">Microsoft.Quantum.Canon.ApplyToFirstQubitCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitCA)