---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Maj-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846545"
---
# <a name="maj-operation"></a><span data-ttu-id="da60c-102">Maj-Vorgang</span><span class="sxs-lookup"><span data-stu-id="da60c-102">MAJ operation</span></span>

<span data-ttu-id="da60c-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="da60c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="da60c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="da60c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="da60c-105">Dadurch wird der Vorgang für die direkte Mehrheit auf 3 Qubits angewendet.</span><span class="sxs-lookup"><span data-stu-id="da60c-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="da60c-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da60c-106">Description</span></span>

<span data-ttu-id="da60c-107">Wenn wir den Zustand des Ziel-Qubit als $ \ket{z} $ und die Eingabe Zustände der Eingabe-Qubits als $ \ket{x} $ und $ \ket{y} $ bezeichnen, dieser Vorgang führt die folgende Transformation aus: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{Maj} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="da60c-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="da60c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da60c-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="da60c-109">input0: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="da60c-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="da60c-110">Das erste Eingabe-Qubit.</span><span class="sxs-lookup"><span data-stu-id="da60c-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="da60c-111">eingabe1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="da60c-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="da60c-112">Das zweite Eingabe-Qubit.</span><span class="sxs-lookup"><span data-stu-id="da60c-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="da60c-113">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="da60c-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="da60c-114">Ein Qubit, auf das die Mehrheits Funktion angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="da60c-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="da60c-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="da60c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

