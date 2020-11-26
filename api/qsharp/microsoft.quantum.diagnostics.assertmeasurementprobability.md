---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Assertmessrementwahrscheinlichkeits-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 032b9224ad728f0637596668c2928a889deeba55
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202361"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="a9c0f-102">Assertmessrementwahrscheinlichkeits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a9c0f-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="a9c0f-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a9c0f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a9c0f-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a9c0f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a9c0f-105">Bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.</span><span class="sxs-lookup"><span data-stu-id="a9c0f-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a9c0f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9c0f-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="a9c0f-107">Basen: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="a9c0f-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="a9c0f-108">Ein Maßeffekt zur Bestätigung der Wahrscheinlichkeit von, ausgedrückt als Multi-Qubit-Pauli-Operator.</span><span class="sxs-lookup"><span data-stu-id="a9c0f-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="a9c0f-109">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a9c0f-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a9c0f-110">Ein Register, für das die-Assertion durchführen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9c0f-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="a9c0f-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a9c0f-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="a9c0f-112">Erwartetes Ergebnis von `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="a9c0f-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="a9c0f-113">prob: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a9c0f-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a9c0f-114">Die Wahrscheinlichkeit, mit der das angegebene Ergebnis erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="a9c0f-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="a9c0f-115">msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a9c0f-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a9c0f-116">Eine Meldung, die gemeldet werden soll, wenn die Übersetzung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a9c0f-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="a9c0f-117">Tol: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a9c0f-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="a9c0f-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a9c0f-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a9c0f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9c0f-119">Remarks</span></span>

<span data-ttu-id="a9c0f-120">Beachten Sie, dass die unter-und kontrollierten Versionen dieses Vorgangs die Bedingung nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a9c0f-120">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9c0f-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9c0f-121">See Also</span></span>

- [<span data-ttu-id="a9c0f-122">Microsoft. Quantum. Diagnostics. assertmeasurement</span><span class="sxs-lookup"><span data-stu-id="a9c0f-122">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)