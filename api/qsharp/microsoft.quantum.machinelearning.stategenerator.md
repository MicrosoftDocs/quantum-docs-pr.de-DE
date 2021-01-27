---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Benutzerdefinierter stategenerator-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854874"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="8cd63-102">Benutzerdefinierter stategenerator-Typ</span><span class="sxs-lookup"><span data-stu-id="8cd63-102">StateGenerator user defined type</span></span>

<span data-ttu-id="8cd63-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8cd63-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8cd63-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8cd63-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="8cd63-105">Beschreibt einen Vorgang, bei dem eine gegebene Eingabe auf einen sequenziellen Klassifizierer vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="8cd63-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="8cd63-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="8cd63-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="8cd63-107">Nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8cd63-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8cd63-108">Die Anzahl der Qubits, für die die codierte Eingabe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cd63-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="8cd63-109">Vorbereiten: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8cd63-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8cd63-110">Ein Vorgang, bei dem die codierte Eingabe für ein Little-in-Register-Register von `NQubits` Qubits vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="8cd63-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>