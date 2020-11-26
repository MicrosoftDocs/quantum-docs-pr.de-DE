---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Oracleto Discrete-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: 158a90bbd0c68406e0a8507ae99fc08fad3b6d19
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193844"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="532d9-102">Oracleto Discrete-Funktion</span><span class="sxs-lookup"><span data-stu-id="532d9-102">OracleToDiscrete function</span></span>

<span data-ttu-id="532d9-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="532d9-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="532d9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="532d9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="532d9-105">Bei einem Vorgang, der ein "Blackbox"-Oracle darstellt, gibt ein diskretes Oracle-Mal zurück, das den mehrfach wiederholten "Black-Box"-Oracle darstellt.</span><span class="sxs-lookup"><span data-stu-id="532d9-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="532d9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="532d9-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a><span data-ttu-id="532d9-107">blackboxoracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="532d9-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="532d9-108">Der Vorgang, der exponentiell berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="532d9-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="532d9-109">Ausgabe: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="532d9-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="532d9-110">Ein Vorgang, der teilweise über das "Blackbox"-Oracle angewendet wird, das das diskrete Zeit-Oracle darstellt.</span><span class="sxs-lookup"><span data-stu-id="532d9-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>