---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: Blockencodingreflectionbylcu-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: b8eff9d207752213ccdf42a9ad80fefb2da07216
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723914"
---
# <a name="blockencodingreflectionbylcu-function"></a><span data-ttu-id="d5ca7-102">Blockencodingreflectionbylcu-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5ca7-102">BlockEncodingReflectionByLCU function</span></span>

<span data-ttu-id="d5ca7-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d5ca7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d5ca7-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5ca7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d5ca7-105">Codiert einen relevanten Operator in eine `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="d5ca7-105">Encodes an operator of interest into a `BlockEncodingReflection`.</span></span>

<span data-ttu-id="d5ca7-106">Dadurch wird ein `BlockEncodingReflection` einheitlicher $U = p\cdot v\cdot P ^ \dagger $ erstellt, der einen Operator $H = \ sum_ {j} | \ alpha_j codiert | U_j $ von Interesse, bei dem es sich um eine lineare Kombination von uniflüssen handelt.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-106">This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="d5ca7-107">In der Regel ist $P $ eine einheitliche Zustands Vorbereitung, z {0} \_ . b. $P \ket a \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ und $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="d5ca7-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5ca7-108">Input</span></span>

### <a name="statepreparation--qubit--unit-adj--ctl"></a><span data-ttu-id="d5ca7-109">statepreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d5ca7-109">statePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d5ca7-110">Ein einheitlicher $P $, der einen bestimmten Ziel Status vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="d5ca7-111">Selector: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d5ca7-111">selector : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d5ca7-112">Ein einheitlicher $V $, der die Komponenten unierungen von $H $ codiert.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="d5ca7-113">Ausgabe: [blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="d5ca7-113">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="d5ca7-114">Ein einheitlicher $U $, der gemeinsam für Register agiert `a` und `s` $H $ codiert und $U "^ {-1} = U $" erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d5ca7-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^{-1} = U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ca7-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5ca7-115">Remarks</span></span>

<span data-ttu-id="d5ca7-116">Diese `BlockEncoding` Implementierung gibt Ihnen die Eigenschaften eines `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="d5ca7-116">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5ca7-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5ca7-117">See Also</span></span>

- [<span data-ttu-id="d5ca7-118">Microsoft. Quantum. Simulation. blockencoding</span><span class="sxs-lookup"><span data-stu-id="d5ca7-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="d5ca7-119">Microsoft. Quantum. Simulation. blockencodingreflection</span><span class="sxs-lookup"><span data-stu-id="d5ca7-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)