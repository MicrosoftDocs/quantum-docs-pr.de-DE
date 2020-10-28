---
uid: Microsoft.Quantum.Intrinsic.CNOT
title: CNOT-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CNOT
qsharp.summary: >-
  Applies the controlled-NOT (CNOT) gate to a pair of qubits.

  \begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: 2fb5b4df189fb3ab23b2ca5cb273b2451ffcc067
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722668"
---
# <a name="cnot-operation"></a><span data-ttu-id="f2dcb-102">CNOT-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f2dcb-102">CNOT operation</span></span>

<span data-ttu-id="f2dcb-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="f2dcb-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="f2dcb-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2dcb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2dcb-105">Wendet das CNOT-Gate (Controlled-not) auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="f2dcb-105">Applies the controlled-NOT (CNOT) gate to a pair of qubits.</span></span>

<span data-ttu-id="f2dcb-106">\begin{align} \operatschmue{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span><span class="sxs-lookup"><span data-stu-id="f2dcb-106">\begin{align} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}, \end{align}</span></span>

<span data-ttu-id="f2dcb-107">Dabei werden Zeilen und Spalten im Quantum-Konzept Handbuch als geordnet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2dcb-107">where rows and columns are ordered as in the quantum concepts guide.</span></span>

```qsharp
operation CNOT (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f2dcb-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2dcb-108">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="f2dcb-109">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f2dcb-109">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f2dcb-110">Steuerelement-Qubit für das CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="f2dcb-110">Control qubit for the CNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f2dcb-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f2dcb-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f2dcb-112">Ziel-Qubit für das CNOT-Gate.</span><span class="sxs-lookup"><span data-stu-id="f2dcb-112">Target qubit for the CNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f2dcb-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f2dcb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f2dcb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2dcb-114">Remarks</span></span>

<span data-ttu-id="f2dcb-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="f2dcb-115">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```