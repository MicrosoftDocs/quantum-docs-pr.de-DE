---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Pauliblockencoding-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848004"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="0a1b7-102">Pauliblockencoding-Funktion</span><span class="sxs-lookup"><span data-stu-id="0a1b7-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="0a1b7-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="0a1b7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0a1b7-105">Erstellt eine einheitliche Block Codierung für ein hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="0a1b7-106">Die hamiltonan $H = \ sum_ {j} \ alpha_j P_j $ wird durch eine Summe von Pauli-Begriffen $P _J $, jeweils mit dem tatsächlichen Koeffizienten $ \ alpha_j $, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="0a1b7-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0a1b7-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="0a1b7-108">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="0a1b7-109">Eine `GeneratorSystem` , die $H $ als Summe von Pauli-Begriffen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="0a1b7-110">Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="0a1b7-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="0a1b7-111">Erster Parameter</span><span class="sxs-lookup"><span data-stu-id="0a1b7-111">First parameter</span></span>

<span data-ttu-id="0a1b7-112">Die einnorm der Koeffizienten $ \alpha = \ sum_ {j} | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="0a1b7-113">Zweiter Parameter</span><span class="sxs-lookup"><span data-stu-id="0a1b7-113">Second parameter</span></span>

<span data-ttu-id="0a1b7-114">Ein `BlockEncodingReflection` einheitlicher $U $ der hamiltonan $H $.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="0a1b7-115">Da diese einheitliche $U ^ 2 = I $ erfüllt, ist Sie auch eine Reflektion.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a1b7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a1b7-116">Remarks</span></span>

<span data-ttu-id="0a1b7-117">Dies wird erreicht, indem der Status $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ vorbereitet und die Vorbereitung wieder vorbereitet wird, und das Erstellen einer multiplizierten, einheitlichen <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> und- <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .</span><span class="sxs-lookup"><span data-stu-id="0a1b7-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>