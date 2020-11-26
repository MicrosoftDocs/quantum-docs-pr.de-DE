---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Applymultiplycontrolledlowdepthand-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 1aeab429bd6304c621e0d5225b43a76eab607c84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209195"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a><span data-ttu-id="998bc-102">Applymultiplycontrolledlowdepthand-Vorgang</span><span class="sxs-lookup"><span data-stu-id="998bc-102">ApplyMultiplyControlledLowDepthAnd operation</span></span>

<span data-ttu-id="998bc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="998bc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="998bc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="998bc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="998bc-105">Implementiert ein mehrfach kontrolliertes "deffoli"-Gate, wobei angenommen wird, dass das Ziel-Qubit initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="998bc-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="998bc-106">Der Adjoint-Vorgang geht davon aus, dass das Ziel-Qubit auf 0 zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="998bc-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>  <span data-ttu-id="998bc-107">Erfordert eine RZ-Tiefe von 1, während die Anzahl von hilfsqubits in der Anzahl der Qubits exponentiell ist.</span><span class="sxs-lookup"><span data-stu-id="998bc-107">Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.</span></span>

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="998bc-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="998bc-108">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="998bc-109">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="998bc-109">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="998bc-110">Steuerelement-Qubits</span><span class="sxs-lookup"><span data-stu-id="998bc-110">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="998bc-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="998bc-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="998bc-112">Ziel-Qubit</span><span class="sxs-lookup"><span data-stu-id="998bc-112">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="998bc-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="998bc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

