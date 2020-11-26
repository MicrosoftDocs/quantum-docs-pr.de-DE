---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Arrangedqubits-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f3bc4dff73d5ad6393294fc3770b8d36e6094fb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217066"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="9d8bc-102">Arrangedqubits-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d8bc-102">ArrangedQubits function</span></span>

<span data-ttu-id="9d8bc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9d8bc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9d8bc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d8bc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d8bc-105">Anordnen von Steuerelement-, Ziel-und hilfsqubits gemäß einem Index</span><span class="sxs-lookup"><span data-stu-id="9d8bc-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="9d8bc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d8bc-106">Description</span></span>

<span data-ttu-id="9d8bc-107">Gibt ein Qubit-Array mit dem Ziel am Index 0 und Control i am Index 2 ^ i zurück.</span><span class="sxs-lookup"><span data-stu-id="9d8bc-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="9d8bc-108">Die hilfsqubits werden an alle anderen Positionen im Array eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9d8bc-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="9d8bc-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d8bc-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="9d8bc-110">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9d8bc-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="9d8bc-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9d8bc-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="9d8bc-112">Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9d8bc-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="9d8bc-113">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9d8bc-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

