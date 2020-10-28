---
uid: Microsoft.Quantum.Math.InverseModI
title: Inversetmodi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 6efc9da5f5ebb64065a90e749daa629dc2dce9cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723634"
---
# <a name="inversemodi-function"></a><span data-ttu-id="6391b-102">Inversetmodi-Funktion</span><span class="sxs-lookup"><span data-stu-id="6391b-102">InverseModI function</span></span>

<span data-ttu-id="6391b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="6391b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="6391b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6391b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6391b-105">Gibt $b $ zurück, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="6391b-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="6391b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6391b-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6391b-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6391b-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6391b-108">Die Zahl, die umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="6391b-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="6391b-109">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6391b-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6391b-110">Der Modulo, gemäß dem die Zahlen invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6391b-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="6391b-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6391b-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6391b-112">Ganze Zahl $b $, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="6391b-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>