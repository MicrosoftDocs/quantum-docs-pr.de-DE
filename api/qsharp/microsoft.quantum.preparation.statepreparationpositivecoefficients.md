---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Statepreparationpositivekoefficients-Funktion
ms.date: 1/23/2021 12:00:00 AM
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
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855844"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="a8c2c-102">Statepreparationpositivekoefficients-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8c2c-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="a8c2c-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="a8c2c-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="a8c2c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8c2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="a8c2c-105">Statepreparationpositivekoefficients ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="a8c2c-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="a8c2c-107">Gibt einen Vorgang zurück, der den gegebenen Quantum-Zustand vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="a8c2c-108">Der zurückgegebene Vorgang $U $ bereitet einen beliebigen Quantum-Status $ \ket{\psi} $ mit positiven Koeffizienten $ \ alpha_j \ge $0 aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0...0} $ vor.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="a8c2c-109">Die Aktion "U" für ein neu zugeordneter Register wird durch "$ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \bruchteil {" angegeben. \ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="a8c2c-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a8c2c-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a8c2c-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8c2c-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a8c2c-112">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a8c2c-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a8c2c-113">Array von bis zu $2 ^ n $ Koeffizienten $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="a8c2c-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="a8c2c-115">Ausgabe: die [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a8c2c-116">Eine einheitliche Zustands Vorbereitungs Operation $U $.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="a8c2c-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a8c2c-117">Example</span></span>

<span data-ttu-id="a8c2c-118">Im folgenden Code Ausschnitt wird der Quantum-Status $ \ket{\psi} = \ sqrt {1/8} \ Ket {0} + \ sqrt {7/8} \ Ket {2} $ im Qubit-Register vorbereitet `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="a8c2c-118">The following snippet prepares the quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="a8c2c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8c2c-119">Remarks</span></span>

<span data-ttu-id="a8c2c-120">Negative Eingabe Koeffizienten $ \ alpha_j < $0 werden als positiv mit dem Wert $ | \ alpha_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-120">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="a8c2c-121">`coefficients` wird mit Elementen $ \ alpha_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-121">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>