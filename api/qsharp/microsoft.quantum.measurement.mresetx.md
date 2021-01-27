---
uid: Microsoft.Quantum.Measurement.MResetX
title: Mresetx-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 44459e681daf1d28ce7d45f91ad59059babe5716
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853754"
---
# <a name="mresetx-operation"></a><span data-ttu-id="949da-102">Mresetx-Vorgang</span><span class="sxs-lookup"><span data-stu-id="949da-102">MResetX operation</span></span>

<span data-ttu-id="949da-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="949da-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="949da-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="949da-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="949da-105">Misst ein einzelnes Qubit in der X-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.</span><span class="sxs-lookup"><span data-stu-id="949da-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="949da-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="949da-106">Description</span></span>

<span data-ttu-id="949da-107">Führt eine einzelne Qubit-Messung im $X $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="949da-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="949da-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="949da-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="949da-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="949da-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="949da-110">Ein einzelnes Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="949da-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="949da-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="949da-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="949da-112">Das Ergebnis der Messung `target` im Pauli-$X $.</span><span class="sxs-lookup"><span data-stu-id="949da-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>