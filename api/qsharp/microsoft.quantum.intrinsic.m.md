---
uid: Microsoft.Quantum.Intrinsic.M
title: M-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 0037d7f5ad060857c6ca2c863b1d24aca3e338cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818872"
---
# <a name="m-operation"></a><span data-ttu-id="34928-102">M-Vorgang</span><span class="sxs-lookup"><span data-stu-id="34928-102">M operation</span></span>

<span data-ttu-id="34928-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="34928-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="34928-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="34928-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="34928-105">Führt eine Messung eines einzelnen Qubit in der Pauli-$Z $ aus.</span><span class="sxs-lookup"><span data-stu-id="34928-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="34928-106">Das Ausgabe Ergebnis wird durch die Distribution \begin{align} \pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span><span class="sxs-lookup"><span data-stu-id="34928-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="34928-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="34928-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="34928-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34928-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="34928-109">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="34928-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="34928-110">Qubit, das gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="34928-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="34928-111">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="34928-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="34928-112">`Zero` , wenn der Eigen Wert $ + $1 festgestellt wird, und, `One` Wenn der Eigen Wert $-$1 festgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="34928-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="34928-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34928-113">Remarks</span></span>

<span data-ttu-id="34928-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="34928-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```