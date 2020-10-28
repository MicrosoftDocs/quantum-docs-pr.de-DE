---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Applymultiplycontrolledand-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: feca28d394e4af31eb4ffe737111d00ede45e27e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705191"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="96da5-102">Applymultiplycontrolledand-Vorgang</span><span class="sxs-lookup"><span data-stu-id="96da5-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="96da5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="96da5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="96da5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="96da5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="96da5-105">Implementiert ein mehrfach kontrolliertes "deffoli"-Gate, wobei angenommen wird, dass das Ziel-Qubit initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="96da5-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="96da5-106">Der Adjoint-Vorgang geht davon aus, dass das Ziel-Qubit auf 0 zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="96da5-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="96da5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="96da5-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="96da5-108">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="96da5-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="96da5-109">Steuerelement-Qubits</span><span class="sxs-lookup"><span data-stu-id="96da5-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="96da5-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="96da5-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="96da5-111">Ziel-Qubit</span><span class="sxs-lookup"><span data-stu-id="96da5-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="96da5-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="96da5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

