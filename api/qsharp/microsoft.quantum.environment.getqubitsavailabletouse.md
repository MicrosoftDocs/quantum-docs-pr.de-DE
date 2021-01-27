---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Getqubitsavailabletouse-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 2ed8c3789331a15b351769be960d06f6364d8047
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827799"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="e992d-102">Getqubitsavailabletouse-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e992d-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="e992d-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="e992d-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="e992d-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e992d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e992d-105">Gibt die Anzahl der zurzeit verfügbaren Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="e992d-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="e992d-106">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e992d-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e992d-107">Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `using` .</span><span class="sxs-lookup"><span data-stu-id="e992d-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="e992d-108">Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e992d-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="e992d-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e992d-109">See Also</span></span>

- [<span data-ttu-id="e992d-110">Microsoft. Quantum. Environment. getqubitsavailableumausleihen</span><span class="sxs-lookup"><span data-stu-id="e992d-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)