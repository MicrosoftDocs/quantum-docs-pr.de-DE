---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Operationpowca-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 32de77cbd54cc8eeb8c4a967fd046dca709cd9ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205642"
---
# <a name="operationpowca-function"></a><span data-ttu-id="10303-102">Operationpowca-Funktion</span><span class="sxs-lookup"><span data-stu-id="10303-102">OperationPowCA function</span></span>

<span data-ttu-id="10303-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="10303-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="10303-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="10303-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="10303-105">Löst einen Vorgang für eine Stromversorgung aus.</span><span class="sxs-lookup"><span data-stu-id="10303-105">Raises an operation to a power.</span></span>
<span data-ttu-id="10303-106">Der-Modifizierer `A` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="10303-106">The modifier `A` indicates that the operation is controllable and adjointable.</span></span>

<span data-ttu-id="10303-107">Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="10303-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="10303-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10303-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="10303-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="10303-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="10303-110">Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10303-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="10303-111">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10303-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10303-112">Gibt an, wie oft $U $ wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10303-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="10303-113">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="10303-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="10303-114">Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.</span><span class="sxs-lookup"><span data-stu-id="10303-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="10303-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="10303-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="10303-116">GIF</span><span class="sxs-lookup"><span data-stu-id="10303-116">'T</span></span>

<span data-ttu-id="10303-117">Der Typ des Vorgangs, der eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10303-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="10303-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="10303-118">See Also</span></span>

- [<span data-ttu-id="10303-119">Microsoft. Quantum. Canon. operationpow</span><span class="sxs-lookup"><span data-stu-id="10303-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)