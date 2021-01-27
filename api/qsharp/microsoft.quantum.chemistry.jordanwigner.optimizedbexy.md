---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Optimizedbexy-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 28a7c7877a3d48fd5ba50384d7996017e7cdb14f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837246"
---
# <a name="optimizedbexy-operation"></a><span data-ttu-id="c8369-102">Optimizedbexy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c8369-102">OptimizedBEXY operation</span></span>

<span data-ttu-id="c8369-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="c8369-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="c8369-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c8369-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="c8369-105">Ein einheitlicher $U $, der die Pauli-Zeichenfolge auf $ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1} anwendet... Z_0 $ on Qubits $0.. p $, bedingt an einem Index $z \in \{ 0, 1 \} $ und $p $.</span><span class="sxs-lookup"><span data-stu-id="c8369-105">A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$.</span></span> <span data-ttu-id="c8369-106">Das heißt: $ $ \begin{align} u\ket {z} \ Ket {p} \ Ket {\ PSI} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 \ket{\psi} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="c8369-106">That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$</span></span>

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c8369-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8369-107">Input</span></span>

### <a name="paulibasis--qubit"></a><span data-ttu-id="c8369-108">paulibasis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c8369-108">pauliBasis : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c8369-109">Wenn sich dieses Qubit im Status $ \ket {0} $ befindet, wird $X $ angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8369-109">When this qubit is in state $\ket{0}$, $X$ is applied.</span></span> <span data-ttu-id="c8369-110">Wenn Sie den Status $ \ket {1} $ aufweist, wird $Y $ angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8369-110">When it is in state $\ket{1}$, $Y$ is applied.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="c8369-111">Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c8369-111">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c8369-112">Der Status $ \ket{p} $ dieses Registers bestimmt das Qubit, auf dem $X $ oder $Y $ angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8369-112">The state $\ket{p}$ of this register determines the qubit on which $X$ or $Y$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="c8369-113">targetregiester: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c8369-113">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c8369-114">Das Register der Qubits, auf die die Pauli-Operatoren angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8369-114">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c8369-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c8369-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="c8369-116">References</span><span class="sxs-lookup"><span data-stu-id="c8369-116">References</span></span>

- <span data-ttu-id="c8369-117">Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="c8369-117">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>