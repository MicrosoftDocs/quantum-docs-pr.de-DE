---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: ApplyDelta-Parität (Vorgang)
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: f5f1d74274994f042f1bc3f2e0d5332f504be02c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851108"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="80402-102">ApplyDelta-Parität (Vorgang)</span><span class="sxs-lookup"><span data-stu-id="80402-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="80402-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="80402-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="80402-104">Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="80402-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="80402-105">Berechnet den Unterschied in der Parität zwischen einem vorherigen pqrs... Begriffe und die nächsten pqrs... zeitig.</span><span class="sxs-lookup"><span data-stu-id="80402-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="80402-106">Dieser Unterschied wird für ein zusätzliches Qubit berechnet.</span><span class="sxs-lookup"><span data-stu-id="80402-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="80402-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80402-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="80402-108">prevfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="80402-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="80402-109">Liste der Indizes für vorherige pqrs... Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="80402-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="80402-110">nextfermionicterm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="80402-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="80402-111">Liste der Indizes für die nächsten pqrs... Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="80402-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="80402-112">AUX: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="80402-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="80402-113">Ein zusätzliches Qubit, auf das die Ergebnisse der Paritäts Berechnung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="80402-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="80402-114">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="80402-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="80402-115">Qubit wurde von allen pqrs bearbeitet... Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="80402-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="80402-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="80402-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="80402-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80402-117">Remarks</span></span>

<span data-ttu-id="80402-118">Dabei wird davon ausgegangen, dass die Indizes von P < Q < R < S <... für prevpq und nextpq.</span><span class="sxs-lookup"><span data-stu-id="80402-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>