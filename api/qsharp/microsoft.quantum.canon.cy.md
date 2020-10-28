---
uid: Microsoft.Quantum.Canon.CY
title: CY-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 291891457ff39cf7092d17aa1d900dd0d35d9cf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704279"
---
# <a name="cy-operation"></a><span data-ttu-id="1065a-102">CY-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1065a-102">CY operation</span></span>

<span data-ttu-id="1065a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1065a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1065a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1065a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1065a-105">Wendet das Ende-Y-Gate (CY) auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="1065a-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="1065a-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-i \\ \\ 0 & 0 & i & 0 \end{align}, $ $, wobei Zeilen und Spalten im Quantum-Konzept Handbuch organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="1065a-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="1065a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1065a-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="1065a-108">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1065a-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1065a-109">Steuerelement-Qubit für das CY-Gate.</span><span class="sxs-lookup"><span data-stu-id="1065a-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="1065a-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1065a-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1065a-111">Ziel-Qubit für das CY Gate.</span><span class="sxs-lookup"><span data-stu-id="1065a-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1065a-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1065a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1065a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1065a-113">Remarks</span></span>

<span data-ttu-id="1065a-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="1065a-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```