---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Estimatefrequescya-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: f12fc150de5bcea3d53ce88003c71976d8f2467f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204350"
---
# <a name="estimatefrequencya-operation"></a><span data-ttu-id="56e07-102">Estimatefrequescya-Vorgang</span><span class="sxs-lookup"><span data-stu-id="56e07-102">EstimateFrequencyA operation</span></span>

<span data-ttu-id="56e07-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="56e07-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="56e07-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56e07-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56e07-105">Bei einer Vorbereitung, bei der es sich um adjointable und Messungen handelt, schätzt die Häufigkeit, mit der diese Messung erfolgreich ist (gibt zurück `Zero` ), indem eine bestimmte Anzahl von Tests ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56e07-105">Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="56e07-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56e07-106">Input</span></span>

### <a name="preparation--qubit--unit--is-adj"></a><span data-ttu-id="56e07-107">Vorbereitung: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="56e07-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="56e07-108">Ein adjointable-Vorgang $P $, der einen bestimmten Status $ \rho $ für das Eingabe Register vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="56e07-108">An adjointable operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="56e07-109">Messung: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="56e07-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="56e07-110">Ein Vorgang $M $, der die Maßeinheit darstellt.</span><span class="sxs-lookup"><span data-stu-id="56e07-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="56e07-111">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="56e07-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="56e07-112">Die Anzahl der Qubits, die für die Vorbereitung und Messung jeweils ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="56e07-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="56e07-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="56e07-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="56e07-114">Gibt an, wie oft die Messung durchgeführt werden soll, um die gewünschte Häufigkeit einzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="56e07-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="56e07-115">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56e07-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56e07-116">Eine Schätzung von $ \hat{p} $ der Häufigkeit, mit der $M (p (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ zurückgibt `Zero` , wird mithilfe der unausgewogenen Binomial-Schätzung $ \hat{p} = n \_ {\uparamerow}/n \_ {\text{Measurements}} $ abgerufen, wobei $n \_ {\uparamerow} $ die Anzahl der `Zero` beobachteten Ergebnisse ist.</span><span class="sxs-lookup"><span data-stu-id="56e07-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e07-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e07-117">Remarks</span></span>

<span data-ttu-id="56e07-118">Bei adjointable-Vorgängen können bestimmte Annahmen festgelegt werden, z. b. durch das Aufrufen des Vorgangs, dass die Qubits auf genau denselben Zustand vorbereitet werden, sodass Zielcomputer einige Leistungsoptimierungen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="56e07-118">For adjointable operations, certain assumptions can be made such like calling the operation will prepare the qubits to exactly the same state, which allow target machines to make some performance optimizations.</span></span>