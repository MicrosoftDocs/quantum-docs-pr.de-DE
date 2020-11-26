---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Getqubitsavailabletouse-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201409"
---
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="d8148-102">Getqubitsavailabletouse-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d8148-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="d8148-103">Namespace: [Microsoft. Quantum. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="d8148-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="d8148-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d8148-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d8148-105">Gibt die Anzahl der zurzeit verfügbaren Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="d8148-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="d8148-106">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d8148-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d8148-107">Die Anzahl der Qubits, die in einer-Anweisung zugeordnet werden können `using` .</span><span class="sxs-lookup"><span data-stu-id="d8148-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="d8148-108">Wenn der verwendete Zielcomputer diese Informationen nicht bereitstellt, `-1` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8148-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8148-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8148-109">See Also</span></span>

- [<span data-ttu-id="d8148-110">Microsoft. Quantum. Environment. getqubitsavailableumausleihen</span><span class="sxs-lookup"><span data-stu-id="d8148-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)