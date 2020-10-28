---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Getqubitsavailabledeausleihen-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702588"
---
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="4014c-102">Getqubitsavailabledeausleihen-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4014c-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="4014c-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="4014c-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="4014c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4014c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4014c-105">Gibt die Anzahl der derzeit zur Verfügung stehenden Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="4014c-105">Returns the number of qubits currently available to borrow.</span></span>
<span data-ttu-id="4014c-106">Dies schließt nicht verwendete Qubits ein. Das heißt, dies schließt die von zurückgegebenen Qubits ein `GetQubitsAvailableToUse` .</span><span class="sxs-lookup"><span data-stu-id="4014c-106">This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="4014c-107">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4014c-107">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4014c-108">Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="4014c-108">The number of qubits that could be allocated in a `borrowing` statement.</span></span>
<span data-ttu-id="4014c-109">Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4014c-109">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="4014c-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4014c-110">See Also</span></span>

- [<span data-ttu-id="4014c-111">Microsoft. Quantum. Environment. getqubitsavailabletouse</span><span class="sxs-lookup"><span data-stu-id="4014c-111">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)