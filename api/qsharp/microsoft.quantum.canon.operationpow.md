---
uid: Microsoft.Quantum.Canon.OperationPow
title: Operationpow-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703955"
---
# <a name="operationpow-function"></a><span data-ttu-id="0c807-102">Operationpow-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c807-102">OperationPow function</span></span>

<span data-ttu-id="0c807-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0c807-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0c807-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0c807-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0c807-105">Löst einen Vorgang für eine Stromversorgung aus.</span><span class="sxs-lookup"><span data-stu-id="0c807-105">Raises an operation to a power.</span></span>

<span data-ttu-id="0c807-106">Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0c807-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="0c807-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c807-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="0c807-108">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0c807-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0c807-109">Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c807-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="0c807-110">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0c807-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0c807-111">Gibt an, wie oft $U $ wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c807-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="0c807-112">Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0c807-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="0c807-113">Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.</span><span class="sxs-lookup"><span data-stu-id="0c807-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0c807-114">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0c807-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0c807-115">GIF</span><span class="sxs-lookup"><span data-stu-id="0c807-115">'T</span></span>

<span data-ttu-id="0c807-116">Der Typ des Vorgangs, der eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c807-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c807-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c807-117">See Also</span></span>

- [<span data-ttu-id="0c807-118">Microsoft. Quantum. Canon. operationpowc</span><span class="sxs-lookup"><span data-stu-id="0c807-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="0c807-119">Microsoft. Quantum. Canon. operationpowa</span><span class="sxs-lookup"><span data-stu-id="0c807-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="0c807-120">Microsoft. Quantum. Canon. operationpowca</span><span class="sxs-lookup"><span data-stu-id="0c807-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)