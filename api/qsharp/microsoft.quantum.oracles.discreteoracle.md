---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: Benutzerdefinierter Typ "diskreteoracle"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: accbd7b88cc2f6522da20ec1959492310ff0e743
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193895"
---
# <a name="discreteoracle-user-defined-type"></a><span data-ttu-id="1acc8-102">Benutzerdefinierter Typ "diskreteoracle"</span><span class="sxs-lookup"><span data-stu-id="1acc8-102">DiscreteOracle user defined type</span></span>

<span data-ttu-id="1acc8-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="1acc8-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="1acc8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1acc8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1acc8-105">Stellt ein diskretes Oracle dar.</span><span class="sxs-lookup"><span data-stu-id="1acc8-105">Represents a discrete-time oracle.</span></span>

<span data-ttu-id="1acc8-106">Dies ist ein Oracle, das $U ^ m $ für einen Fixed-Vorgang implementiert $U $ und eine nicht negative ganze Zahl $m $.</span><span class="sxs-lookup"><span data-stu-id="1acc8-106">This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.</span></span>

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

