---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Applytransformation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 1bd6f9580e09752f1de75927d6bb35417bb1ff21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725258"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="0ddaa-102">Applytransformation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0ddaa-102">ApplyTransposition operation</span></span>

<span data-ttu-id="0ddaa-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="0ddaa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="0ddaa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ddaa-105">Description</span></span>

<span data-ttu-id="0ddaa-106">Mit diesem Vorgang wird die Amplitude beim Index `a` mit der Amplitude bei Index `b` im angegebenen Status Vektor der `register` Länge $n $ vertauscht.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="0ddaa-107">Wenn `a` entspricht `b` , wird der Zustands Vektor nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="0ddaa-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0ddaa-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="0ddaa-109">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0ddaa-110">Erster Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="0ddaa-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0ddaa-112">Zweiter Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="0ddaa-113">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0ddaa-114">Eine Liste von $n $ Qubits, auf die die-Umsetzung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ddaa-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ddaa-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ddaa-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

