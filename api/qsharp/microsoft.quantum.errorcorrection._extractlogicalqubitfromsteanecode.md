---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 71390feb84660cc9bf7bb12b64eac6d3ca512387
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702576"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a><span data-ttu-id="ffd13-102">_ExtractLogicalQubitFromSteaneCode Vorgang</span><span class="sxs-lookup"><span data-stu-id="ffd13-102">_ExtractLogicalQubitFromSteaneCode operation</span></span>

<span data-ttu-id="ffd13-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="ffd13-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="ffd13-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ffd13-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ffd13-105">Die Messgeräte Messung und die Umkehrung der Einbettung.</span><span class="sxs-lookup"><span data-stu-id="ffd13-105">Syndrome measurement and the inverse of embedding.</span></span>

<span data-ttu-id="ffd13-106">$X $-und $Z $-Stabilizers werden nicht gleichermaßen behandelt, was auf die jeweilige Auswahl der Codierungs Verbindung zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="ffd13-106">$X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit.</span></span>
<span data-ttu-id="ffd13-107">Diese Asymmetrie führt zu einer anderen Extraktions Routine für die Analyse.</span><span class="sxs-lookup"><span data-stu-id="ffd13-107">This asymmetry leads to a different syndrome extraction routine.</span></span>
<span data-ttu-id="ffd13-108">Sie können das-Syndrom Messen, indem Sie den multiqubit-Pauli-Operator direkt auf den Code Zustand messen. für den Zweck der Wiederverwendung wird jedoch das logische Qubit an ein einzelnes Qubit zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ffd13-108">One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.</span></span>

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a><span data-ttu-id="ffd13-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ffd13-109">Input</span></span>

### <a name="code--logicalregister"></a><span data-ttu-id="ffd13-110">Code: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="ffd13-110">code : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>





## <a name="output--qubitintint"></a><span data-ttu-id="ffd13-111">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="ffd13-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="ffd13-112">Das logische Qubit und ein paar von ganzen Zahlen für $X $--Syndrom und $Z $--Syndrom.</span><span class="sxs-lookup"><span data-stu-id="ffd13-112">The logical qubit and a pair of integers for $X$-syndrome and $Z$-syndrome.</span></span>
<span data-ttu-id="ffd13-113">Sie stellen den Index des Code-Qubit dar, auf dem ein einzelner $X $-oder $Z $-Error das gemessene Syndrom verursacht hätte.</span><span class="sxs-lookup"><span data-stu-id="ffd13-113">They represent the index of the code qubit on which a single $X$- or $Z$-error would have caused the measured syndrome.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd13-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffd13-114">Remarks</span></span>

<span data-ttu-id="ffd13-115">Beachten Sie, dass dieser Vorgang nicht als gekennzeichnet ist `internal` , da Komponententests direkt von diesem Vorgang abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ffd13-115">Note that this operation is not marked as `internal`, as unit tests directly depend on this operation.</span></span> <span data-ttu-id="ffd13-116">Bei zukünftigen Verbesserungen sollten Komponententests umgestaltet werden, damit Sie nur direkt von öffentlichen callables abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ffd13-116">As a future improvement, unit tests should be refactored to depend only on public callables directly.</span></span>

> [!WARNING]
> <span data-ttu-id="ffd13-117">Diese Routine ist auf eine bestimmte Codierungs Verbindung für den 7-Qubit-Code von Steane zugeschnitten. Wenn die Codierungs Verbindung geändert wird, muss das Ergebnis des-syndrotes möglicherweise anders interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="ffd13-117">This routine is tailored to a particular encoding circuit for Steane's 7 qubit code; if the encoding circuit is modified then the syndrome outcome might have to be interpreted differently.</span></span>