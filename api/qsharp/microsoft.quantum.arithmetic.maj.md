---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: Maj-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 356689baa6d47b7b93a393f3672991bb589f6921
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222761"
---
# <a name="maj-operation"></a><span data-ttu-id="a4986-102">Maj-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a4986-102">MAJ operation</span></span>

<span data-ttu-id="a4986-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a4986-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a4986-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4986-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4986-105">Dadurch wird der Vorgang für die direkte Mehrheit auf 3 Qubits angewendet.</span><span class="sxs-lookup"><span data-stu-id="a4986-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a4986-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4986-106">Description</span></span>

<span data-ttu-id="a4986-107">Wenn wir den Zustand des Ziel-Qubit als $ \ket{z} $ und die Eingabe Zustände der Eingabe-Qubits als $ \ket{x} $ und $ \ket{y} $ bezeichnen, dieser Vorgang führt die folgende Transformation aus: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{Maj} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="a4986-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="a4986-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a4986-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="a4986-109">input0: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4986-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4986-110">Das erste Eingabe-Qubit.</span><span class="sxs-lookup"><span data-stu-id="a4986-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="a4986-111">eingabe1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4986-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4986-112">Das zweite Eingabe-Qubit.</span><span class="sxs-lookup"><span data-stu-id="a4986-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a4986-113">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4986-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4986-114">Ein Qubit, auf das die Mehrheits Funktion angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4986-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a4986-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a4986-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

