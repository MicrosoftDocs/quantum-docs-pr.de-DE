---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: -Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 1bc14ec8e7c608d1195a03a354c71e870594f86d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853769"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="697cf-102">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="697cf-102">MeasurePaulis operation</span></span>

<span data-ttu-id="697cf-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="697cf-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="697cf-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="697cf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="697cf-105">Wenn ein Array von Multi-Qubit-Pauli-Operatoren verwendet wird, werden die einzelnen Measures mit einem angegebenen Mess Gadget versehen und dann das Array der Ergebnisse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="697cf-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="697cf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="697cf-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="697cf-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="697cf-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="697cf-108">Array von multiqubit-Pauli-Operatoren, die gemessen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="697cf-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="697cf-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="697cf-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="697cf-110">Registrieren Sie sich, um die angegebenen Operatoren zu messen.</span><span class="sxs-lookup"><span data-stu-id="697cf-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="697cf-111">Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="697cf-111">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="697cf-112">Der Vorgang, der die Messung eines gegebenen Multi-Qubit-Operators ausführt.</span><span class="sxs-lookup"><span data-stu-id="697cf-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="697cf-113">Ausgabe: __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="697cf-113">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="697cf-114">Das Array von Ergebnissen, das beim Messen der einzelnen Elemente von auf abgerufen wird `paulis` `target` .</span><span class="sxs-lookup"><span data-stu-id="697cf-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>