---
uid: Microsoft.Quantum.Bitwise.XBits
title: Xbits-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: ddaace8df6e4c47c4affe2eeffb8d8ce31f37327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845247"
---
# <a name="xbits-function"></a><span data-ttu-id="a2935-102">Xbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2935-102">XBits function</span></span>

<span data-ttu-id="a2935-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="a2935-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="a2935-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a2935-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a2935-105">Gibt eine ganze Zahl zurück, die die X-Bits eines Arrays von Pauli-Operatoren darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2935-105">Returns an integer representing the X bits of an array of Pauli operators.</span></span>

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="a2935-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a2935-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="a2935-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="a2935-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="a2935-108">Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2935-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="a2935-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a2935-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a2935-110">Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliZ` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliX` oder ist `PauliY` .</span><span class="sxs-lookup"><span data-stu-id="a2935-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliZ` and where $p_i = 1$ if `paulis[i]` is `PauliX` or `PauliY`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2935-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2935-111">Remarks</span></span>

<span data-ttu-id="a2935-112">Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.</span><span class="sxs-lookup"><span data-stu-id="a2935-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2935-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a2935-113">See Also</span></span>

- [<span data-ttu-id="a2935-114">Microsoft. Quantum. bitse. zbits</span><span class="sxs-lookup"><span data-stu-id="a2935-114">Microsoft.Quantum.Bitwise.ZBits</span></span>](xref:Microsoft.Quantum.Bitwise.ZBits)