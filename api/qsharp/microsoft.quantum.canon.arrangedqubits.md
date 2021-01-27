---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Arrangedqubits-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841079"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="59619-102">Arrangedqubits-Funktion</span><span class="sxs-lookup"><span data-stu-id="59619-102">ArrangedQubits function</span></span>

<span data-ttu-id="59619-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="59619-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="59619-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59619-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59619-105">Anordnen von Steuerelement-, Ziel-und hilfsqubits gemäß einem Index</span><span class="sxs-lookup"><span data-stu-id="59619-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="59619-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59619-106">Description</span></span>

<span data-ttu-id="59619-107">Gibt ein Qubit-Array mit dem Ziel am Index 0 und Control i am Index 2 ^ i zurück.</span><span class="sxs-lookup"><span data-stu-id="59619-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="59619-108">Die hilfsqubits werden an alle anderen Positionen im Array eingefügt.</span><span class="sxs-lookup"><span data-stu-id="59619-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="59619-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59619-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="59619-110">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="59619-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="59619-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="59619-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="59619-112">Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="59619-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="59619-113">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="59619-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

