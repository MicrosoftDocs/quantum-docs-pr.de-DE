---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: Applyandchain-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: c53bca6ecf964f4358b0a7ff1c61d4e8e195cd7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219361"
---
# <a name="applyandchain-operation"></a><span data-ttu-id="d6a36-102">Applyandchain-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6a36-102">ApplyAndChain operation</span></span>

<span data-ttu-id="d6a36-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d6a36-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d6a36-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6a36-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6a36-105">Berechnet eine Kette von und Gates</span><span class="sxs-lookup"><span data-stu-id="d6a36-105">Computes a chain of AND gates</span></span>

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="d6a36-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6a36-106">Description</span></span>

<span data-ttu-id="d6a36-107">Die zusätzlichen Qubits zum Berechnen temporärer Ergebnisse müssen explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6a36-107">The auxiliary qubits to compute temporary results must be specified explicitly.</span></span>
<span data-ttu-id="d6a36-108">Die Länge dieses Registers ist `Length(ctrlRegister) - 2` , wenn mindestens zwei Steuerelemente vorhanden sind, andernfalls ist die Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d6a36-108">The length of that register is `Length(ctrlRegister) - 2`, if there are at least two controls, otherwise the length is 0.</span></span>

## <a name="input"></a><span data-ttu-id="d6a36-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d6a36-109">Input</span></span>

### <a name="auxregister--qubit"></a><span data-ttu-id="d6a36-110">"auxregister": [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d6a36-110">auxRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="ctrlregister--qubit"></a><span data-ttu-id="d6a36-111">ctrlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d6a36-111">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="d6a36-112">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d6a36-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="d6a36-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d6a36-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

