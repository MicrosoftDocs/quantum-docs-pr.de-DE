---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Applytransformation-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203313"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="dadc7-102">Applytransformation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dadc7-102">ApplyTransposition operation</span></span>

<span data-ttu-id="dadc7-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="dadc7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="dadc7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dadc7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="dadc7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dadc7-105">Description</span></span>

<span data-ttu-id="dadc7-106">Mit diesem Vorgang wird die Amplitude beim Index `a` mit der Amplitude bei Index `b` im angegebenen Status Vektor der `register` Länge $n $ vertauscht.</span><span class="sxs-lookup"><span data-stu-id="dadc7-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="dadc7-107">Wenn `a` entspricht `b` , wird der Zustands Vektor nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="dadc7-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="dadc7-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dadc7-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="dadc7-109">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dadc7-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dadc7-110">Erster Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)</span><span class="sxs-lookup"><span data-stu-id="dadc7-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="dadc7-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dadc7-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dadc7-112">Zweiter Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)</span><span class="sxs-lookup"><span data-stu-id="dadc7-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="dadc7-113">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="dadc7-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="dadc7-114">Eine Liste von $n $ Qubits, auf die die-Umsetzung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dadc7-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dadc7-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dadc7-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

