---
uid: Microsoft.Quantum.Bitwise.Parity
title: Paritäts Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Parity
qsharp.summary: Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).
ms.openlocfilehash: b34ef36b0336ec1dea7fdbd878c6d695b38d623e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842132"
---
# <a name="parity-function"></a><span data-ttu-id="44fe2-102">Paritäts Funktion</span><span class="sxs-lookup"><span data-stu-id="44fe2-102">Parity function</span></span>

<span data-ttu-id="44fe2-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="44fe2-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="44fe2-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="44fe2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="44fe2-105">Gibt die bitweise Parität einer Ganzzahl zurück (1, wenn die binäre Darstellung eine ungerade Anzahl von Elementen enthält, andernfalls 0).</span><span class="sxs-lookup"><span data-stu-id="44fe2-105">Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).</span></span>

```qsharp
function Parity (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="44fe2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="44fe2-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="44fe2-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="44fe2-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="44fe2-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="44fe2-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="44fe2-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44fe2-109">Example</span></span>

```qsharp
let a = 248;
let x = Parity(a); // x : Int = 1.
```