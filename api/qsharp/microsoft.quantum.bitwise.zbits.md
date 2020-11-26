---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Zbits-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: 3ded981dc53236a48f1fb8f6ae12e39c17469447
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219446"
---
# <a name="zbits-function"></a><span data-ttu-id="82110-102">Zbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="82110-102">ZBits function</span></span>

<span data-ttu-id="82110-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="82110-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="82110-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="82110-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="82110-105">Gibt eine ganze Zahl zurück, die die Z-Bits eines Arrays von Pauli-Operatoren darstellt.</span><span class="sxs-lookup"><span data-stu-id="82110-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="82110-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="82110-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="82110-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="82110-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="82110-108">Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82110-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="82110-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82110-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82110-110">Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliX` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliY` oder ist `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="82110-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="82110-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82110-111">Remarks</span></span>

<span data-ttu-id="82110-112">Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.</span><span class="sxs-lookup"><span data-stu-id="82110-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="82110-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82110-113">See Also</span></span>

- [<span data-ttu-id="82110-114">Microsoft. Quantum. bitse. xbits</span><span class="sxs-lookup"><span data-stu-id="82110-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)