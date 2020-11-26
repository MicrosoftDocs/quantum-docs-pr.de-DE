---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Reflectaboutinteger-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: d4bae0cba5ee45e8d48070e36efab0159ade9137
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222370"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="fa9fa-102">Reflectaboutinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fa9fa-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="fa9fa-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="fa9fa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="fa9fa-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fa9fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fa9fa-105">Reflektiert ein Quantum-Register über eine angegebene klassische Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="fa9fa-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="fa9fa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa9fa-106">Description</span></span>

<span data-ttu-id="fa9fa-107">Wenn ein Quantum-Register anfänglich im Status $ \ sum_i \ alpha_i \ket{i} $, wobei jede $ \ket{i} $ ein Basiszustand ist, der eine ganze Zahl $i $ darstellt, gibt den Status des Registers zum Basisstatus für eine gegebene Ganzzahl $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $ an.</span><span class="sxs-lookup"><span data-stu-id="fa9fa-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="fa9fa-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fa9fa-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="fa9fa-109">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fa9fa-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fa9fa-110">Die klassische Ganzzahl, die den Basiszustand indiziert, der reflektiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa9fa-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="fa9fa-111">reg: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fa9fa-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="fa9fa-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa9fa-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fa9fa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa9fa-113">Remarks</span></span>

<span data-ttu-id="fa9fa-114">Dieser Vorgang wird direkt implementiert, ohne dass zusätzliche Qubits explizit zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fa9fa-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>