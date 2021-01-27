---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Estimatefrequency-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 1e044a08718e02d673edab1d6b9d16d7f09618dc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851887"
---
# <a name="estimatefrequency-operation"></a><span data-ttu-id="1313b-102">Estimatefrequency-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1313b-102">EstimateFrequency operation</span></span>

<span data-ttu-id="1313b-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="1313b-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="1313b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1313b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1313b-105">Bei einer Vorbereitung und Messung schätzt die Häufigkeit, mit der diese Messung erfolgreich ist (gibt zurück `Zero` ), indem eine bestimmte Anzahl von Tests ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1313b-105">Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="1313b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1313b-106">Input</span></span>

### <a name="preparation--qubit--unit"></a><span data-ttu-id="1313b-107">Vorbereitung: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1313b-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="1313b-108">Ein Vorgang $P $, der einen bestimmten Zustand $ \rho $ für das Eingabe Register vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="1313b-108">An operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="1313b-109">Messung: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="1313b-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="1313b-110">Ein Vorgang $M $, der die Maßeinheit darstellt.</span><span class="sxs-lookup"><span data-stu-id="1313b-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="1313b-111">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1313b-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1313b-112">Die Anzahl der Qubits, die für die Vorbereitung und Messung jeweils ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1313b-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="1313b-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1313b-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1313b-114">Gibt an, wie oft die Messung durchgeführt werden soll, um die gewünschte Häufigkeit einzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="1313b-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="1313b-115">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1313b-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1313b-116">Eine Schätzung von $ \hat{p} $ der Häufigkeit, mit der $M (p (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ zurückgibt `Zero` , wird mithilfe der unausgewogenen Binomial-Schätzung $ \hat{p} = n \_ {\uparamerow}/n \_ {\text{Measurements}} $ abgerufen, wobei $n \_ {\uparamerow} $ die Anzahl der `Zero` beobachteten Ergebnisse ist.</span><span class="sxs-lookup"><span data-stu-id="1313b-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

<span data-ttu-id="1313b-117">Dies ist besonders wichtig auf Ziel Computern, die physische Beschränkungen berücksichtigen, damit Wahrscheinlichkeiten nicht gemessen werden können.</span><span class="sxs-lookup"><span data-stu-id="1313b-117">This is particularly important on target machines which respect physical limitations, such that probabilities cannot be measured.</span></span>