---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Statepreparationpositivekoefficients-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722892"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="bc8b1-102">Statepreparationpositivekoefficients-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc8b1-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="bc8b1-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="bc8b1-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="bc8b1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bc8b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bc8b1-105">Gibt einen Vorgang zurück, der den gegebenen Quantum-Zustand vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-105">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="bc8b1-106">Der zurückgegebene Vorgang $U $ bereitet einen beliebigen Quantum-Status $ \ket{\psi} $ mit positiven Koeffizienten $ \ alpha_j \ge $0 aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0...0} $ vor.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-106">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="bc8b1-107">Die Aktion "U" für ein neu zugeordneter Register wird durch "$ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \bruchteil {" angegeben. \ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-107">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="bc8b1-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="bc8b1-108">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="bc8b1-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bc8b1-109">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="bc8b1-110">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bc8b1-110">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bc8b1-111">Array von bis zu $2 ^ n $ Koeffizienten $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-111">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="bc8b1-112">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-112">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit-adj--ctl"></a><span data-ttu-id="bc8b1-113">Ausgabe: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="bc8b1-113">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="bc8b1-114">Eine einheitliche Zustands Vorbereitungs Operation $U $.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-114">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8b1-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc8b1-115">Remarks</span></span>

<span data-ttu-id="bc8b1-116">Negative Eingabe Koeffizienten $ \ alpha_j < $0 werden als positiv mit dem Wert $ | \ alpha_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-116">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="bc8b1-117">`coefficients` wird mit Elementen $ \ alpha_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-117">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>