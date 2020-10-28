---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Operationpowa-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 66df354c6de7e48624712276882759043b78466c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703931"
---
# <a name="operationpowa-function"></a><span data-ttu-id="3dbc8-102">Operationpowa-Funktion</span><span class="sxs-lookup"><span data-stu-id="3dbc8-102">OperationPowA function</span></span>

<span data-ttu-id="3dbc8-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3dbc8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3dbc8-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3dbc8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3dbc8-105">Löst einen Vorgang für eine Stromversorgung aus.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-105">Raises an operation to a power.</span></span>
<span data-ttu-id="3dbc8-106">Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="3dbc8-107">Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="3dbc8-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3dbc8-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="3dbc8-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="3dbc8-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="3dbc8-110">Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="3dbc8-111">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3dbc8-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3dbc8-112">Gibt an, wie oft $U $ wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-adj"></a><span data-ttu-id="3dbc8-113">Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="3dbc8-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="3dbc8-114">Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3dbc8-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3dbc8-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3dbc8-116">GIF</span><span class="sxs-lookup"><span data-stu-id="3dbc8-116">'T</span></span>

<span data-ttu-id="3dbc8-117">Der Typ des Vorgangs, der eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="3dbc8-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3dbc8-118">See Also</span></span>

- [<span data-ttu-id="3dbc8-119">Microsoft. Quantum. Canon. operationpow</span><span class="sxs-lookup"><span data-stu-id="3dbc8-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)