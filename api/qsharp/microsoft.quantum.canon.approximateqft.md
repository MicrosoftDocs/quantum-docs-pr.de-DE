---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Näherer Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 31fd87c0f61292142c7493cc29cad1082a9a2d67
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850323"
---
# <a name="approximateqft-operation"></a><span data-ttu-id="42a86-102">Näherer Vorgang</span><span class="sxs-lookup"><span data-stu-id="42a86-102">ApproximateQFT operation</span></span>

<span data-ttu-id="42a86-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="42a86-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="42a86-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42a86-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42a86-105">Wenden Sie die ungefähre quantfourier Transform (aqft) auf ein Quantum-Register an.</span><span class="sxs-lookup"><span data-stu-id="42a86-105">Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.</span></span>

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="42a86-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42a86-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="42a86-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42a86-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42a86-108">Näherungs Parameter, der bestimmt, auf welcher Ebene die kontrollierten Z-Drehungen in der QFT-Verbindung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="42a86-108">approximation parameter which determines at which level the controlled Z-rotations that occur in the QFT circuit are pruned.</span></span>

<span data-ttu-id="42a86-109">Der Näherungs Parameter a bestimmt die Bereinigungs Ebene der Z-Drehungen, d. h. a ∈ {0.. n} und alle Z-Drehungen 2D/2K, wobei k>a aus der QFT-Leitung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="42a86-109">The approximation parameter a determines the pruning level of the Z-rotations, i.e., a ∈ {0..n} and all Z-rotations 2π/2ᵏ where k>a are removed from the QFT circuit.</span></span> <span data-ttu-id="42a86-110">Es ist bekannt, dass für k >= Protokoll. (n) + Protokoll Taste (1/1) + 3 eine Grenze gebunden werden kann | | QFT-aqft | |<.</span><span class="sxs-lookup"><span data-stu-id="42a86-110">It is known that for k >= log₂(n)+log₂(1/ε)+3 one can bound ||QFT-AQFT||<ε.</span></span>


### <a name="qs--bigendian"></a><span data-ttu-id="42a86-111">QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="42a86-111">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="42a86-112">das Quantum-Register von n Qubits, auf das die ungefähre Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="42a86-112">quantum register of n qubits to which the Approximate Quantum Fourier Transform is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="42a86-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42a86-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="42a86-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a86-114">Remarks</span></span>

<span data-ttu-id="42a86-115">Für aqft sind Z-Drehung-Gates im Format 2D/2K und Hadamard Gates erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42a86-115">AQFT requires Z-rotation gates of the form 2π/2ᵏ and Hadamard gates.</span></span>

<span data-ttu-id="42a86-116">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung codiert werden.</span><span class="sxs-lookup"><span data-stu-id="42a86-116">The input and output are assumed to be encoded in big endian encoding.</span></span>

## <a name="references"></a><span data-ttu-id="42a86-117">References</span><span class="sxs-lookup"><span data-stu-id="42a86-117">References</span></span>

- [<span data-ttu-id="42a86-118">*M. roetteler, Th. Beth*, Appl. Algebra eng. Commun. Co. 19 (3): 177-193 (2008)</span><span class="sxs-lookup"><span data-stu-id="42a86-118"> *M. Roetteler, Th. Beth*, Appl. Algebra Eng. Commun. Comput. 19(3): 177-193 (2008) </span></span>](http://doi.org/10.1007/s00200-008-0072-2)
- [<span data-ttu-id="42a86-119">*D. kopierungsarxiv* : quant-ph/0201067v1</span><span class="sxs-lookup"><span data-stu-id="42a86-119"> *D. Coppersmith* arXiv:quant-ph/0201067v1 </span></span>](https://arxiv.org/abs/quant-ph/0201067)