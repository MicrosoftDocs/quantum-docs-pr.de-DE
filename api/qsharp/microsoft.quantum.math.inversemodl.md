---
uid: Microsoft.Quantum.Math.InverseModL
title: Inverlmodl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e09c9da500889dfcb514d0a02dec957bfaa70e1c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851388"
---
# <a name="inversemodl-function"></a><span data-ttu-id="4ab3d-102">Inverlmodl-Funktion</span><span class="sxs-lookup"><span data-stu-id="4ab3d-102">InverseModL function</span></span>

<span data-ttu-id="4ab3d-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4ab3d-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4ab3d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ab3d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ab3d-105">Gibt $b $ zurück, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="4ab3d-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="4ab3d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ab3d-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="4ab3d-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4ab3d-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4ab3d-108">Die Zahl, die umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="4ab3d-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="4ab3d-109">Modulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4ab3d-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4ab3d-110">Der Modulo, gemäß dem die Zahlen invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ab3d-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="4ab3d-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4ab3d-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4ab3d-112">Ganze Zahl $b $, sodass $a \cdot b = 1 (\operatschmue{mod} \texttt{Modulus}) $.</span><span class="sxs-lookup"><span data-stu-id="4ab3d-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>