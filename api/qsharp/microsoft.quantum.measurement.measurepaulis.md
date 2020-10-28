---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: -Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 7348ab3941af391c451d5c66f888cf3b6662cf20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706759"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="3e284-102">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3e284-102">MeasurePaulis operation</span></span>

<span data-ttu-id="3e284-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="3e284-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="3e284-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3e284-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3e284-105">Wenn ein Array von Multi-Qubit-Pauli-Operatoren verwendet wird, werden die einzelnen Measures mit einem angegebenen Mess Gadget versehen und dann das Array der Ergebnisse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e284-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="3e284-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e284-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="3e284-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="3e284-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="3e284-108">Array von multiqubit-Pauli-Operatoren, die gemessen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e284-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="3e284-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3e284-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3e284-110">Registrieren Sie sich, um die angegebenen Operatoren zu messen.</span><span class="sxs-lookup"><span data-stu-id="3e284-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="3e284-111">Gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="3e284-111">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="3e284-112">Der Vorgang, der die Messung eines gegebenen Multi-Qubit-Operators ausführt.</span><span class="sxs-lookup"><span data-stu-id="3e284-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="3e284-113">Ausgabe: __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="3e284-113">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="3e284-114">Das Array von Ergebnissen, das beim Messen der einzelnen Elemente von auf abgerufen wird `paulis` `target` .</span><span class="sxs-lookup"><span data-stu-id="3e284-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>