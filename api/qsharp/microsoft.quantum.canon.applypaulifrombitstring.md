---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Applypaulifrombitstring-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: 09754accb92c1339b781003e5722e3c8f5884e6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705106"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="6f10e-102">Applypaulifrombitstring-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6f10e-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="6f10e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6f10e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6f10e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6f10e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6f10e-105">Wendet einen Pauli-Operator auf jedes Qubit in einem Array an, wenn das entsprechende Bit eines booleschen Arrays mit einer angegebenen Eingabe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6f10e-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="6f10e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f10e-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="6f10e-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="6f10e-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="6f10e-108">Der Pauli-Operator, auf den angewendet wird. `qubits[idx]``bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="6f10e-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="6f10e-109">bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6f10e-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6f10e-110">Anwenden von Pauli, wenn Bit dieser Wert ist</span><span class="sxs-lookup"><span data-stu-id="6f10e-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="6f10e-111">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="6f10e-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="6f10e-112">Boolesches Register, das angibt, welches entsprechende Qubit in `qubits` operiert werden soll</span><span class="sxs-lookup"><span data-stu-id="6f10e-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="6f10e-113">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6f10e-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6f10e-114">Das Quantum-Register, für das der angegebene Pauli-Operator selektiv angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f10e-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="6f10e-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6f10e-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6f10e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f10e-116">Remarks</span></span>

<span data-ttu-id="6f10e-117">Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6f10e-117">The Boolean array and the quantum register must be of equal length.</span></span>