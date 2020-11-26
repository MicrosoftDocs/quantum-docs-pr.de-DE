---
uid: Microsoft.Quantum.Measurement.MResetX
title: Mresetx-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 04fb0f84ddf79a3d2cfc21fdaabd16c129f6d72f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194201"
---
# <a name="mresetx-operation"></a><span data-ttu-id="9878f-102">Mresetx-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9878f-102">MResetX operation</span></span>

<span data-ttu-id="9878f-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="9878f-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="9878f-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9878f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9878f-105">Misst ein einzelnes Qubit in der X-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.</span><span class="sxs-lookup"><span data-stu-id="9878f-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="9878f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9878f-106">Description</span></span>

<span data-ttu-id="9878f-107">Führt eine einzelne Qubit-Messung im $X $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="9878f-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="9878f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9878f-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="9878f-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9878f-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9878f-110">Ein einzelnes Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9878f-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9878f-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="9878f-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="9878f-112">Das Ergebnis der Messung `target` im Pauli-$X $.</span><span class="sxs-lookup"><span data-stu-id="9878f-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>