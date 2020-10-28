---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Reflectaboutinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706338"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="acfd5-102">Reflectaboutinteger-Vorgang</span><span class="sxs-lookup"><span data-stu-id="acfd5-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="acfd5-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="acfd5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="acfd5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="acfd5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="acfd5-105">Reflektiert ein Quantum-Register über eine angegebene klassische Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="acfd5-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="acfd5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acfd5-106">Description</span></span>

<span data-ttu-id="acfd5-107">Wenn ein Quantum-Register anfänglich im Status $ \ sum_i \ alpha_i \ket{i} $, wobei jede $ \ket{i} $ ein Basiszustand ist, der eine ganze Zahl $i $ darstellt, gibt den Status des Registers zum Basisstatus für eine gegebene Ganzzahl $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $ an.</span><span class="sxs-lookup"><span data-stu-id="acfd5-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="acfd5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acfd5-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="acfd5-109">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="acfd5-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="acfd5-110">Die klassische Ganzzahl, die den Basiszustand indiziert, der reflektiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="acfd5-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="acfd5-111">reg: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="acfd5-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="acfd5-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="acfd5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="acfd5-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="acfd5-113">Remarks</span></span>

<span data-ttu-id="acfd5-114">Dieser Vorgang wird direkt implementiert, ohne dass zusätzliche Qubits explizit zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="acfd5-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>