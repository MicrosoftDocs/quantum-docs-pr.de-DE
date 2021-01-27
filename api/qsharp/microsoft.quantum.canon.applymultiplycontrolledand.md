---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledAnd
title: Applymultiplycontrolledand-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.
ms.openlocfilehash: ac3972287d55ed2df85e1d88510918cc5202c711
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844845"
---
# <a name="applymultiplycontrolledand-operation"></a><span data-ttu-id="b138f-102">Applymultiplycontrolledand-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b138f-102">ApplyMultiplyControlledAnd operation</span></span>

<span data-ttu-id="b138f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b138f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b138f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b138f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b138f-105">Implementiert ein mehrfach kontrolliertes "deffoli"-Gate, wobei angenommen wird, dass das Ziel-Qubit initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b138f-105">Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.</span></span>  <span data-ttu-id="b138f-106">Der Adjoint-Vorgang geht davon aus, dass das Ziel-Qubit auf 0 zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b138f-106">The adjoint operation assumes that the target qubit will be reset to 0.</span></span>

```qsharp
operation ApplyMultiplyControlledAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="b138f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b138f-107">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="b138f-108">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b138f-108">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b138f-109">Steuerelement-Qubits</span><span class="sxs-lookup"><span data-stu-id="b138f-109">Control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b138f-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b138f-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b138f-111">Ziel-Qubit</span><span class="sxs-lookup"><span data-stu-id="b138f-111">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="b138f-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b138f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

