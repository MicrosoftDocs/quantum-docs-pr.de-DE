---
uid: Microsoft.Quantum.Measurement.MResetY
title: Mresegty-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 2e41e76a46b68178a8a22b39131d6ca2a8c50b64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854637"
---
# <a name="mresety-operation"></a><span data-ttu-id="6ae86-102">Mresegty-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6ae86-102">MResetY operation</span></span>

<span data-ttu-id="6ae86-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="6ae86-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="6ae86-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6ae86-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6ae86-105">Misst ein einzelnes Qubit in der Y-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.</span><span class="sxs-lookup"><span data-stu-id="6ae86-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="6ae86-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ae86-106">Description</span></span>

<span data-ttu-id="6ae86-107">Führt eine einzelne Qubit-Messung im $Y $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="6ae86-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="6ae86-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ae86-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="6ae86-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6ae86-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6ae86-110">Ein einzelnes Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ae86-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="6ae86-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6ae86-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="6ae86-112">Das Ergebnis der Messung `target` im Pauli-$Y $.</span><span class="sxs-lookup"><span data-stu-id="6ae86-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>