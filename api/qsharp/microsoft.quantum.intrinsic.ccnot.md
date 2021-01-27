---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Ccnot-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: a9186269a868c2ac9d2f15727a3b0ed1bfec3fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819031"
---
# <a name="ccnot-operation"></a><span data-ttu-id="d18f2-102">Ccnot-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d18f2-102">CCNOT operation</span></span>

<span data-ttu-id="d18f2-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d18f2-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d18f2-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d18f2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d18f2-105">Wendet das (doppelt kontrollierte – not)-Gate auf drei Qubits an.</span><span class="sxs-lookup"><span data-stu-id="d18f2-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d18f2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d18f2-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="d18f2-107">Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d18f2-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d18f2-108">Das erste Steuerelement-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="d18f2-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="d18f2-109">Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d18f2-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d18f2-110">Das zweite Steuerelement-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="d18f2-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d18f2-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d18f2-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d18f2-112">Ziel-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="d18f2-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d18f2-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d18f2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d18f2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d18f2-114">Remarks</span></span>

<span data-ttu-id="d18f2-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="d18f2-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```