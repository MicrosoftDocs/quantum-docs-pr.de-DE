---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Zbits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: f66b8ef0370e898dd1d095ff2840c91566f32cb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705551"
---
# <a name="zbits-function"></a><span data-ttu-id="51e0c-102">Zbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="51e0c-102">ZBits function</span></span>

<span data-ttu-id="51e0c-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="51e0c-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="51e0c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51e0c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51e0c-105">Gibt eine ganze Zahl zurück, die die Z-Bits eines Arrays von Pauli-Operatoren darstellt.</span><span class="sxs-lookup"><span data-stu-id="51e0c-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="51e0c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="51e0c-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="51e0c-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="51e0c-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="51e0c-108">Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51e0c-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="51e0c-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51e0c-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51e0c-110">Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliX` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliY` oder ist `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="51e0c-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e0c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51e0c-111">Remarks</span></span>

<span data-ttu-id="51e0c-112">Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.</span><span class="sxs-lookup"><span data-stu-id="51e0c-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="51e0c-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51e0c-113">See Also</span></span>

- [<span data-ttu-id="51e0c-114">Microsoft. Quantum. bitse. xbits</span><span class="sxs-lookup"><span data-stu-id="51e0c-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)