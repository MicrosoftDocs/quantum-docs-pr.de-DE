---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Logicalandmeasandfix-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704031"
---
# <a name="logicalandmeasandfix-operation"></a><span data-ttu-id="0883f-102">Logicalandmeasandfix-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0883f-102">LogicalANDMeasAndFix operation</span></span>

<span data-ttu-id="0883f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0883f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0883f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0883f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0883f-105">Berechnet das logische and von mehreren Qubits.</span><span class="sxs-lookup"><span data-stu-id="0883f-105">Computes the logical AND of multiple qubits.</span></span>

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0883f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0883f-106">Input</span></span>

### <a name="ctrlregister--qubit"></a><span data-ttu-id="0883f-107">ctrlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0883f-107">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0883f-108">Qubits-Eingabe für die mehrfach Eingabe und das Gate.</span><span class="sxs-lookup"><span data-stu-id="0883f-108">Qubits input to the multiple-input AND gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="0883f-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0883f-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0883f-110">Ein Qubit, in dem die Ausgabe von und geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="0883f-110">Qubit on which output of AND is written to.</span></span> <span data-ttu-id="0883f-111">Dabei wird davon ausgegangen, dass Sie immer im Zustand "$ \ket $" gestartet werden {0} .</span><span class="sxs-lookup"><span data-stu-id="0883f-111">This is assumed to always start in the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0883f-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0883f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0883f-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0883f-113">Remarks</span></span>

<span data-ttu-id="0883f-114">Wenn `ctrlRegister` genau $2 $ Qubits hat, entspricht dies dem Vorgang, `CCNOT` aber Phase mit einer Phase $e ^ {i \ Pi/2} $ auf $ \ket {001} $ und $-e ^ {i \ Pi/2} $ auf $ \ket {101} $ und $ \ket {011} $.</span><span class="sxs-lookup"><span data-stu-id="0883f-114">When `ctrlRegister` has exactly $2$ qubits, this is equivalent to the `CCNOT` operation but phase with a phase $e^{i\Pi/2}$ on $\ket{001}$ and $-e^{i\Pi/2}$ on $\ket{101}$ and $\ket{011}$.</span></span>
<span data-ttu-id="0883f-115">Das Adjoint-Verfahren ist auch ein Measure-und Fixup-Ansatz, bei dem es sich nur um die Umkehrung des ursprünglichen Vorgangs handelt (siehe Verweise), aber weniger T-Gates verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0883f-115">The Adjoint is also measure-and-fixup approach that is the inverse of the original operation only in special cases (see references), but uses fewer T-gates.</span></span>

## <a name="references"></a><span data-ttu-id="0883f-116">Referenzen</span><span class="sxs-lookup"><span data-stu-id="0883f-116">References</span></span>

- [<span data-ttu-id="0883f-117">*Craig Gidney* , 1709,06648</span><span class="sxs-lookup"><span data-stu-id="0883f-117"> *Craig Gidney* , 1709.06648</span></span>](https://arxiv.org/abs/1709.06648)