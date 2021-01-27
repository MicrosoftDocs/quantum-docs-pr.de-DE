---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Assertmessrementwahrscheinlichkeits-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830821"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="87d6e-102">Assertmessrementwahrscheinlichkeits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="87d6e-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="87d6e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="87d6e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="87d6e-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="87d6e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="87d6e-105">Bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.</span><span class="sxs-lookup"><span data-stu-id="87d6e-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="87d6e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="87d6e-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="87d6e-107">Basen: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="87d6e-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="87d6e-108">Ein Maßeffekt zur Bestätigung der Wahrscheinlichkeit von, ausgedrückt als Multi-Qubit-Pauli-Operator.</span><span class="sxs-lookup"><span data-stu-id="87d6e-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="87d6e-109">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="87d6e-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="87d6e-110">Ein Register, für das die-Assertion durchführen werden soll.</span><span class="sxs-lookup"><span data-stu-id="87d6e-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="87d6e-111">Ergebnis: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="87d6e-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="87d6e-112">Erwartetes Ergebnis von `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="87d6e-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="87d6e-113">prob: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="87d6e-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="87d6e-114">Die Wahrscheinlichkeit, mit der das angegebene Ergebnis erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="87d6e-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="87d6e-115">msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="87d6e-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="87d6e-116">Eine Meldung, die gemeldet werden soll, wenn die Übersetzung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="87d6e-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="87d6e-117">Tol: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="87d6e-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="87d6e-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="87d6e-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="87d6e-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="87d6e-119">Example</span></span>

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a><span data-ttu-id="87d6e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87d6e-120">Remarks</span></span>

<span data-ttu-id="87d6e-121">Beachten Sie, dass die unter-und kontrollierten Versionen dieses Vorgangs die Bedingung nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="87d6e-121">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="87d6e-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="87d6e-122">See Also</span></span>

- [<span data-ttu-id="87d6e-123">Microsoft. Quantum. Diagnostics. assertmeasurement</span><span class="sxs-lookup"><span data-stu-id="87d6e-123">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)