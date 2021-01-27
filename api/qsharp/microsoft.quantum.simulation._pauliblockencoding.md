---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: _PauliBlockEncoding-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: c27ef1a6b7cd7c84defe2a783e9fb1610e52d1e7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851064"
---
# <a name="_pauliblockencoding-function"></a><span data-ttu-id="8e586-102">_PauliBlockEncoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="8e586-102">_PauliBlockEncoding function</span></span>

<span data-ttu-id="8e586-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8e586-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8e586-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e586-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e586-105">Erstellt eine einheitliche Block Codierung für ein hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="8e586-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="8e586-106">Die hamiltonan $H = \ sum_ {j} \ alpha_j P_j $ wird durch eine Summe von Pauli-Begriffen $P _J $, jeweils mit dem tatsächlichen Koeffizienten $ \ alpha_j $, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8e586-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="8e586-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8e586-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="8e586-108">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="8e586-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="8e586-109">Eine `GeneratorSystem` , die $H $ als Summe von Pauli-Begriffen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8e586-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a><span data-ttu-id="8e586-110">stateprepeinheitlicher: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [littleeindian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8e586-110">statePrepUnitary : [Double](xref:microsoft.quantum.lang-ref.double)[] -> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8e586-111">Ein einheitlicher Vorgang $V $, der die einheitliche $V _J $ gesteuert für Index $ \ket{j} $ anwendet, wenn eine Funktion $f: j\rightarrow V_j $.</span><span class="sxs-lookup"><span data-stu-id="8e586-111">A unitary operation $V$ that applies the unitary $V_j$ controlled on index $\ket{j}$, given a function $f: j\rightarrow V_j$.</span></span>


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="8e586-112">Multiplexer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL)-> ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8e586-112">multiplexer : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl) -> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>





## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="8e586-113">Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="8e586-113">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="8e586-114">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="8e586-114">First parameter</span></span>

<span data-ttu-id="8e586-115">Die einnorm der Koeffizienten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="8e586-115">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="8e586-116">Zweiter Parameter</span><span class="sxs-lookup"><span data-stu-id="8e586-116">Second parameter</span></span>

<span data-ttu-id="8e586-117">Ein `BlockEncodingReflection` einheitlicher $U $ der hamiltonan $U $.</span><span class="sxs-lookup"><span data-stu-id="8e586-117">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $U$.</span></span> <span data-ttu-id="8e586-118">Da diese einheitliche $U ^ 2 = I $ erfüllt, ist Sie auch eine Reflektion.</span><span class="sxs-lookup"><span data-stu-id="8e586-118">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e586-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e586-119">Remarks</span></span>

<span data-ttu-id="8e586-120">Beispiel Vorgänge für die Vorbereitung und Aufhebung der Vorbereitung des Zustands $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ und das Erstellen einer Multiplikations kontrollierten einheitlich sind <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> und <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="8e586-120">Example operations the prepare and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and construct a multiply-controlled unitary are <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>