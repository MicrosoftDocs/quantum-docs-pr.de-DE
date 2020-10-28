---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Pauliblockencoding-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 1426c7cbc257f9263ff45a96738fe798c3679ba1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706674"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="33115-102">Pauliblockencoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="33115-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="33115-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="33115-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="33115-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33115-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33115-105">Erstellt eine einheitliche Block Codierung für ein hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="33115-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="33115-106">Die hamiltonan $H = \ sum_ {j} \ alpha_j P_j $ wird durch eine Summe von Pauli-Begriffen $P _J $, jeweils mit dem tatsächlichen Koeffizienten $ \ alpha_j $, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="33115-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="33115-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="33115-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="33115-108">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="33115-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="33115-109">Eine `GeneratorSystem` , die $H $ als Summe von Pauli-Begriffen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="33115-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="33115-110">Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="33115-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="33115-111">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="33115-111">First parameter</span></span>

<span data-ttu-id="33115-112">Die einnorm der Koeffizienten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="33115-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="33115-113">Zweiter Parameter</span><span class="sxs-lookup"><span data-stu-id="33115-113">Second parameter</span></span>

<span data-ttu-id="33115-114">Ein `BlockEncodingReflection` einheitlicher $U $ der hamiltonan $H $.</span><span class="sxs-lookup"><span data-stu-id="33115-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="33115-115">Da diese einheitliche $U ^ 2 = I $ erfüllt, ist Sie auch eine Reflektion.</span><span class="sxs-lookup"><span data-stu-id="33115-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="33115-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="33115-116">Remarks</span></span>

<span data-ttu-id="33115-117">Dies wird erreicht, indem der Status $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ vorbereitet und die Vorbereitung wieder vorbereitet wird, und das Erstellen einer multiplizierten, einheitlichen <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> und- <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="33115-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>