---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: Blockencodingbylcu-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 04738aa54ce8b719b05954824e3553388a995df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724865"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="d8722-102">Blockencodingbylcu-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8722-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="d8722-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d8722-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d8722-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d8722-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d8722-105">Codiert einen relevanten Operator in eine `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="d8722-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="d8722-106">Dadurch wird ein `BlockEncoding` einheitlicher $U = p\cdot v\cdot P ^ \dagger $ erstellt, der einen Operator $H = \ sum_ {j} | \ alpha_j codiert | U_j $ von Interesse, bei dem es sich um eine lineare Kombination von uniflüssen handelt.</span><span class="sxs-lookup"><span data-stu-id="d8722-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="d8722-107">In der Regel ist $P $ eine einheitliche Zustands Vorbereitung, z. b. $P \ket {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ und $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $.</span><span class="sxs-lookup"><span data-stu-id="d8722-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="d8722-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8722-108">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="d8722-109">statepreparation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d8722-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d8722-110">Ein einheitlicher $P $, der einen bestimmten Ziel Status vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d8722-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="d8722-111">Selektor: ('t, es) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d8722-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d8722-112">Ein einheitlicher $V $, der die Komponenten unierungen von $H $ codiert.</span><span class="sxs-lookup"><span data-stu-id="d8722-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit-adj--ctl"></a><span data-ttu-id="d8722-113">Ausgabe: ('t, es) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d8722-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="d8722-114">Ein einheitlicher $U $, der gemeinsam für Register fungiert `a` und `s` $H $ codiert und $U ^ \dagger = U $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="d8722-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d8722-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d8722-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d8722-116">GIF</span><span class="sxs-lookup"><span data-stu-id="d8722-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="d8722-117">Spaniens</span><span class="sxs-lookup"><span data-stu-id="d8722-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="d8722-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d8722-118">Remarks</span></span>

<span data-ttu-id="d8722-119">Diese `BlockEncoding` Implementierung gibt Ihnen die Eigenschaften eines `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="d8722-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8722-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8722-120">See Also</span></span>

- [<span data-ttu-id="d8722-121">Microsoft. Quantum. Simulation. blockencoding</span><span class="sxs-lookup"><span data-stu-id="d8722-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="d8722-122">Microsoft. Quantum. Simulation. blockencodingreflection</span><span class="sxs-lookup"><span data-stu-id="d8722-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)