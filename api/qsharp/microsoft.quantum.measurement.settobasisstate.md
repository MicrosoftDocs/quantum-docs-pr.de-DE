---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Setdebasisstate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: dfa054360a5e82b7ae6ec5a6d52e7d5fe566f42e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854622"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="cf8c9-102">Setdebasisstate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf8c9-102">SetToBasisState operation</span></span>

<span data-ttu-id="cf8c9-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="cf8c9-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="cf8c9-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cf8c9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="cf8c9-105">Legt ein Qubit auf einen angegebenen Berechnungsbasis Zustand fest, indem das Qubit gemessen und bei Bedarf ein bitflip angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="cf8c9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf8c9-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="cf8c9-107">gewünscht: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="cf8c9-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="cf8c9-108">Der Basiszustand, auf den das Qubit festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="cf8c9-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cf8c9-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cf8c9-110">Das Qubit, dessen Zustand festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf8c9-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cf8c9-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cf8c9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cf8c9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf8c9-112">Remarks</span></span>

<span data-ttu-id="cf8c9-113">Als invariante dieses Vorgangs wird beim Aufrufen von `M(q)` sofort nach der Wert `SetToBasisState(result, q)` zurückgegeben `result` .</span><span class="sxs-lookup"><span data-stu-id="cf8c9-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>