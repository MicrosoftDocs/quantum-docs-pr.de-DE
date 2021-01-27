---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: fe64343e30a0a3f0d05382e7812d37d5b13133d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853212"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a><span data-ttu-id="d0d07-102">_ExtractLogicalQubitFromSteaneCode Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0d07-102">_ExtractLogicalQubitFromSteaneCode operation</span></span>

<span data-ttu-id="d0d07-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d0d07-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d0d07-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d0d07-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d0d07-105">Die Messgeräte Messung und die Umkehrung der Einbettung.</span><span class="sxs-lookup"><span data-stu-id="d0d07-105">Syndrome measurement and the inverse of embedding.</span></span>

<span data-ttu-id="d0d07-106">$X $-und $Z $-Stabilizers werden nicht gleichermaßen behandelt, was auf die jeweilige Auswahl der Codierungs Verbindung zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="d0d07-106">$X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit.</span></span>
<span data-ttu-id="d0d07-107">Diese Asymmetrie führt zu einer anderen Extraktions Routine für die Analyse.</span><span class="sxs-lookup"><span data-stu-id="d0d07-107">This asymmetry leads to a different syndrome extraction routine.</span></span>
<span data-ttu-id="d0d07-108">Sie können das-Syndrom Messen, indem Sie den multiqubit-Pauli-Operator direkt auf den Code Zustand messen. für den Zweck der Wiederverwendung wird jedoch das logische Qubit an ein einzelnes Qubit zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0d07-108">One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.</span></span>

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a><span data-ttu-id="d0d07-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0d07-109">Input</span></span>

### <a name="code--logicalregister"></a><span data-ttu-id="d0d07-110">Code: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="d0d07-110">code : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>





## <a name="output--qubitintint"></a><span data-ttu-id="d0d07-111">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="d0d07-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="d0d07-112">Das logische Qubit und ein paar von ganzen Zahlen für $X $--Syndrom und $Z $--Syndrom.</span><span class="sxs-lookup"><span data-stu-id="d0d07-112">The logical qubit and a pair of integers for $X$-syndrome and $Z$-syndrome.</span></span>
<span data-ttu-id="d0d07-113">Sie stellen den Index des Code-Qubit dar, auf dem ein einzelner $X $-oder $Z $-Error das gemessene Syndrom verursacht hätte.</span><span class="sxs-lookup"><span data-stu-id="d0d07-113">They represent the index of the code qubit on which a single $X$- or $Z$-error would have caused the measured syndrome.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0d07-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0d07-114">Remarks</span></span>

<span data-ttu-id="d0d07-115">Beachten Sie, dass dieser Vorgang nicht als gekennzeichnet ist `internal` , da Komponententests direkt von diesem Vorgang abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d0d07-115">Note that this operation is not marked as `internal`, as unit tests directly depend on this operation.</span></span> <span data-ttu-id="d0d07-116">Bei zukünftigen Verbesserungen sollten Komponententests umgestaltet werden, damit Sie nur direkt von öffentlichen callables abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="d0d07-116">As a future improvement, unit tests should be refactored to depend only on public callables directly.</span></span>

> [!WARNING]
> <span data-ttu-id="d0d07-117">Diese Routine ist auf eine bestimmte Codierungs Verbindung für den 7-Qubit-Code von Steane zugeschnitten. Wenn die Codierungs Verbindung geändert wird, muss das Ergebnis des-syndrotes möglicherweise anders interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="d0d07-117">This routine is tailored to a particular encoding circuit for Steane's 7 qubit code; if the encoding circuit is modified then the syndrome outcome might have to be interpreted differently.</span></span>