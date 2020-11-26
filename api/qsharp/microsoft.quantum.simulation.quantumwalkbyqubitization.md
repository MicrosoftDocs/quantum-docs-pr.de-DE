---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: Quantenwalkbyqubitisierung-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ccef1bbf400e01800053777d0010acb7addaef53
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192484"
---
# <a name="quantumwalkbyqubitization-function"></a><span data-ttu-id="ec130-102">Quantenwalkbyqubitisierung-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec130-102">QuantumWalkByQubitization function</span></span>

<span data-ttu-id="ec130-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ec130-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ec130-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec130-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec130-105">Konvertiert eine Block Codierungs Reflektion in einen Quantum Walk.</span><span class="sxs-lookup"><span data-stu-id="ec130-105">Converts a block-encoding reflection into a quantum walk.</span></span>

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="ec130-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec130-106">Description</span></span>

<span data-ttu-id="ec130-107">Wenn ein `BlockEncodingReflection` von einem einheitlichen $U $ repräsentiert wird, der einen Operator $H $ of Interest codiert, konvertiert ihn in einen Quantum Walk $W $, der das Spektrum von $ \pm e ^ {\pm i\sin ^ {-1} (H)} $ enthält.</span><span class="sxs-lookup"><span data-stu-id="ec130-107">Given a `BlockEncodingReflection` represented by a unitary $U$ that encodes some operator $H$ of interest, converts it into a quantum walk $W$ containing the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="input"></a><span data-ttu-id="ec130-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ec130-108">Input</span></span>

### <a name="blockencoding--blockencodingreflection"></a><span data-ttu-id="ec130-109">blockencoding: [blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="ec130-109">blockEncoding : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="ec130-110">Ein `BlockEncodingReflection` einheitlicher $U $, der in einen Quantum Walk konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec130-110">A `BlockEncodingReflection` unitary $U$ to be converted into a Quantum walk.</span></span>



## <a name="output--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="ec130-111">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="ec130-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ec130-112">Ein Quantum Walk $W $, das sich zusammen in Registern verhält `a` und `s` $H $ codiert und das Spektrum von $ \pm e ^ {\pm i\sin ^ {-1} (H)} $ enthält.</span><span class="sxs-lookup"><span data-stu-id="ec130-112">A quantum walk $W$ acting jointly on registers `a` and `s` that block- encodes $H$, and contains the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="references"></a><span data-ttu-id="ec130-113">Referenzen</span><span class="sxs-lookup"><span data-stu-id="ec130-113">References</span></span>

- <span data-ttu-id="ec130-114">Hamiltona Simulation by qubitisierung Guang Hao Low, ISAL. Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="ec130-114">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="ec130-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec130-115">See Also</span></span>

- [<span data-ttu-id="ec130-116">Microsoft. Quantum. Simulation. blockencoding</span><span class="sxs-lookup"><span data-stu-id="ec130-116">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="ec130-117">Microsoft. Quantum. Simulation. blockencodingreflection</span><span class="sxs-lookup"><span data-stu-id="ec130-117">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)