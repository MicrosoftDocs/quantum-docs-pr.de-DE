---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Erstellungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 1ee25dbccd5bddde406cf8ed84dff77d96d7804e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706746"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="d52e1-102">Erstellungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="d52e1-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="d52e1-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="d52e1-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="d52e1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d52e1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d52e1-105">Misst den angegebenen Pauli-Operator mithilfe eines expliziten Scratch-Qubit, um die Messung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d52e1-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="d52e1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d52e1-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="d52e1-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d52e1-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d52e1-108">Ein Multi-Qubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d52e1-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d52e1-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d52e1-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d52e1-110">Die zu messende Qubit-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d52e1-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d52e1-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="d52e1-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="d52e1-112">Das Ergebnis der Messung des angegebenen Pauli-Operators für das `target` Register.</span><span class="sxs-lookup"><span data-stu-id="d52e1-112">The result of measuring the given Pauli operator on the `target` register.</span></span>