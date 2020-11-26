---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: -Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227079"
---
# <a name="measureallz-operation"></a><span data-ttu-id="9b879-102">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b879-102">MeasureAllZ operation</span></span>

<span data-ttu-id="9b879-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="9b879-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="9b879-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b879-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b879-105">Misst gemeinsam ein Register von Qubits in der Pauli Z-Basis.</span><span class="sxs-lookup"><span data-stu-id="9b879-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="9b879-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b879-106">Description</span></span>

<span data-ttu-id="9b879-107">Misst ein Register von Qubits im $Z \otimes z \otimes \cdots \otimes z $, das die Parität des gesamten Registers darstellt.</span><span class="sxs-lookup"><span data-stu-id="9b879-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="9b879-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b879-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="9b879-109">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9b879-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9b879-110">Das zu messende Register.</span><span class="sxs-lookup"><span data-stu-id="9b879-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="9b879-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="9b879-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="9b879-112">Das Ergebnis der Messung $Z \otimes z \otimes \cdots \otimes z $.</span><span class="sxs-lookup"><span data-stu-id="9b879-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>