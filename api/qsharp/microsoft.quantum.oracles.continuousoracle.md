---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Continuousoracle-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: ac254b7556878550216d5c0c9222620fdc5c5702
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855931"
---
# <a name="continuousoracle-user-defined-type"></a><span data-ttu-id="638cb-102">Continuousoracle-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="638cb-102">ContinuousOracle user defined type</span></span>

<span data-ttu-id="638cb-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="638cb-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="638cb-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="638cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="638cb-105">Stellt ein kontinuierliches Oracle dar.</span><span class="sxs-lookup"><span data-stu-id="638cb-105">Represents a continuous-time oracle.</span></span>

<span data-ttu-id="638cb-106">Dies ist ein Oracle, das $U (\delta t): \ket{\psi (t)} \mapsto \ket{\psi (t + \delta t)} $ für alle Male $t $ implementiert, wobei $U $ ein fester Vorgang ist und $ \delta t $ eine nicht negative reelle Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="638cb-106">This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.</span></span>

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

