---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: -Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701940"
---
# <a name="measureallz-operation"></a><span data-ttu-id="dcc91-102">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dcc91-102">MeasureAllZ operation</span></span>

<span data-ttu-id="dcc91-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="dcc91-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="dcc91-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dcc91-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dcc91-105">Misst gemeinsam ein Register von Qubits in der Pauli Z-Basis.</span><span class="sxs-lookup"><span data-stu-id="dcc91-105">Jointly measures a register of qubits in the Pauli Z basis.</span></span>

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a><span data-ttu-id="dcc91-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcc91-106">Description</span></span>

<span data-ttu-id="dcc91-107">Misst ein Register von Qubits im $Z \otimes z \otimes \cdots \otimes z $, das die Parität des gesamten Registers darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcc91-107">Measures a register of qubits in the $Z \otimes Z \otimes \cdots \otimes Z$ basis, representing the parity of the entire register.</span></span>

## <a name="input"></a><span data-ttu-id="dcc91-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dcc91-108">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="dcc91-109">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="dcc91-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="dcc91-110">Das zu messende Register.</span><span class="sxs-lookup"><span data-stu-id="dcc91-110">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="dcc91-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="dcc91-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="dcc91-112">Das Ergebnis der Messung $Z \otimes z \otimes \cdots \otimes z $.</span><span class="sxs-lookup"><span data-stu-id="dcc91-112">The result of measuring $Z \otimes Z \otimes \cdots \otimes Z$.</span></span>