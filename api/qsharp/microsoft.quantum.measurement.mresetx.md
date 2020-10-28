---
uid: Microsoft.Quantum.Measurement.MResetX
title: Mresetx-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: a16d7405388b560edcdb6c36b6668791f7ba1398
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725005"
---
# <a name="mresetx-operation"></a><span data-ttu-id="6e6dc-102">Mresetx-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6e6dc-102">MResetX operation</span></span>

<span data-ttu-id="6e6dc-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="6e6dc-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="6e6dc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6e6dc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6e6dc-105">Misst ein einzelnes Qubit in der X-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="6e6dc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e6dc-106">Description</span></span>

<span data-ttu-id="6e6dc-107">Führt eine einzelne Qubit-Messung im $X $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="6e6dc-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="6e6dc-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e6dc-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="6e6dc-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6e6dc-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6e6dc-110">Ein einzelnes Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="6e6dc-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6e6dc-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="6e6dc-112">Das Ergebnis der Messung `target` im Pauli-$X $.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>