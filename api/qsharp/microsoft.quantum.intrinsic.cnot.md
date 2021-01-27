---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: CNOT-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 02ae795c785dcbc25b56ac513a9237540e57ea63
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849439"
---
# <a name="cnot-operation"></a><span data-ttu-id="2e4cc-102">CNOT-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2e4cc-102">CNOT operation</span></span>

<span data-ttu-id="2e4cc-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="2e4cc-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="2e4cc-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2e4cc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2e4cc-105">Wendet das CNOT-Gate (Controlled-not) auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="2e4cc-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="2e4cc-106">\begin{align} \operatschmue{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="2e4cc-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="2e4cc-107">Dabei werden Zeilen und Spalten im Quantum-Konzept Handbuch als geordnet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e4cc-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2e4cc-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2e4cc-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="2e4cc-109">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2e4cc-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2e4cc-110">Steuerelement-Qubit für das CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="2e4cc-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="2e4cc-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2e4cc-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2e4cc-112">Ziel-Qubit für das CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="2e4cc-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e4cc-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e4cc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2e4cc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e4cc-114">Remarks</span></span>

<span data-ttu-id="2e4cc-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="2e4cc-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```