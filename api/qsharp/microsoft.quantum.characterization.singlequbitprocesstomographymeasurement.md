---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Singlequbitprocesstomographymeasurement-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 3756040df8e34ecee1e968428b08387e0096ab7b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204197"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="a3fc6-102">Singlequbitprocesstomographymeasurement-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a3fc6-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="a3fc6-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="a3fc6-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="a3fc6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3fc6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3fc6-105">Führt eine Single-Qubit-Prozess-Tomographie-Messung auf der Grundlage eines bestimmten relevanten Kanals aus.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="a3fc6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3fc6-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="a3fc6-107">Vorbereitung: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="a3fc6-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="a3fc6-108">Das Pauli-Basiselement $P $, in dem ein Qubit vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="a3fc6-109">Messung: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="a3fc6-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="a3fc6-110">Das Pauli-Basiselement $Q $, in dem ein Qubit gemessen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="a3fc6-111">Channel: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a3fc6-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a3fc6-112">Ein einzelner Qubit-Kanal $ \lambda $, dessen Verhalten mit der Prozess Tomographie geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a3fc6-113">Ausgabe: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a3fc6-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="a3fc6-114">Das Ergebnis `Zero` mit der Wahrscheinlichkeit $ $ \begin{align} \pr (\texttt{Zero} | \lambda; P, Q) = \operatorname{TR}\left (\bruch {\boldone + Q} {2} \lambda\left [\bruchteil {\boldone + P} {2} \right] \right).</span><span class="sxs-lookup"><span data-stu-id="a3fc6-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="a3fc6-115">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a3fc6-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="a3fc6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3fc6-116">Remarks</span></span>

<span data-ttu-id="a3fc6-117">Die Verteilung der Ergebnisse, die von diesem Vorgang zurückgegeben werden, ist ein Sonderfall von zwei-Qubit-Zustands-Tomographie.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="a3fc6-118">Let $ \rho = J (\lambda)/$2 ist der Bundesstaat Choi – jamiłkowski für $ \lambda $.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="a3fc6-119">Anschließend ist die obige Verteilung mit $ $ \begin{align} \pr (\texttt{Zero} | \rho;) identisch. M) = \operatorname{TR} (m \rho), \end{align} $ $ WHERE $M = 2 (\boldone + P) ^ \mathrm{t}/2 \cdot (\boldone + Q)/$2 ist das effektive Maß, das $P $ und $Q $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="a3fc6-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>