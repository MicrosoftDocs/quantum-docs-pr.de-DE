---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: Austausch Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 4d8d037404ac835a1dd032790e7fd03f29591c41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849271"
---
# <a name="swap-operation"></a><span data-ttu-id="84b9b-102">Austausch Vorgang</span><span class="sxs-lookup"><span data-stu-id="84b9b-102">SWAP operation</span></span>

<span data-ttu-id="84b9b-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="84b9b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="84b9b-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="84b9b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="84b9b-105">Wendet das Auslagerungs Gate auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="84b9b-105">Applies the SWAP gate to a pair of qubits.</span></span>

<span data-ttu-id="84b9b-106">\begin{align} \operatorname{tauap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="84b9b-106">\begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="84b9b-107">Dabei werden Zeilen und Spalten im Quantum-Konzept Handbuch als geordnet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84b9b-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="84b9b-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84b9b-108">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="84b9b-109">qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="84b9b-109">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="84b9b-110">Das erste Qubit, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="84b9b-110">First qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="84b9b-111">qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="84b9b-111">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="84b9b-112">Zweites Qubit, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="84b9b-112">Second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="84b9b-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84b9b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="84b9b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84b9b-114">Remarks</span></span>

<span data-ttu-id="84b9b-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="84b9b-115">Equivalent to:</span></span>

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```