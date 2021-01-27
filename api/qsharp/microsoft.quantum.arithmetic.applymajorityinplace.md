---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Applymajorityinplace-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 10b512392b2098663c09b2e07a09c4025da90706
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843728"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="5fbfc-102">Applymajorityinplace-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5fbfc-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="5fbfc-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5fbfc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5fbfc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5fbfc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5fbfc-105">Wendet den drei-Qubit-Mehrheits Vorgang direkt auf ein Register von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="5fbfc-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5fbfc-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fbfc-106">Description</span></span>

<span data-ttu-id="5fbfc-107">Mit diesem Vorgang wird die Mehrheits Funktion auf drei Qubits berechnet.</span><span class="sxs-lookup"><span data-stu-id="5fbfc-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="5fbfc-108">Wenn wir das Ausgabe-Qubit als $z $ und Eingabe-Qubits als $x $ und $y $ bezeichnen, führt der Vorgang die folgende Transformation aus: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatschmue{Maj} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="5fbfc-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="5fbfc-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fbfc-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="5fbfc-110">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5fbfc-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5fbfc-111">Das erste Eingabe-Qubit.</span><span class="sxs-lookup"><span data-stu-id="5fbfc-111">First input qubit.</span></span> <span data-ttu-id="5fbfc-112">Beachten Sie, dass die Ausgabe direkt berechnet und in diesem Qubit gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="5fbfc-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="5fbfc-113">Eingabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5fbfc-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5fbfc-114">Zweite und dritte Eingabe-Qubits.</span><span class="sxs-lookup"><span data-stu-id="5fbfc-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fbfc-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fbfc-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

