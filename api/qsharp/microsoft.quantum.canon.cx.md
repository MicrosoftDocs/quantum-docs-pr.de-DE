---
uid: Microsoft.Quantum.Canon.CX
title: CX-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: e27b30a6b4609daaac2cc5eda68120115777af0c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840755"
---
# <a name="cx-operation"></a><span data-ttu-id="558a4-102">CX-Vorgang</span><span class="sxs-lookup"><span data-stu-id="558a4-102">CX operation</span></span>

<span data-ttu-id="558a4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="558a4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="558a4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="558a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="558a4-105">Wendet das X (gesteuertes X)-Gate auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="558a4-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="558a4-106">$ $ \begin{align} \left (\begin{Matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{Matrix}\right) \end{align}, $ $, wobei Zeilen und Spalten im Quantum-Konzept Handbuch organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="558a4-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="558a4-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="558a4-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="558a4-108">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="558a4-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="558a4-109">Steuerelement-Qubit für das CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="558a4-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="558a4-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="558a4-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="558a4-111">Ziel-Qubit für das CX-Gate.</span><span class="sxs-lookup"><span data-stu-id="558a4-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="558a4-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="558a4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="558a4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="558a4-113">Remarks</span></span>

<span data-ttu-id="558a4-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="558a4-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="558a4-115">und zu:</span><span class="sxs-lookup"><span data-stu-id="558a4-115">and to:</span></span>

```qsharp
CNOT(control, target);
```