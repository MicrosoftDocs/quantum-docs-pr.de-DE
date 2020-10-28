---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Getqubitsavailabletouse-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702587"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="137c5-102">Getqubitsavailabletouse-Vorgang</span><span class="sxs-lookup"><span data-stu-id="137c5-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="137c5-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="137c5-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="137c5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="137c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="137c5-105">Gibt die Anzahl der zurzeit verfügbaren Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="137c5-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="137c5-106">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="137c5-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="137c5-107">Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `using` .</span><span class="sxs-lookup"><span data-stu-id="137c5-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="137c5-108">Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="137c5-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="137c5-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="137c5-109">See Also</span></span>

- [<span data-ttu-id="137c5-110">Microsoft. Quantum. Environment. getqubitsavailableumausleihen</span><span class="sxs-lookup"><span data-stu-id="137c5-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)