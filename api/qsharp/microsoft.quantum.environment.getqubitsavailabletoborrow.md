---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Getqubitsavailabledeausleihen-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: 30b97c2b6e1353f008d085c3bae6160763557c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201460"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="ba7c5-102">Getqubitsavailabledeausleihen-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ba7c5-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="ba7c5-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="ba7c5-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="ba7c5-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ba7c5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ba7c5-105">Gibt die Anzahl der derzeit zur Verfügung stehenden Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="ba7c5-105">Returns the number of qubits currently available to borrow.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="ba7c5-106">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ba7c5-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ba7c5-107">Die Anzahl der Qubits, die ausgeliehen werden könnten und nicht als Teil einer-Anweisung zugeordnet werden `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="ba7c5-107">The number of qubits that could be borrowed and won't be allocated as part of a `borrowing` statement.</span></span>
<span data-ttu-id="ba7c5-108">Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba7c5-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba7c5-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ba7c5-109">See Also</span></span>

- [<span data-ttu-id="ba7c5-110">Microsoft. Quantum. Environment. getqubitsavailabletouse</span><span class="sxs-lookup"><span data-stu-id="ba7c5-110">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)