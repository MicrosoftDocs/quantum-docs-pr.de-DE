---
uid: Microsoft.Quantum.Measurement.MResetY
title: Mresegty-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 36c6f227135b5ccaf1146fd7afdc8205d416c5dd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227028"
---
# <a name="mresety-operation"></a><span data-ttu-id="89fd5-102">Mresegty-Vorgang</span><span class="sxs-lookup"><span data-stu-id="89fd5-102">MResetY operation</span></span>

<span data-ttu-id="89fd5-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="89fd5-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="89fd5-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="89fd5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="89fd5-105">Misst ein einzelnes Qubit in der Y-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.</span><span class="sxs-lookup"><span data-stu-id="89fd5-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="89fd5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89fd5-106">Description</span></span>

<span data-ttu-id="89fd5-107">Führt eine einzelne Qubit-Messung im $Y $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="89fd5-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="89fd5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89fd5-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="89fd5-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="89fd5-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="89fd5-110">Ein einzelnes Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="89fd5-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="89fd5-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="89fd5-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="89fd5-112">Das Ergebnis der Messung `target` im Pauli-$Y $.</span><span class="sxs-lookup"><span data-stu-id="89fd5-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>