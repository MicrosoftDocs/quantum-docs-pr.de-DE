---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: Statepreparationcomplexcoefficients-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: 1d0efa7b83d2e8e75c4b293866f3929f357ec44b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210368"
---
# <a name="statepreparationcomplexcoefficients-function"></a><span data-ttu-id="ae207-102">Statepreparationcomplexcoefficients-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae207-102">StatePreparationComplexCoefficients function</span></span>

<span data-ttu-id="ae207-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="ae207-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="ae207-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae207-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="ae207-105">Statepreparationcomplexkoefficients ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ae207-105">StatePreparationComplexCoefficients has been deprecated.</span></span> <span data-ttu-id="ae207-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP>.</span><span class="sxs-lookup"><span data-stu-id="ae207-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="ae207-107">Gibt einen Vorgang zurück, der einen bestimmten Quantum-Zustand vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="ae207-107">Returns an operation that prepares a specific quantum state.</span></span>

<span data-ttu-id="ae207-108">Der zurückgegebene Vorgang $U $ bereitet einen beliebigen Quantum-Status $ \ket{\psi} $ mit komplexen Koeffizienten $r _J e ^ {i t_j} $ aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="ae207-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="ae207-109">Die Aktion "U" für ein neu zugeordneter Register wird durch "$ $ \begin{align} u\ket {0..." angegeben. 0} = \ket{\psi} = \bruchteil {\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="ae207-109">The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}.</span></span>
<span data-ttu-id="ae207-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="ae207-110">\end{align} $$</span></span>

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="ae207-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae207-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="ae207-112">Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="ae207-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="ae207-113">Array von bis zu $2 ^ n $ komplexen Koeffizienten, die durch ihren absoluten Wert und Phase $ (r_j, t_j) $ dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ae207-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="ae207-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="ae207-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="ae207-115">Ausgabe: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL.</span><span class="sxs-lookup"><span data-stu-id="ae207-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ae207-116">Eine einheitliche Zustands Vorbereitungs Operation $U $.</span><span class="sxs-lookup"><span data-stu-id="ae207-116">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae207-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae207-117">Remarks</span></span>

<span data-ttu-id="ae207-118">Negative Eingabe Koeffizienten $r _J < $0 werden als positiv mit dem Wert $ | r_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="ae207-118">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="ae207-119">`coefficients` wird mit den Elementen $ (r_j, t_j) = (0,0, 0,0) $ aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ae207-119">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>