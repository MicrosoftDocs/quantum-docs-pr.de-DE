---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: ApplyDelta-Parität (Vorgang)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: bb01eb684ff1820be08a573c0ca6cfc12efeb889
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723983"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="822e6-102">ApplyDelta-Parität (Vorgang)</span><span class="sxs-lookup"><span data-stu-id="822e6-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="822e6-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="822e6-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="822e6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="822e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="822e6-105">Berechnet den Unterschied in der Parität zwischen einem vorherigen pqrs... Begriffe und die nächsten pqrs... zeitig.</span><span class="sxs-lookup"><span data-stu-id="822e6-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="822e6-106">Dieser Unterschied wird für ein zusätzliches Qubit berechnet.</span><span class="sxs-lookup"><span data-stu-id="822e6-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="822e6-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="822e6-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="822e6-108">prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="822e6-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="822e6-109">Liste der Indizes für vorherige pqrs... Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="822e6-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="822e6-110">nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="822e6-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="822e6-111">Liste der Indizes für die nächsten pqrs... Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="822e6-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="822e6-112">AUX: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="822e6-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="822e6-113">Ein zusätzliches Qubit, auf das die Ergebnisse der Paritäts Berechnung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="822e6-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="822e6-114">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="822e6-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="822e6-115">Qubit wurde von allen pqrs bearbeitet... Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="822e6-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="822e6-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="822e6-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="822e6-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="822e6-117">Remarks</span></span>

<span data-ttu-id="822e6-118">Dabei wird davon ausgegangen, dass die Indizes von P < Q < R < S <... für prevpq und nextpq.</span><span class="sxs-lookup"><span data-stu-id="822e6-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>