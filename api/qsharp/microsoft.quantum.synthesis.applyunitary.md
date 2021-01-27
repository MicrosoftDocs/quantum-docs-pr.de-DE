---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Applyeinheitlicher-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859215"
---
# <a name="applyunitary-operation"></a><span data-ttu-id="e8421-102">Applyeinheitlicher-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8421-102">ApplyUnitary operation</span></span>

<span data-ttu-id="e8421-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="e8421-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="e8421-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8421-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8421-105">Wendet ein Gate an, das durch die einheitliche Matrix 2 ^ n x 2 ^ n definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8421-105">Applies gate defined by 2^n x 2^n unitary matrix.</span></span>

<span data-ttu-id="e8421-106">Schlägt fehl, wenn die Matrix nicht einheitlich ist oder die falsche Größe aufweist.</span><span class="sxs-lookup"><span data-stu-id="e8421-106">Fails if matrix is not unitary, or has wrong size.</span></span>

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e8421-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e8421-107">Input</span></span>

### <a name="unitary--complex"></a><span data-ttu-id="e8421-108">einheitlich: [Komplex](xref:Microsoft.Quantum.Math.Complex)[] []</span><span class="sxs-lookup"><span data-stu-id="e8421-108">unitary : [Complex](xref:Microsoft.Quantum.Math.Complex)[][]</span></span>

<span data-ttu-id="e8421-109">2 ^ n x 2 ^ n einheitliche Matrix, die den Vorgang beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8421-109">2^n x 2^n unitary matrix describing the operation.</span></span>
<span data-ttu-id="e8421-110">Wenn die Matrix nicht einheitlich oder nicht von der passenden Größe ist, wird von eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e8421-110">If matrix is not unitary or not of suitable size, throws an exception.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="e8421-111">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e8421-111">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e8421-112">Die Qubits, auf die das Vorgangs Register der Länge n angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8421-112">Qubits to which apply the operation - register of length n.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8421-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8421-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

