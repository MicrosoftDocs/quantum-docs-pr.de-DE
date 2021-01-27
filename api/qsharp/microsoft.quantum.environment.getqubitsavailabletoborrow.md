---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Getqubitsavailabledeausleihen-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: f2294fadb9c10d800b7a743fbfe0810f36f18516
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853248"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="514bd-102">Getqubitsavailabledeausleihen-Vorgang</span><span class="sxs-lookup"><span data-stu-id="514bd-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="514bd-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="514bd-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="514bd-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="514bd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="514bd-105">Gibt die Anzahl der derzeit zur Verfügung stehenden Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="514bd-105">Returns the number of qubits currently available to borrow.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="514bd-106">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="514bd-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="514bd-107">Die Anzahl der Qubits, die ausgeliehen werden könnten und nicht als Teil einer-Anweisung zugeordnet werden `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="514bd-107">The number of qubits that could be borrowed and won't be allocated as part of a `borrowing` statement.</span></span>
<span data-ttu-id="514bd-108">Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="514bd-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="514bd-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="514bd-109">See Also</span></span>

- [<span data-ttu-id="514bd-110">Microsoft. Quantum. Environment. getqubitsavailabletouse</span><span class="sxs-lookup"><span data-stu-id="514bd-110">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)