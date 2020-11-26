---
uid: Microsoft.Quantum.Math.InverseModI
title: Inversetmodi-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 217ce4cd113ecbc6a06ed83c6c1dcb7baa46387d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195374"
---
# <a name="inversemodi-function"></a><span data-ttu-id="2c4e7-102">Inversetmodi-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c4e7-102">InverseModI function</span></span>

<span data-ttu-id="2c4e7-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2c4e7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c4e7-105">Gibt $b $ zurück, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="2c4e7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2c4e7-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="2c4e7-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c4e7-108">Die Zahl, die umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="2c4e7-109">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c4e7-110">Der Modulo, gemäß dem die Zahlen invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="2c4e7-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c4e7-112">Ganze Zahl $b $, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>