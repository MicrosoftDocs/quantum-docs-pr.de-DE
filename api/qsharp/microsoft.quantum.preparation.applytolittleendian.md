---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Applydelittleendian-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: 1194ac369d2d474330357d26dd22709e9c68dd6e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226484"
---
# <a name="applytolittleendian-operation"></a><span data-ttu-id="d2e93-102">Applydelittleendian-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2e93-102">ApplyToLittleEndian operation</span></span>

<span data-ttu-id="d2e93-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d2e93-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d2e93-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d2e93-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d2e93-105">Wendet einen Vorgang auf die zugrunde liegenden Qubits an, die ein Little-in-sdian-Register bilden.</span><span class="sxs-lookup"><span data-stu-id="d2e93-105">Applies an operation to the underlying qubits making up a little-endian register.</span></span> <span data-ttu-id="d2e93-106">Dieser Vorgang wird als "intern" gekennzeichnet, da ein Little-te-Register als "nicht transparent" bezeichnet werden soll, sodass es sich hierbei nur um ein Implementierungsdetail handelt.</span><span class="sxs-lookup"><span data-stu-id="d2e93-106">This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.</span></span>

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d2e93-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2e93-107">Input</span></span>

### <a name="bareop--qubit--unit--is-adj--ctl"></a><span data-ttu-id="d2e93-108">bareop: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d2e93-108">bareOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="register--littleendian"></a><span data-ttu-id="d2e93-109">Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d2e93-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="d2e93-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d2e93-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

