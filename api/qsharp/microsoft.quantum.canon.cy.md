---
uid: Microsoft.Quantum.Canon.CY
title: CY-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 4a1a533421dd9205e973d5e8237d67b20bc4886d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216573"
---
# <a name="cy-operation"></a><span data-ttu-id="30f84-102">CY-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30f84-102">CY operation</span></span>

<span data-ttu-id="30f84-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="30f84-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="30f84-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30f84-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30f84-105">Wendet das Ende-Y-Gate (CY) auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="30f84-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="30f84-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & i & 0 \end{align}, $ $, wobei Zeilen und Spalten im Quantum-Konzept Handbuch organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="30f84-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="30f84-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30f84-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="30f84-108">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="30f84-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="30f84-109">Steuerelement-Qubit für das CY-Gate.</span><span class="sxs-lookup"><span data-stu-id="30f84-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="30f84-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="30f84-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="30f84-111">Ziel-Qubit für das CY Gate.</span><span class="sxs-lookup"><span data-stu-id="30f84-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="30f84-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30f84-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="30f84-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30f84-113">Remarks</span></span>

<span data-ttu-id="30f84-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="30f84-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```