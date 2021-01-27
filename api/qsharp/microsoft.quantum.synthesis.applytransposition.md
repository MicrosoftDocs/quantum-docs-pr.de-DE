---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Applytransformation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855581"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="f4d41-102">Applytransformation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4d41-102">ApplyTransposition operation</span></span>

<span data-ttu-id="f4d41-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f4d41-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f4d41-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4d41-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f4d41-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4d41-105">Description</span></span>

<span data-ttu-id="f4d41-106">Mit diesem Vorgang wird die Amplitude beim Index `a` mit der Amplitude bei Index `b` im angegebenen Status Vektor der `register` Länge $n $ vertauscht.</span><span class="sxs-lookup"><span data-stu-id="f4d41-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="f4d41-107">Wenn `a` entspricht `b` , wird der Zustands Vektor nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="f4d41-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="f4d41-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4d41-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f4d41-109">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4d41-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4d41-110">Erster Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)</span><span class="sxs-lookup"><span data-stu-id="f4d41-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="f4d41-111">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4d41-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4d41-112">Zweiter Index (muss ein Wert zwischen 0 und $2 ^ n-$1 sein)</span><span class="sxs-lookup"><span data-stu-id="f4d41-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="f4d41-113">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f4d41-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f4d41-114">Eine Liste von $n $ Qubits, auf die die-Umsetzung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4d41-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f4d41-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4d41-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="f4d41-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f4d41-116">Example</span></span>

<span data-ttu-id="f4d41-117">Bereiten Sie eine einheitliche Superposition der Zahl Zustände $ | 1 \ rangle $, $ | 2 \ rangle $ und $ | 3 \ rangle $ on 2 Qubits vor.</span><span class="sxs-lookup"><span data-stu-id="f4d41-117">Prepare a uniform superposition of number states $|1\rangle$, $|2\rangle$, and $|3\rangle$ on 2 qubits.</span></span>

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```