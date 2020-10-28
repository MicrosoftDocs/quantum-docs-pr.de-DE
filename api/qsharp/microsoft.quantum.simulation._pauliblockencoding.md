---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: _PauliBlockEncoding-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: ba30a7e87bd970961dc87f048aa586ff5c512e2a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701765"
---
# <a name="_pauliblockencoding-function"></a><span data-ttu-id="aaa71-102">_PauliBlockEncoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="aaa71-102">_PauliBlockEncoding function</span></span>

<span data-ttu-id="aaa71-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="aaa71-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="aaa71-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aaa71-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aaa71-105">Erstellt eine einheitliche Block Codierung für ein hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="aaa71-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="aaa71-106">Die hamiltonan $H = \ sum_ {j} \ alpha_j P_j $ wird durch eine Summe von Pauli-Begriffen $P _J $, jeweils mit dem tatsächlichen Koeffizienten $ \ alpha_j $, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aaa71-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="aaa71-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aaa71-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="aaa71-108">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="aaa71-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="aaa71-109">Eine `GeneratorSystem` , die $H $ als Summe von Pauli-Begriffen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="aaa71-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>


### <a name="stateprepunitary--double---littleendian--unit-adj--ctl"></a><span data-ttu-id="aaa71-110">stateprepeinheitlicher: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [littleeindian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="aaa71-110">statePrepUnitary : [Double](xref:microsoft.quantum.lang-ref.double)[] -> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="aaa71-111">Ein einheitlicher Vorgang $V $, der die einheitliche $V _J $ gesteuert für Index $ \ket{j} $ anwendet, wenn eine Funktion $f: j\rightarrow V_j $.</span><span class="sxs-lookup"><span data-stu-id="aaa71-111">A unitary operation $V$ that applies the unitary $V_j$ controlled on index $\ket{j}$, given a function $f: j\rightarrow V_j$.</span></span>


### <a name="multiplexer--intint---qubit--unit-adj--ctl---littleendianqubit--unit-adj--ctl"></a><span data-ttu-id="aaa71-112">Multiplexer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)-> ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="aaa71-112">multiplexer : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl) -> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>





## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="aaa71-113">Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="aaa71-113">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="aaa71-114">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="aaa71-114">First parameter</span></span>

<span data-ttu-id="aaa71-115">Die einnorm der Koeffizienten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="aaa71-115">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="aaa71-116">Zweiter Parameter</span><span class="sxs-lookup"><span data-stu-id="aaa71-116">Second parameter</span></span>

<span data-ttu-id="aaa71-117">Ein `BlockEncodingReflection` einheitlicher $U $ der hamiltonan $U $.</span><span class="sxs-lookup"><span data-stu-id="aaa71-117">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $U$.</span></span> <span data-ttu-id="aaa71-118">Da diese einheitliche $U ^ 2 = I $ erfüllt, ist Sie auch eine Reflektion.</span><span class="sxs-lookup"><span data-stu-id="aaa71-118">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa71-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aaa71-119">Remarks</span></span>

<span data-ttu-id="aaa71-120">Beispiel Vorgänge für die Vorbereitung und Aufhebung der Vorbereitung des Zustands $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ und das Erstellen einer Multiplikations kontrollierten einheitlich sind <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> und <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="aaa71-120">Example operations the prepare and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and construct a multiply-controlled unitary are <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>