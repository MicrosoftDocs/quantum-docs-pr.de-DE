---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Mresetz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: fc9ba6576b56d7df1a57334e1da46b9c48376ecb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853743"
---
# <a name="mresetz-operation"></a><span data-ttu-id="4074f-102">Mresetz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4074f-102">MResetZ operation</span></span>

<span data-ttu-id="4074f-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="4074f-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="4074f-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4074f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4074f-105">Misst ein einzelnes Qubit in der Z-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.</span><span class="sxs-lookup"><span data-stu-id="4074f-105">Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="4074f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4074f-106">Description</span></span>

<span data-ttu-id="4074f-107">Führt eine einzelne Qubit-Messung im $Z $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="4074f-107">Performs a single-qubit measurement in the $Z$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="4074f-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4074f-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="4074f-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4074f-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="4074f-110">Ein einzelnes Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4074f-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="4074f-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="4074f-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="4074f-112">Das Ergebnis der Messung `target` im Pauli-$Z $.</span><span class="sxs-lookup"><span data-stu-id="4074f-112">The result of measuring `target` in the Pauli $Z$ basis.</span></span>