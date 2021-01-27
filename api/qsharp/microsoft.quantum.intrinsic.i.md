---
uid: Microsoft.Quantum.Intrinsic.I
title: I-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: I
qsharp.summary: Performs the identity operation (no-op) on a single qubit.
ms.openlocfilehash: 0af14a9aff20da493e95c7feba6afbb907d3d69f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849406"
---
# <a name="i-operation"></a><span data-ttu-id="4a9a8-102">I-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4a9a8-102">I operation</span></span>

<span data-ttu-id="4a9a8-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="4a9a8-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="4a9a8-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4a9a8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4a9a8-105">Führt den Identitäts Vorgang (No-OP) für ein einzelnes Qubit aus.</span><span class="sxs-lookup"><span data-stu-id="4a9a8-105">Performs the identity operation (no-op) on a single qubit.</span></span>

```qsharp
operation I (target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4a9a8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a9a8-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="4a9a8-107">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4a9a8-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="4a9a8-108">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a9a8-108">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4a9a8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a9a8-109">Remarks</span></span>

<span data-ttu-id="4a9a8-110">Dabei handelt es sich um einen No-op-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4a9a8-110">This is a no-op.</span></span> <span data-ttu-id="4a9a8-111">Sie wird aus Gründen der Vollständigkeit bereitgestellt. manchmal ist es hilfreich, die Identität in einem Algorithmus aufzurufen oder Sie als Parameter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="4a9a8-111">It is provided for completeness and because sometimes it is useful to call the identity in an algorithm or to pass it as a parameter.</span></span>