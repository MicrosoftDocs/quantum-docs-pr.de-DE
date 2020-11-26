---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Knilldinoch-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: df00c7572d909a67ec658bc8dccaf0e338afe5c5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200746"
---
# <a name="knilldistill-operation"></a><span data-ttu-id="92739-102">Knilldinoch-Vorgang</span><span class="sxs-lookup"><span data-stu-id="92739-102">KnillDistill operation</span></span>

<span data-ttu-id="92739-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="92739-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="92739-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92739-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92739-105">Implementiert den Knill Magic State-Destillations Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="92739-105">Implements the Knill magic state distillation algorithm.</span></span>

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a><span data-ttu-id="92739-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92739-106">Description</span></span>

<span data-ttu-id="92739-107">Bei 15 ungefähren Kopien eines Magic State $ $ \begin{align} \cos\bruchteil {\pi} {8} \ket {0} + \sin \bruchteil {\pi} {8} \ket {1} \end{align} ergibt $ $ eine Kopie einer höheren Qualität.</span><span class="sxs-lookup"><span data-stu-id="92739-107">Given 15 approximate copies of a magic state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1} \end{align}, $$ yields one higher-quality copy.</span></span>

## <a name="input"></a><span data-ttu-id="92739-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="92739-108">Input</span></span>

### <a name="roughmagic--qubit"></a><span data-ttu-id="92739-109">roughmagic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="92739-109">roughMagic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="92739-110">Ein Register von 15 Qubits, das ungefähre Kopien eines magischen Zustands enthält.</span><span class="sxs-lookup"><span data-stu-id="92739-110">A register of fifteen qubits containing approximate copies of a magic state.</span></span> <span data-ttu-id="92739-111">Die folgende Anwendung dieses Destillations Verfahrens `roughMagic[0]` enthält eine Kopie der höheren Qualität, und der Rest des Registers wird auf den Status $ \ket{00\cdots 0} $ zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="92739-111">Following application of this distillation procedure, `roughMagic[0]` will contain one higher-quality copy, and the rest of the register will be reset to the $\ket{00\cdots 0}$ state.</span></span>



## <a name="output--bool"></a><span data-ttu-id="92739-112">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="92739-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="92739-113">Wenn `true` , dann wird die Prozedur erfolgreich ausgeführt, und die Kopie der höheren Qualität sollte akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="92739-113">If `true`, then the procedure succeeded and the higher-quality copy should be accepted.</span></span> <span data-ttu-id="92739-114">Gibt an, `false` dass die Prozedur fehlgeschlagen ist und der Status des Registers als nicht definiert angesehen werden soll.</span><span class="sxs-lookup"><span data-stu-id="92739-114">If `false`, the procedure failed, and the state of the register should be considered undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="92739-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92739-115">Remarks</span></span>

<span data-ttu-id="92739-116">Wir folgen dem Algorithmus von "Knill".</span><span class="sxs-lookup"><span data-stu-id="92739-116">We follow the algorithm of Knill.</span></span>
<span data-ttu-id="92739-117">Allerdings ist die aktuelle Implementierung von weitem nicht optimal, da zu viele Qubits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92739-117">However, the present implementation is far from being optimal, as it uses too many qubits.</span></span>
<span data-ttu-id="92739-118">Die magischen Zustände werden in diese Routine eingefügt. in diesem Fall gibt es bessere Protokolle.</span><span class="sxs-lookup"><span data-stu-id="92739-118">The magic states are injected in this routine, in which case there are better protocols.</span></span>

## <a name="references"></a><span data-ttu-id="92739-119">Referenzen</span><span class="sxs-lookup"><span data-stu-id="92739-119">References</span></span>

- [<span data-ttu-id="92739-120">Knill</span><span class="sxs-lookup"><span data-stu-id="92739-120">Knill</span></span>](https://arxiv.org/abs/quant-ph/0402171)