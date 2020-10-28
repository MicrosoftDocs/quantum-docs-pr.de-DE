---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Setdebasisstate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: bb40ddcf6518a30f5d88eec21cf8e2c2d6e0bbaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724670"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="fa8f4-102">Setdebasisstate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fa8f4-102">SetToBasisState operation</span></span>

<span data-ttu-id="fa8f4-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="fa8f4-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="fa8f4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fa8f4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fa8f4-105">Legt ein Qubit auf einen angegebenen Berechnungsbasis Zustand fest, indem das Qubit gemessen und bei Bedarf ein bitflip angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa8f4-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="fa8f4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fa8f4-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="fa8f4-107">gewünscht: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="fa8f4-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="fa8f4-108">Der Basiszustand, auf den das Qubit festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa8f4-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="fa8f4-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fa8f4-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fa8f4-110">Das Qubit, dessen Zustand festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa8f4-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fa8f4-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa8f4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fa8f4-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa8f4-112">Remarks</span></span>

<span data-ttu-id="fa8f4-113">Als invariante dieses Vorgangs wird beim Aufrufen von `M(q)` sofort nach der Wert `SetToBasisState(result, q)` zurückgegeben `result` .</span><span class="sxs-lookup"><span data-stu-id="fa8f4-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>