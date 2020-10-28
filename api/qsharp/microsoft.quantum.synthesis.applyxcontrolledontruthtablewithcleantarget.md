---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Applyxcontrolledontruthtablewithcleantarget-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: b43a5351985339bcf7c1f2bbe03ae6dc6dfdd165
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725230"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a><span data-ttu-id="b5810-102">Applyxcontrolledontruthtablewithcleantarget-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5810-102">ApplyXControlledOnTruthTableWithCleanTarget operation</span></span>

<span data-ttu-id="b5810-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b5810-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b5810-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b5810-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b5810-105">Wendet den @"microsoft.quantum.intrinsic.x" Vorgang auf an `target` , wenn die boolesche Funktion `func` für die klassische Zuweisung in als true ausgewertet wird `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="b5810-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="b5810-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5810-106">Description</span></span>

<span data-ttu-id="b5810-107">Mit diesem Vorgang wird ein Sonderfall von implementiert @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , bei dem das Ziel-Qubit bekanntermaßen im $ \ket {0} $-Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="b5810-107">This operation implements a special case of @"microsoft.quantum.synthesis.applyxcontrolledontruthtable", in which the target qubit is known to be in the $\ket{0}$ state.</span></span>

<span data-ttu-id="b5810-108">Die-Implementierung nutzt @"microsoft.quantum.intrinsic.cnot" und @"microsoft.quantum.intrinsic.r1" Gates.</span><span class="sxs-lookup"><span data-stu-id="b5810-108">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>  <span data-ttu-id="b5810-109">Die Implementierung des Adjoint-Vorgangs ist optimiert und verwendet eine maßbasierte unberechnung.</span><span class="sxs-lookup"><span data-stu-id="b5810-109">The implementation of the adjoint operation is optimized and uses measurement-based uncomputation.</span></span>

## <a name="input"></a><span data-ttu-id="b5810-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5810-110">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="b5810-111">Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b5810-111">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b5810-112">Boolesche Wahrheitstabelle, dargestellt als große ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="b5810-112">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="b5810-113">controlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b5810-113">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b5810-114">Register von Steuerungs Qubits</span><span class="sxs-lookup"><span data-stu-id="b5810-114">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b5810-115">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b5810-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b5810-116">Ziel-Qubit (muss in $ \ket {0} $ State sein)</span><span class="sxs-lookup"><span data-stu-id="b5810-116">Target qubit (must be in $\ket{0}$ state)</span></span>



## <a name="output--unit"></a><span data-ttu-id="b5810-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b5810-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="b5810-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5810-118">See Also</span></span>

- [<span data-ttu-id="b5810-119">Microsoft. Quantum. Synthese. applyxcontrolledontruthtable</span><span class="sxs-lookup"><span data-stu-id="b5810-119">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)