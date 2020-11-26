---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Ccnot-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: 715796ddd915d80036933e3f1ceefa97aa62cecf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212476"
---
# <a name="ccnot-operation"></a><span data-ttu-id="52dcf-102">Ccnot-Vorgang</span><span class="sxs-lookup"><span data-stu-id="52dcf-102">CCNOT operation</span></span>

<span data-ttu-id="52dcf-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="52dcf-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="52dcf-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="52dcf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="52dcf-105">Wendet das (doppelt kontrollierte – not)-Gate auf drei Qubits an.</span><span class="sxs-lookup"><span data-stu-id="52dcf-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="52dcf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="52dcf-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="52dcf-107">Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="52dcf-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="52dcf-108">Das erste Steuerelement-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="52dcf-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="52dcf-109">Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="52dcf-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="52dcf-110">Das zweite Steuerelement-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="52dcf-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="52dcf-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="52dcf-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="52dcf-112">Ziel-Qubit für das ccnot-Gate.</span><span class="sxs-lookup"><span data-stu-id="52dcf-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="52dcf-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52dcf-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="52dcf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52dcf-114">Remarks</span></span>

<span data-ttu-id="52dcf-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="52dcf-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```