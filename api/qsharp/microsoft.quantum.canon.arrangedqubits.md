---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Arrangedqubits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704498"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="80184-102">Arrangedqubits-Funktion</span><span class="sxs-lookup"><span data-stu-id="80184-102">ArrangedQubits function</span></span>

<span data-ttu-id="80184-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="80184-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="80184-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80184-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80184-105">Anordnen von Steuerelement-, Ziel-und hilfsqubits gemäß einem Index</span><span class="sxs-lookup"><span data-stu-id="80184-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="80184-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80184-106">Description</span></span>

<span data-ttu-id="80184-107">Gibt ein Qubit-Array mit dem Ziel am Index 0 und Control i am Index 2 ^ i zurück.</span><span class="sxs-lookup"><span data-stu-id="80184-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="80184-108">Die hilfsqubits werden an alle anderen Positionen im Array eingefügt.</span><span class="sxs-lookup"><span data-stu-id="80184-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="80184-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80184-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="80184-110">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="80184-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="80184-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="80184-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="80184-112">Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="80184-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="80184-113">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="80184-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

