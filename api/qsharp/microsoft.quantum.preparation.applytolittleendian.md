---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Applydelittleendian-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: d94a9969a3f827d594946ab8ca6cd4672da7ef7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724109"
---
# <a name="applytolittleendian-operation"></a><span data-ttu-id="8e6e6-102">Applydelittleendian-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8e6e6-102">ApplyToLittleEndian operation</span></span>

<span data-ttu-id="8e6e6-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="8e6e6-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="8e6e6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8e6e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8e6e6-105">Wendet einen Vorgang auf die zugrunde liegenden Qubits an, die ein Little-in-sdian-Register bilden.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-105">Applies an operation to the underlying qubits making up a little-endian register.</span></span> <span data-ttu-id="8e6e6-106">Dieser Vorgang wird als "intern" gekennzeichnet, da ein Little-te-Register als "nicht transparent" bezeichnet werden soll, sodass es sich hierbei nur um ein Implementierungsdetail handelt.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-106">This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.</span></span>

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="8e6e6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e6e6-107">Input</span></span>

### <a name="bareop--qubit--unit-adj--ctl"></a><span data-ttu-id="8e6e6-108">bareop: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8e6e6-108">bareOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="register--littleendian"></a><span data-ttu-id="8e6e6-109">Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8e6e6-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="8e6e6-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e6e6-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

