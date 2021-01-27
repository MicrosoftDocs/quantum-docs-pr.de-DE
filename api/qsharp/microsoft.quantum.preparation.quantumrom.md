---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Quantenrom-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 64ed9aed7c9d9a4a689c5926f3cd085a2521c4db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856822"
---
# <a name="quantumrom-function"></a><span data-ttu-id="8fa1f-102">Quantenrom-Funktion</span><span class="sxs-lookup"><span data-stu-id="8fa1f-102">QuantumROM function</span></span>

<span data-ttu-id="8fa1f-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="8fa1f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="8fa1f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fa1f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="8fa1f-105">Quantum Rom ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-105">QuantumROM has been deprecated.</span></span> <span data-ttu-id="8fa1f-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PurifiedMixedState>.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.</span></span>

<span data-ttu-id="8fa1f-107">Verwendet die Quantum-Rom-Technik, um eine angegebene Dichte Matrix darzustellen.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-107">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="8fa1f-108">Eine Liste mit $N $ Koeffizienten $ \ alpha_j $, dadurch wird ein einheitlicher $U $ zurückgegeben, der die Quantum-Rom-Technik verwendet, um eine Näherung von $ \tilde \rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ der Reinigung der Dichte Matrix $ \rho = \ sum_ {j = 0} ^ {n-1} \bruchteil {| alpha_j |} zu erstellen. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-108">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="8fa1f-109">In dieser Näherung ist der Fehler $ \epsilon $, dass $ | p_j-\bruch{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ und $ \| \tilde \rho-\rho \| \le \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-109">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="8fa1f-110">Anders ausgedrückt: $ $ \begin{align} u\ket {0} ^ {\lceil\ Log_2 n\rceil} \ Ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{Garbage} _J}.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-110">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="8fa1f-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="8fa1f-111">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="8fa1f-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fa1f-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="8fa1f-113">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8fa1f-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8fa1f-114">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="8fa1f-115">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8fa1f-115">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8fa1f-116">Ein Array von $N $ Koeffizienten, das die Wahrscheinlichkeit von Basis Zuständen angibt.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-116">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="8fa1f-117">Negative Zahlen $-\ alpha_j $ werden als positiv $ | \ alpha_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="8fa1f-118">Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[, int,](xref:microsoft.quantum.lang-ref.int)[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit) ist ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="8fa1f-118">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="8fa1f-119">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa1f-119">First parameter</span></span>

<span data-ttu-id="8fa1f-120">Ein Tupel `(x,(y,z))` , bei dem `x = y + z` die Gesamtzahl der zugeordneten Qubits ist, `y` die Anzahl der Qubits für das `LittleEndian` Register und `z` die Anzahl der Garbage Qubits.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-120">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="8fa1f-121">Zweiter Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa1f-121">Second parameter</span></span>

<span data-ttu-id="8fa1f-122">Die einnorm $ \ sum_j | \ alpha_j | $ des Koeffizienten-Arrays.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-122">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="8fa1f-123">Dritter Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa1f-123">Third parameter</span></span>

<span data-ttu-id="8fa1f-124">Der einheitliche $U $.</span><span class="sxs-lookup"><span data-stu-id="8fa1f-124">The unitary $U$.</span></span>

## <a name="example"></a><span data-ttu-id="8fa1f-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fa1f-125">Example</span></span>

<span data-ttu-id="8fa1f-126">Der folgende Code Ausschnitt bereitet eine Reinigung des $3 $-Qubit-Zustands $ \rho = \ sum_ {j = 0} ^ {4} \bruchteil {| alpha_j |} vor. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $, wobei $ \vec\alpha = (1.0, 2.0, 3.0, 4.0, 5.0) $ und der Fehler lautet `1e-3` .</span><span class="sxs-lookup"><span data-stu-id="8fa1f-126">The following code snippet prepares an purification of the $3$-qubit state $\rho=\sum_{j=0}^{4}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$, where $\vec\alpha=(1.0,2.0,3.0,4.0,5.0)$, and the error is `1e-3`;</span></span>

```qsharp
let coefficients = [1.0,2.0,3.0,4.0,5.0];
let targetError = 1e-3;
let ((nTotalQubits, (nIndexQubits, nGarbageQubits)), oneNorm, op) = QuantumROM(targetError, coefficients);
using (indexRegister = Qubit[nIndexQubits]) {
    using (garbageRegister = Qubit[nGarbageQubits]) {
        op(LittleEndian(indexRegister), garbageRegister);
    }
}
```

## <a name="references"></a><span data-ttu-id="8fa1f-127">References</span><span class="sxs-lookup"><span data-stu-id="8fa1f-127">References</span></span>

- <span data-ttu-id="8fa1f-128">Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="8fa1f-128">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>