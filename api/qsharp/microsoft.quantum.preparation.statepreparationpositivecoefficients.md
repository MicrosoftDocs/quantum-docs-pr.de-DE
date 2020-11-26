---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Statepreparationpositivekoefficients-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 8f1fd7d77531996faf566adb78f452929d6cbd50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193249"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="a85e7-102">Statepreparationpositivekoefficients-Funktion</span><span class="sxs-lookup"><span data-stu-id="a85e7-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="a85e7-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="a85e7-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="a85e7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a85e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="a85e7-105">Statepreparationpositivekoefficients ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a85e7-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="a85e7-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>.</span><span class="sxs-lookup"><span data-stu-id="a85e7-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="a85e7-107">Gibt einen Vorgang zurück, der den gegebenen Quantum-Zustand vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="a85e7-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="a85e7-108">Der zurückgegebene Vorgang $U $ bereitet einen beliebigen Quantum-Status $ \ket{\psi} $ mit positiven Koeffizienten $ \ alpha_j \ge $0 aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0...0} $ vor.</span><span class="sxs-lookup"><span data-stu-id="a85e7-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="a85e7-109">Die Aktion "U" für ein neu zugeordneter Register wird durch "$ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \bruchteil {" angegeben. \ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="a85e7-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="a85e7-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a85e7-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a85e7-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a85e7-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a85e7-112">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a85e7-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a85e7-113">Array von bis zu $2 ^ n $ Koeffizienten $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="a85e7-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="a85e7-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="a85e7-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="a85e7-115">Ausgabe: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL.</span><span class="sxs-lookup"><span data-stu-id="a85e7-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a85e7-116">Eine einheitliche Zustands Vorbereitungs Operation $U $.</span><span class="sxs-lookup"><span data-stu-id="a85e7-116">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="a85e7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a85e7-117">Remarks</span></span>

<span data-ttu-id="a85e7-118">Negative Eingabe Koeffizienten $ \ alpha_j < $0 werden als positiv mit dem Wert $ | \ alpha_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="a85e7-118">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="a85e7-119">`coefficients` wird mit Elementen $ \ alpha_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a85e7-119">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>