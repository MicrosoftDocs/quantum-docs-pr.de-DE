---
uid: Microsoft.Quantum.Bitwise.XBits
title: Xbits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: 91619803c7efe56e617b16637f5302aa0b7978ec
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705570"
---
# <a name="xbits-function"></a><span data-ttu-id="420d0-102">Xbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="420d0-102">XBits function</span></span>

<span data-ttu-id="420d0-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="420d0-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="420d0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="420d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="420d0-105">Gibt eine ganze Zahl zurück, die die X-Bits eines Arrays von Pauli-Operatoren darstellt.</span><span class="sxs-lookup"><span data-stu-id="420d0-105">Returns an integer representing the X bits of an array of Pauli operators.</span></span>

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="420d0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="420d0-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="420d0-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="420d0-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="420d0-108">Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="420d0-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="420d0-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="420d0-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="420d0-110">Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliZ` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliX` oder ist `PauliY` .</span><span class="sxs-lookup"><span data-stu-id="420d0-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliZ` and where $p_i = 1$ if `paulis[i]` is `PauliX` or `PauliY`.</span></span>

## <a name="remarks"></a><span data-ttu-id="420d0-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="420d0-111">Remarks</span></span>

<span data-ttu-id="420d0-112">Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.</span><span class="sxs-lookup"><span data-stu-id="420d0-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="420d0-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="420d0-113">See Also</span></span>

- [<span data-ttu-id="420d0-114">Microsoft. Quantum. bitse. zbits</span><span class="sxs-lookup"><span data-stu-id="420d0-114">Microsoft.Quantum.Bitwise.ZBits</span></span>](xref:Microsoft.Quantum.Bitwise.ZBits)