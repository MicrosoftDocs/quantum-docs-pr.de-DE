---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Setdebasisstate-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: 2612bfe488c830abd835be89b2f8ea6795abf675
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194150"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="49deb-102">Setdebasisstate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="49deb-102">SetToBasisState operation</span></span>

<span data-ttu-id="49deb-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="49deb-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="49deb-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="49deb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="49deb-105">Legt ein Qubit auf einen angegebenen Berechnungsbasis Zustand fest, indem das Qubit gemessen und bei Bedarf ein bitflip angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="49deb-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="49deb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="49deb-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="49deb-107">gewünscht: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="49deb-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="49deb-108">Der Basiszustand, auf den das Qubit festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49deb-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="49deb-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="49deb-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="49deb-110">Das Qubit, dessen Zustand festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49deb-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="49deb-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="49deb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="49deb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49deb-112">Remarks</span></span>

<span data-ttu-id="49deb-113">Als invariante dieses Vorgangs wird beim Aufrufen von `M(q)` sofort nach der Wert `SetToBasisState(result, q)` zurückgegeben `result` .</span><span class="sxs-lookup"><span data-stu-id="49deb-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>