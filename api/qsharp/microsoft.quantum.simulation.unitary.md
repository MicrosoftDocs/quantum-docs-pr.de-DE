---
uid: Microsoft.Quantum.Simulation.Unitary
title: Einheitlicher benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: Unitary
qsharp.summary: Represents evolution under a unitary operator.
ms.openlocfilehash: f148b59d2445f964fc0332e2010571a0ace2d4ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858395"
---
# <a name="unitary-user-defined-type"></a><span data-ttu-id="9611a-102">Einheitlicher benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="9611a-102">Unitary user defined type</span></span>

<span data-ttu-id="9611a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9611a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9611a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9611a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9611a-105">Stellt die Weiterentwicklung unter einem einheitlichen Operator dar.</span><span class="sxs-lookup"><span data-stu-id="9611a-105">Represents evolution under a unitary operator.</span></span>

```qsharp

newtype Unitary = ((Qubit[] => Unit is Adj + Ctl));
```

