---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Oracleto Discrete-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842538"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="28ebf-102">Oracleto Discrete-Funktion</span><span class="sxs-lookup"><span data-stu-id="28ebf-102">OracleToDiscrete function</span></span>

<span data-ttu-id="28ebf-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="28ebf-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="28ebf-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28ebf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28ebf-105">Bei einem Vorgang, der ein "Blackbox"-Oracle darstellt, gibt ein diskretes Oracle-Mal zurück, das den mehrfach wiederholten "Black-Box"-Oracle darstellt.</span><span class="sxs-lookup"><span data-stu-id="28ebf-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="28ebf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="28ebf-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a><span data-ttu-id="28ebf-107">blackboxoracle: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="28ebf-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="28ebf-108">Der Vorgang, der exponentiell berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="28ebf-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="28ebf-109">Ausgabe: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="28ebf-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="28ebf-110">Ein Vorgang, der teilweise über das "Blackbox"-Oracle angewendet wird, das das diskrete Zeit-Oracle darstellt.</span><span class="sxs-lookup"><span data-stu-id="28ebf-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>

## <a name="example"></a><span data-ttu-id="28ebf-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28ebf-111">Example</span></span>

<span data-ttu-id="28ebf-112">`OracleToDiscrete(U)(3, target)` entspricht dreimal der `U(target)` Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="28ebf-112">`OracleToDiscrete(U)(3, target)` is equivalent to `U(target)` repeated three times.</span></span>