---
uid: Microsoft.Quantum.Canon.CX
title: CX-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: c430525b71ad4ef0812d90a8ff20c41a5d5b8708
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704287"
---
# <a name="cx-operation"></a><span data-ttu-id="dd7ca-102">CX-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dd7ca-102">CX operation</span></span>

<span data-ttu-id="dd7ca-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dd7ca-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dd7ca-105">Wendet das X (gesteuertes X)-Gate auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="dd7ca-106">$ $ \begin{align} \left (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{Matrix}\right) \end{align}, $ $, wobei Zeilen und Spalten im Quantum-Konzept Handbuch organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="dd7ca-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dd7ca-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="dd7ca-108">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dd7ca-109">Steuerelement-Qubit für das CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="dd7ca-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dd7ca-111">Ziel-Qubit für das CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dd7ca-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dd7ca-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd7ca-113">Remarks</span></span>

<span data-ttu-id="dd7ca-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="dd7ca-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="dd7ca-115">und zu:</span><span class="sxs-lookup"><span data-stu-id="dd7ca-115">and to:</span></span>

```qsharp
CNOT(control, target);
```