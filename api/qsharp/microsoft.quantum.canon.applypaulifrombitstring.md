---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Applypaulifrombitstring-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: cf4c99ec5134fac788cdd4c8a057258790152a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209059"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="8724a-102">Applypaulifrombitstring-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8724a-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="8724a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8724a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8724a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8724a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8724a-105">Wendet einen Pauli-Operator auf jedes Qubit in einem Array an, wenn das entsprechende Bit eines booleschen Arrays mit einer angegebenen Eingabe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8724a-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8724a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8724a-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="8724a-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="8724a-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="8724a-108">Der Pauli-Operator, auf den angewendet wird. `qubits[idx]``bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="8724a-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="8724a-109">bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8724a-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8724a-110">Anwenden von Pauli, wenn Bit dieser Wert ist</span><span class="sxs-lookup"><span data-stu-id="8724a-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="8724a-111">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="8724a-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="8724a-112">Boolesches Register, das angibt, welches entsprechende Qubit in `qubits` operiert werden soll</span><span class="sxs-lookup"><span data-stu-id="8724a-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="8724a-113">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8724a-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8724a-114">Das Quantum-Register, für das der angegebene Pauli-Operator selektiv angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8724a-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="8724a-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8724a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8724a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8724a-116">Remarks</span></span>

<span data-ttu-id="8724a-117">Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8724a-117">The Boolean array and the quantum register must be of equal length.</span></span>