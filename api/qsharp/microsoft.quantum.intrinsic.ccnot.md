---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Ccnot-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702138"
---
# <a name="ccnot-operation"></a><span data-ttu-id="008a1-102">Ccnot-Vorgang</span><span class="sxs-lookup"><span data-stu-id="008a1-102">CCNOT operation</span></span>

<span data-ttu-id="008a1-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="008a1-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="008a1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="008a1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="008a1-105">Wendet das (doppelt kontrollierte – not)-Gate auf drei Qubits an.</span><span class="sxs-lookup"><span data-stu-id="008a1-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="008a1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="008a1-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="008a1-107">Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="008a1-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="008a1-108">Das erste Steuerelement-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="008a1-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="008a1-109">Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="008a1-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="008a1-110">Das zweite Steuerelement-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="008a1-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="008a1-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="008a1-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="008a1-112">Ziel-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="008a1-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="008a1-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="008a1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="008a1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="008a1-114">Remarks</span></span>

<span data-ttu-id="008a1-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="008a1-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```