---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Erstellungs Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 4173aa9daac08a3febdfcbf12dc236f797685436
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854658"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="6e1de-102">Erstellungs Vorgang</span><span class="sxs-lookup"><span data-stu-id="6e1de-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="6e1de-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="6e1de-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="6e1de-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e1de-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e1de-105">Misst den angegebenen Pauli-Operator mithilfe eines expliziten Scratch-Qubit, um die Messung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6e1de-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="6e1de-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e1de-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="6e1de-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="6e1de-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="6e1de-108">Ein Multi-Qubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e1de-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6e1de-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6e1de-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6e1de-110">Die zu messende Qubit-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="6e1de-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="6e1de-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6e1de-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="6e1de-112">Das Ergebnis der Messung des angegebenen Pauli-Operators für das `target` Register.</span><span class="sxs-lookup"><span data-stu-id="6e1de-112">The result of measuring the given Pauli operator on the `target` register.</span></span>