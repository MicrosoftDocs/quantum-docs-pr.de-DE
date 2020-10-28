---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: Optimizedbexy-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 359d347fc57be46200a218646911a7a400b4a96d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703157"
---
# <a name="optimizedbexy-operation"></a><span data-ttu-id="03284-102">Optimizedbexy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03284-102">OptimizedBEXY operation</span></span>

<span data-ttu-id="03284-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="03284-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="03284-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03284-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03284-105">Ein einheitlicher $U $, der die Pauli-Zeichenfolge auf $ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1} anwendet... Z_0 $ on Qubits $0.. p $, bedingt an einem Index $z \in \{ 0, 1 \} $ und $p $.</span><span class="sxs-lookup"><span data-stu-id="03284-105">A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$.</span></span> <span data-ttu-id="03284-106">Das heißt: $ $ \begin{align} u\ket {z} \ Ket {p} \ Ket {\ PSI} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}... Z_0 \ket{\psi} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="03284-106">That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$</span></span>

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="03284-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="03284-107">Input</span></span>

### <a name="paulibasis--qubit"></a><span data-ttu-id="03284-108">paulibasis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="03284-108">pauliBasis : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="03284-109">Wenn sich dieses Qubit im Status $ \ket {0} $ befindet, wird $X $ angewendet.</span><span class="sxs-lookup"><span data-stu-id="03284-109">When this qubit is in state $\ket{0}$, $X$ is applied.</span></span> <span data-ttu-id="03284-110">Wenn Sie den Status $ \ket {1} $ aufweist, wird $Y $ angewendet.</span><span class="sxs-lookup"><span data-stu-id="03284-110">When it is in state $\ket{1}$, $Y$ is applied.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="03284-111">Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="03284-111">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="03284-112">Der Status $ \ket{p} $ dieses Registers bestimmt das Qubit, auf dem $X $ oder $Y $ angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="03284-112">The state $\ket{p}$ of this register determines the qubit on which $X$ or $Y$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="03284-113">targetregiester: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="03284-113">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="03284-114">Das Register der Qubits, auf die die Pauli-Operatoren angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="03284-114">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03284-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03284-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="03284-116">Referenzen</span><span class="sxs-lookup"><span data-stu-id="03284-116">References</span></span>

- <span data-ttu-id="03284-117">Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="03284-117">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>