---
uid: Microsoft.Quantum.Intrinsic.M
title: M-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: ced3a617a7299e169c7a58a1cd0f83f656b2f0b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212340"
---
# <a name="m-operation"></a><span data-ttu-id="30f6d-102">M-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30f6d-102">M operation</span></span>

<span data-ttu-id="30f6d-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="30f6d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="30f6d-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="30f6d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="30f6d-105">Führt eine Messung eines einzelnen Qubit in der Pauli-$Z $ aus.</span><span class="sxs-lookup"><span data-stu-id="30f6d-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="30f6d-106">Das Ausgabe Ergebnis wird durch die Distribution \begin{align} \pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span><span class="sxs-lookup"><span data-stu-id="30f6d-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="30f6d-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="30f6d-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="30f6d-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30f6d-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="30f6d-109">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="30f6d-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="30f6d-110">Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f6d-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="30f6d-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="30f6d-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="30f6d-112">`Zero` , wenn der Eigen Wert $ + $1 festgestellt wird, und, `One` Wenn der Eigen Wert $-$1 festgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30f6d-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f6d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30f6d-113">Remarks</span></span>

<span data-ttu-id="30f6d-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="30f6d-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```