---
uid: Microsoft.Quantum.Intrinsic.M
title: M-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 8d4b120385bfc7086a7cb0e3f77034c760d78d92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707154"
---
# <a name="m-operation"></a><span data-ttu-id="8233b-102">M-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8233b-102">M operation</span></span>

<span data-ttu-id="8233b-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="8233b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="8233b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8233b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8233b-105">Führt eine Messung eines einzelnen Qubit in der Pauli-$Z $ aus.</span><span class="sxs-lookup"><span data-stu-id="8233b-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="8233b-106">Das Ausgabe Ergebnis wird durch die Distribution \begin{align} \pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span><span class="sxs-lookup"><span data-stu-id="8233b-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="8233b-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="8233b-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="8233b-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8233b-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="8233b-109">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8233b-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8233b-110">Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8233b-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="8233b-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="8233b-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="8233b-112">`Zero` , wenn der Eigen Wert $ + $1 festgestellt wird, und, `One` Wenn der Eigen Wert $-$1 festgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8233b-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8233b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8233b-113">Remarks</span></span>

<span data-ttu-id="8233b-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="8233b-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```