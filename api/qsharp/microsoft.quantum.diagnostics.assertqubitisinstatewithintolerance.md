---
uid: Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance
title: Assertqubitisinstatewithintoleranz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitIsInStateWithinTolerance
qsharp.summary: >-
  Asserts that a qubit in the expected state.

  `expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$. The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part. The last argument defines the tolerance with which assertion is made.
ms.openlocfilehash: b40c5c4f731190c8c0d00d33718680e5448bf767
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829781"
---
# <a name="assertqubitisinstatewithintolerance-operation"></a><span data-ttu-id="fbb6e-102">Assertqubitisinstatewithintoleranz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fbb6e-102">AssertQubitIsInStateWithinTolerance operation</span></span>

<span data-ttu-id="fbb6e-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fbb6e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fbb6e-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fbb6e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fbb6e-105">Bestätigt, dass ein Qubit im erwarteten Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-105">Asserts that a qubit in the expected state.</span></span>

<span data-ttu-id="fbb6e-106">`expected` stellt einen komplexen Vektor dar, $ \ket{\psi} = \begin{bmatrix}a & b\end {bmatrix} ^ {\mathrm{T}} $.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-106">`expected` represents a complex vector, $\ket{\psi} = \begin{bmatrix}a & b\end{bmatrix}^{\mathrm{T}}$.</span></span>
<span data-ttu-id="fbb6e-107">Das erste Element der Tupel, das jede $a $ darstellt, $b $ der reelle Teil der komplexen Zahl ist, während das zweite Element der imaginäre Teil ist.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-107">The first element of the tuples representing each of $a$, $b$ is the real part of the complex number, while the second one is the imaginary part.</span></span>
<span data-ttu-id="fbb6e-108">Das letzte Argument definiert die Toleranz, mit der die-Assertionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-108">The last argument defines the tolerance with which assertion is made.</span></span>

```qsharp
operation AssertQubitIsInStateWithinTolerance (expected : (Microsoft.Quantum.Math.Complex, Microsoft.Quantum.Math.Complex), register : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="fbb6e-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fbb6e-109">Input</span></span>

### <a name="expected--complexcomplex"></a><span data-ttu-id="fbb6e-110">erwartet: ([Komplex](xref:Microsoft.Quantum.Math.Complex),[Komplex](xref:Microsoft.Quantum.Math.Complex))</span><span class="sxs-lookup"><span data-stu-id="fbb6e-110">expected : ([Complex](xref:Microsoft.Quantum.Math.Complex),[Complex](xref:Microsoft.Quantum.Math.Complex))</span></span>

<span data-ttu-id="fbb6e-111">Es wurden komplexe Verstärkung für "$ \ket {0} $" bzw. "$ \ket $" erwartet {1} .</span><span class="sxs-lookup"><span data-stu-id="fbb6e-111">Expected complex amplitudes for $\ket{0}$ and $\ket{1}$, respectively.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="fbb6e-112">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fbb6e-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fbb6e-113">Qubit, dessen Zustand bestätigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-113">Qubit whose state is to be asserted.</span></span> <span data-ttu-id="fbb6e-114">Beachten Sie, dass dieses Qubit von anderen zugeordneten Qubits getrennt werden und nicht entkoppelt ist.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-114">Note that this qubit is assumed to be separable from other allocated qubits, and not entangled.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="fbb6e-115">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fbb6e-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fbb6e-116">Additiv Toleranz, mit der tatsächliche Verstärkung von der erwarteten Abweichung abweichen darf.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-116">Additive tolerance by which actual amplitudes are allowed to deviate from expected.</span></span>
<span data-ttu-id="fbb6e-117">Weitere Informationen finden Sie weiter unten in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-117">See remarks below for details.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fbb6e-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fbb6e-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="fbb6e-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fbb6e-119">Example</span></span>

```qsharp
using (qubits = Qubit[2]) {
    // Both qubits are initialized as |0〉: a=(1 + 0*i), b=(0 + 0*i)
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[0], 1e-5);
    AssertQubitIsInStateWithinTolerance((Complex(1., 0.), Complex(0., 0.)), qubits[1], 1e-5);
    Y(qubits[1]);
    // Y |0〉 = i |1〉: a=(0 + 0*i), b=(0 + 1*i)
    AssertQubitIsInStateWithinTolerance((Complex(0., 0.), Complex(0., 1.)), qubits[1], 1e-5);
}
```

## <a name="remarks"></a><span data-ttu-id="fbb6e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbb6e-120">Remarks</span></span>

<span data-ttu-id="fbb6e-121">Der folgende Mathematica-Code kann verwendet werden, um Ausdrücke für Mi, MX, my, MZ zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="fbb6e-121">The following Mathematica code can be used to verify expressions for mi, mx, my, mz:</span></span>

```mathematica
{Id, X, Y, Z} = Table[PauliMatrix[k], {k, 0, 3}];
st = {{ reA + I imA }, { reB + I imB} };
M = st . ConjugateTranspose[st];
mx = Tr[M.X] // ComplexExpand;
my = Tr[M.Y] // ComplexExpand;
mz = Tr[M.Z] // ComplexExpand;
mi = Tr[M.Id] // ComplexExpand;
2 m == Id mi + X mx + Z mz + Y my // ComplexExpand // Simplify
```

<span data-ttu-id="fbb6e-122">Die Toleranz ist die $L \_ {\infty} $ Distance zwischen 3 dimensionalem Real Vector (x, x ₃, x ₄) definiert durch $ \langle\psi | \psi\rangle = x \_ 1 I + x \_ 2 x + x \_ 3 Y + x \_ 4 Z $ und Real Vector (Y. y ₃, y ₄) definiert durch p = Y ₁ I + y. x + y ₃ y + y ₄ Z WHERE p ist die Dichte Matrix, die dem Status des Registers entspricht.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-122">The tolerance is the $L\_{\infty}$ distance between 3 dimensional real vector (x₂,x₃,x₄) defined by $\langle\psi|\psi\rangle = x\_1 I + x\_2 X + x\_3 Y + x\_4 Z$ and real vector (y₂,y₃,y₄) defined by ρ = y₁I + y₂X + y₃Y + y₄Z where ρ is the density matrix corresponding to the state of the register.</span></span>
<span data-ttu-id="fbb6e-123">Dies gilt nur unter der Annahme, dass TR (p) und TR (| ψ ⟩ ⟨ ψ |) gleich 1 sind (z. b. x ₁ = 1/2, y ₁ = 1/2).</span><span class="sxs-lookup"><span data-stu-id="fbb6e-123">This is only true under the assumption that Tr(ρ) and Tr(|ψ⟩⟨ψ|) are both 1 (e.g. x₁ = 1/2, y₁ = 1/2).</span></span>
<span data-ttu-id="fbb6e-124">Wenn dies nicht der Fall ist, wird durch die-Funktion bestätigt, dass der Abstand zwischen (x, x ₁, x ₃-x ₁, x ₄-x ₁, x ₄ + x ₁) und (y, y ₁, y ₃-y ₁, y ₄-y ₁, y ₄ + y ₁) kleiner ist als der Tolerance-Parameter.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-124">If this is not the case, the function asserts that l∞ distance between (x₂-x₁,x₃-x₁,x₄-x₁,x₄+x₁) and (y₂-y₁,y₃-y₁,y₄-y₁,y₄+y₁) is less than the tolerance parameter.</span></span>