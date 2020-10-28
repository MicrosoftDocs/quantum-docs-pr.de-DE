---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Operationpowc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: f3c51410fb7c091385b64a1c4c99b3972d5055b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703919"
---
# <a name="operationpowc-function"></a><span data-ttu-id="9e2bb-102">Operationpowc-Funktion</span><span class="sxs-lookup"><span data-stu-id="9e2bb-102">OperationPowC function</span></span>

<span data-ttu-id="9e2bb-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e2bb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e2bb-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9e2bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9e2bb-105">Löst einen Vorgang für eine Stromversorgung aus.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-105">Raises an operation to a power.</span></span>
<span data-ttu-id="9e2bb-106">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="9e2bb-107">Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="9e2bb-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9e2bb-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="9e2bb-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="9e2bb-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9e2bb-110">Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="9e2bb-111">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9e2bb-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9e2bb-112">Gibt an, wie oft $U $ wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="9e2bb-113">Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="9e2bb-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9e2bb-114">Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9e2bb-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9e2bb-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e2bb-116">GIF</span><span class="sxs-lookup"><span data-stu-id="9e2bb-116">'T</span></span>

<span data-ttu-id="9e2bb-117">Der Typ des Vorgangs, der eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e2bb-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e2bb-118">See Also</span></span>

- [<span data-ttu-id="9e2bb-119">Microsoft. Quantum. Canon. operationpow</span><span class="sxs-lookup"><span data-stu-id="9e2bb-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)