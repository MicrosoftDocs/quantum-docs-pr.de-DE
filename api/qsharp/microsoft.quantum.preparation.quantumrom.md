---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Quantenrom-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 8ba5c6fab4abcfaee7233df9535f22eea5f68c28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722961"
---
# <a name="quantumrom-function"></a><span data-ttu-id="540b6-102">Quantenrom-Funktion</span><span class="sxs-lookup"><span data-stu-id="540b6-102">QuantumROM function</span></span>

<span data-ttu-id="540b6-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="540b6-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="540b6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="540b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="540b6-105">Verwendet die Quantum-Rom-Technik, um eine angegebene Dichte Matrix darzustellen.</span><span class="sxs-lookup"><span data-stu-id="540b6-105">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="540b6-106">Eine Liste mit $N $ Koeffizienten $ \ alpha_j $, dadurch wird ein einheitlicher $U $ zurückgegeben, der die Quantum-Rom-Technik verwendet, um eine Näherung von $ \tilde \rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ der Reinigung der Dichte Matrix $ \rho = \ sum_ {j = 0} ^ {n-1} \bruchteil {| alpha_j |} zu erstellen. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $.</span><span class="sxs-lookup"><span data-stu-id="540b6-106">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="540b6-107">In dieser Näherung ist der Fehler $ \epsilon $, dass $ | p_j-\bruch{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ und $ \| \tilde \rho-\rho \| \le \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="540b6-107">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="540b6-108">Anders ausgedrückt: $ $ \begin{align} u\ket {0} ^ {\lceil\ Log_2 n\rceil} \ Ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{Garbage} _J}.</span><span class="sxs-lookup"><span data-stu-id="540b6-108">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="540b6-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="540b6-109">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="540b6-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="540b6-110">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="540b6-111">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="540b6-111">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="540b6-112">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="540b6-112">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="540b6-113">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="540b6-113">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="540b6-114">Ein Array von $N $ Koeffizienten, das die Wahrscheinlichkeit von Basis Zuständen angibt.</span><span class="sxs-lookup"><span data-stu-id="540b6-114">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="540b6-115">Negative Zahlen $-\ alpha_j $ werden als positiv $ | \ alpha_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="540b6-115">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit-adj--ctl"></a><span data-ttu-id="540b6-116">Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[, int,](xref:microsoft.quantum.lang-ref.int)[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="540b6-116">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="540b6-117">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="540b6-117">First parameter</span></span>

<span data-ttu-id="540b6-118">Ein Tupel `(x,(y,z))` , bei dem `x = y + z` die Gesamtzahl der zugeordneten Qubits ist, `y` die Anzahl der Qubits für das `LittleEndian` Register und `z` die Anzahl der Garbage Qubits.</span><span class="sxs-lookup"><span data-stu-id="540b6-118">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="540b6-119">Zweiter Parameter</span><span class="sxs-lookup"><span data-stu-id="540b6-119">Second parameter</span></span>

<span data-ttu-id="540b6-120">Die einnorm $ \ sum_j | \ alpha_j | $ des Koeffizienten-Arrays.</span><span class="sxs-lookup"><span data-stu-id="540b6-120">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="540b6-121">Dritter Parameter</span><span class="sxs-lookup"><span data-stu-id="540b6-121">Third parameter</span></span>

<span data-ttu-id="540b6-122">Der einheitliche $U $.</span><span class="sxs-lookup"><span data-stu-id="540b6-122">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="540b6-123">Referenzen</span><span class="sxs-lookup"><span data-stu-id="540b6-123">References</span></span>

- <span data-ttu-id="540b6-124">Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="540b6-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>