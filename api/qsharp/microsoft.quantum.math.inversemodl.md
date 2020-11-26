---
uid: Microsoft.Quantum.Math.InverseModL
title: Inverlmodl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 0d768114c84025a067e0b60762e6834fbd36deb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228184"
---
# <a name="inversemodl-function"></a><span data-ttu-id="387ef-102">Inverlmodl-Funktion</span><span class="sxs-lookup"><span data-stu-id="387ef-102">InverseModL function</span></span>

<span data-ttu-id="387ef-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="387ef-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="387ef-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="387ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="387ef-105">Gibt $b $ zurück, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="387ef-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="387ef-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="387ef-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="387ef-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="387ef-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="387ef-108">Die Zahl, die umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="387ef-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="387ef-109">Modulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="387ef-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="387ef-110">Der Modulo, gemäß dem die Zahlen invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="387ef-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="387ef-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="387ef-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="387ef-112">Ganze Zahl $b $, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="387ef-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>