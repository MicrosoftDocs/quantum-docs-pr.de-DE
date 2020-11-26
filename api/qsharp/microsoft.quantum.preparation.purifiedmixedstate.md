---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: Purifedmixedstate-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 73b031f1082d0a12975abad074b07184dcbabdbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230020"
---
# <a name="purifiedmixedstate-function"></a><span data-ttu-id="d5ef4-102">Purifedmixedstate-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5ef4-102">PurifiedMixedState function</span></span>

<span data-ttu-id="d5ef4-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d5ef4-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d5ef4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d5ef4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d5ef4-105">Gibt einen Vorgang zurück, der eine Reinigung eines gegebenen gemischten Zustands vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-105">Returns an operation that prepares a a purification of a given mixed state.</span></span>
<span data-ttu-id="d5ef4-106">Ein "gereinigter gemischter Zustand" bezieht sich auf Zustände in der Form | ψ ⟩ =. i. PI | i ⟩ | garbagei ⟩ angegeben durch einen Vektor von Koeffizienten {Pi}.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-106">A "purified mixed state" refers to states of the form |ψ⟩ = Σᵢ √𝑝ᵢ |𝑖⟩ |garbageᵢ⟩ specified by a vector of coefficients {𝑝ᵢ}.</span></span> <span data-ttu-id="d5ef4-107">Zustände dieses Formulars können auf gemischte Zustände reduziert werden p ≔ Pi | i ⟩ ⟨ i | durch die Ablauf Verfolgung über das "Garbage Register" (d. h. ein gemischter Zustand, der in der Berechnungsbasis diagonal ist).</span><span class="sxs-lookup"><span data-stu-id="d5ef4-107">States of this form can be reduced to mixed states ρ ≔ 𝑝ᵢ |𝑖⟩⟨𝑖| by tracing over the "garbage" register (that is, a mixed state that is diagonal in the computational basis).</span></span>

<span data-ttu-id="d5ef4-108">Weitere Erläuterungen finden Sie unter https://arxiv.org/pdf/1805.03662.pdf?page=15 .</span><span class="sxs-lookup"><span data-stu-id="d5ef4-108">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="d5ef4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5ef4-109">Description</span></span>

<span data-ttu-id="d5ef4-110">Verwendet die Quantum-Rom-Technik, um eine gegebene Dichte Matrix darzustellen, und gibt diese Darstellung als Zustands Vorbereitungs Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-110">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="d5ef4-111">Insbesondere, wenn eine Liste mit $N $ Koeffizienten $ \ alpha_j $, diese Funktion gibt einen Vorgang zurück, der die Quantum Rom-Technik verwendet, um eine Näherung von $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \ zu vorbereiten. End{align} $ $ des gemischten Zustands $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ Frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{align} $ $, wobei jeder $p _J $ eine Näherung zum gegebenen Koeffizienten $ \ alpha_j $ darstellt, sodass $ $ \begin{align} \left | p_j-\bruch{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ für jede $j $.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-111">In particular, given a list of $N$ coefficients $\alpha_j$, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="d5ef4-112">Wenn ein Indexregister und ein Register von Garbage Qubits, anfänglich im Status $ \ket {0} \ket{00\cdots 0}, übergeben werden, bereitet der zurückgegebene Vorgang beide Register bei der Bereinigung von $ \tilde \rho $ vor. $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{Garbage} _J}, \end{align} $ $, damit das Zurücksetzen und Aufheben der Zuordnung des Garbage Registers die gewünschte Vorbereitung innerhalb des Ziel Fehlers $ \epsilon $ aufsetzt.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-112">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="d5ef4-113">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5ef4-113">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="d5ef4-114">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d5ef4-114">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d5ef4-115">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-115">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="d5ef4-116">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d5ef4-116">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d5ef4-117">Ein Array von $N $ Koeffizienten, das die Wahrscheinlichkeit von Basis Zuständen angibt.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-117">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="d5ef4-118">Negative Zahlen $-\ alpha_j $ werden als positiv $ | \ alpha_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-118">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="d5ef4-119">Ausgabe: [mixedstatepreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="d5ef4-119">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="d5ef4-120">Ein Vorgang, bei dem $ \tilde \rho $ als Bereinigung auf einen gemeinsamen Index und ein Garbage Register vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-120">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ef4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5ef4-121">Remarks</span></span>

<span data-ttu-id="d5ef4-122">Die Koeffizienten, die für diesen Vorgang bereitgestellt werden, werden nach der Norm 1 normalisiert, sodass die Koeffizienten immer als eine gültige kategorische Wahrscheinlichkeitsverteilung bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-122">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="d5ef4-123">Referenzen</span><span class="sxs-lookup"><span data-stu-id="d5ef4-123">References</span></span>

- <span data-ttu-id="d5ef4-124">Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="d5ef4-124">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="d5ef4-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5ef4-125">See Also</span></span>

- [<span data-ttu-id="d5ef4-126">Microsoft. Quantum. Preparation. purienedmixedstatewithdata</span><span class="sxs-lookup"><span data-stu-id="d5ef4-126">Microsoft.Quantum.Preparation.PurifiedMixedStateWithData</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)