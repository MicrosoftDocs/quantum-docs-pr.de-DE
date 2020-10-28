---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Preparesinglequbitidentity-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: 12a650568aa5682e8fb6498808d188b154527acb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724880"
---
# <a name="preparesinglequbitidentity-operation"></a><span data-ttu-id="b545e-102">Preparesinglequbitidentity-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b545e-102">PrepareSingleQubitIdentity operation</span></span>

<span data-ttu-id="b545e-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b545e-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b545e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b545e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b545e-105">Bereitet ein Qubit im maximale gemischten Zustand vor.</span><span class="sxs-lookup"><span data-stu-id="b545e-105">Prepares a qubit in the maximally mixed state.</span></span>

<span data-ttu-id="b545e-106">Sie bereitet das angegebene Qubit im Zustand "$ \boldone/$2" vor, indem der%% amp; quot;%% amp; quot;%% amp; quot; \omega (\rho) \mathrel{: =} \frac {1} {4} \ sum_ {\mu \ auf 0 festgelegt \{ wird. 1, 2, 3 \} } \sigma \_ {\mu} \rho \sigma \_ {\mu} ^ {\dagger}, \end{align} $ $, wobei $ \sigma \_ i $ der $i $ th-Pauli-Operator ist und $ \rho $ ein Dichte Operator ist, der einen gemischten Zustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="b545e-106">It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.</span></span>

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b545e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b545e-107">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="b545e-108">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b545e-108">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b545e-109">Ein Qubit, dessen Zustand in der oben beschriebenen Weise depolarisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b545e-109">A qubit whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b545e-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b545e-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b545e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b545e-111">Remarks</span></span>

<span data-ttu-id="b545e-112">Der gemischte Status $ \boldone/$2, der das Ergebnis der Anwendung dieses Vorgangs auf einen Zustand beschreibt, beschreibt implizit einen Erwartungswert gegenüber zufälligen Entscheidungen, die in diesem Vorgang vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="b545e-112">The mixed state $\boldone / 2$ describing the result of applying this operation to a state implicitly describes an expectation value over random choices made in this operation.</span></span>
<span data-ttu-id="b545e-113">Folglich ordnet dieser Vorgang für jede einzelne Anwendung reine Zustände reinen Zuständen zu, aber Sie verhält sich wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="b545e-113">Thus, for any single application, this operation maps pure states to pure states, but it acts as described in expectation.</span></span>
<span data-ttu-id="b545e-114">Insbesondere kann dieser Vorgang in der Prozess Tomographie zum Messen der *nicht unitalen* Komponenten eines Kanals verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b545e-114">In particular, this operation can be used in process tomography to measure the *non-unital* components of a channel.</span></span>