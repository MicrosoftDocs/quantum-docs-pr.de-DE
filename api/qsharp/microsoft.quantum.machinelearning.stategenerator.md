---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Benutzerdefinierter stategenerator-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: e3026dbae7209acd41924c0038a6f9b2c4b41197
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722401"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="79c34-102">Benutzerdefinierter stategenerator-Typ</span><span class="sxs-lookup"><span data-stu-id="79c34-102">StateGenerator user defined type</span></span>

<span data-ttu-id="79c34-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="79c34-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="79c34-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="79c34-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="79c34-105">Beschreibt einen Vorgang, bei dem eine gegebene Eingabe auf einen sequenziellen Klassifizierer vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="79c34-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="79c34-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="79c34-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="79c34-107">Nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="79c34-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="79c34-108">Die Anzahl der Qubits, für die die codierte Eingabe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="79c34-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit-adj--ctl"></a><span data-ttu-id="79c34-109">Vorbereiten: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="79c34-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="79c34-110">Ein Vorgang, bei dem die codierte Eingabe für ein Little-in-Register-Register von `NQubits` Qubits vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="79c34-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>