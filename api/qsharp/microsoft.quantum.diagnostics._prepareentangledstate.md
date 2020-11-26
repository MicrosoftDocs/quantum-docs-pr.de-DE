---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 97a55b4bb85095c7d8e8432dfcd1c6d6f7e93cdc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223934"
---
# <a name="_prepareentangledstate-operation"></a><span data-ttu-id="cc868-102">_prepareEntangledState Vorgang</span><span class="sxs-lookup"><span data-stu-id="cc868-102">_prepareEntangledState operation</span></span>

<span data-ttu-id="cc868-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="cc868-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="cc868-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cc868-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="cc868-105">Bei zwei Registern wird der Status der vollständig entkoppelt zwischen jedem Paar von Qubits in den entsprechenden Registern vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="cc868-105">Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers.</span></span>
<span data-ttu-id="cc868-106">Alle Qubits müssen im Zustand | 0 ⟩ beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc868-106">All qubits must start in the |0⟩ state.</span></span>

<span data-ttu-id="cc868-107">Das Ergebnis ist, dass sich die entsprechenden Paare von Qubits aus jedem Register in der $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $ befinden.</span><span class="sxs-lookup"><span data-stu-id="cc868-107">The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.</span></span>

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cc868-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc868-108">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="cc868-109">Left: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cc868-109">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cc868-110">Ein Qubit-Array im $ \ket{0\cdots 0} $-Status</span><span class="sxs-lookup"><span data-stu-id="cc868-110">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="cc868-111">Right: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cc868-111">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cc868-112">Ein Qubit-Array im $ \ket{0\cdots 0} $-Status</span><span class="sxs-lookup"><span data-stu-id="cc868-112">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="cc868-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cc868-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

