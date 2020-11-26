---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Measure-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: 804ae72ed2d5302b14011b737b7ed3ad2b9a14ca
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212289"
---
# <a name="measure-operation"></a><span data-ttu-id="8a3ce-102">Measure-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8a3ce-102">Measure operation</span></span>

<span data-ttu-id="8a3ce-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="8a3ce-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="8a3ce-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="8a3ce-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="8a3ce-105">Führt eine gemeinsame Messung von einem oder mehreren Qubits in den angegebenen Pauli-Basen aus.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-105">Performs a joint measurement of one or more qubits in the specified Pauli bases.</span></span>

<span data-ttu-id="8a3ce-106">Das Ausgabe Ergebnis wird durch die Verteilung angegeben: \begin{align} \pr (\texttt{Zero} | \ket{\psi}) = \bruch12 \braket{\psi \mid | \left (\boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align}, wobei $P _I $ das $i $ th-Element von ist. `bases` und WHERE $N = \texttt{verlän} (\texttt{Bases}) $.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-106">The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$.</span></span>
<span data-ttu-id="8a3ce-107">Das heißt, die Messung gibt eine `Result` $d $ zurück, sodass der Eigen Wert des beobachteten Mess Effekts $ (-1) ^ d $ ist.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-107">That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.</span></span>

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="8a3ce-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a3ce-108">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="8a3ce-109">Basen: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="8a3ce-109">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="8a3ce-110">Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-110">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="8a3ce-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8a3ce-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8a3ce-112">Das Register der zu messenden Qubits.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-112">Register of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="8a3ce-113">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="8a3ce-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="8a3ce-114">`Zero` , wenn der Eigen Wert $ + $1 festgestellt wird, und, `One` Wenn der Eigen Wert $-$1 festgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-114">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3ce-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a3ce-115">Remarks</span></span>

<span data-ttu-id="8a3ce-116">Wenn die Längen Array-und Qubit-Arrays unterschiedlich lang sind, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="8a3ce-116">If the basis array and qubit array are different lengths, then the operation will fail.</span></span>