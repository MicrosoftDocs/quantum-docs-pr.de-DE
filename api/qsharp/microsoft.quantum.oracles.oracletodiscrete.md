---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Oracleto Discrete-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724249"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="aa887-102">Oracleto Discrete-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa887-102">OracleToDiscrete function</span></span>

<span data-ttu-id="aa887-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="aa887-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="aa887-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aa887-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aa887-105">Bei einem Vorgang, der ein "Blackbox"-Oracle darstellt, gibt ein diskretes Oracle-Mal zurück, das den mehrfach wiederholten "Black-Box"-Oracle darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa887-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="aa887-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa887-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a><span data-ttu-id="aa887-107">blackboxoracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="aa887-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="aa887-108">Der Vorgang, der exponentiell berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa887-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="aa887-109">Ausgabe: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="aa887-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="aa887-110">Ein Vorgang, der teilweise über das "Blackbox"-Oracle angewendet wird, das das diskrete Zeit-Oracle darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa887-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>