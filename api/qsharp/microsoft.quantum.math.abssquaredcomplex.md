---
uid: Microsoft.Quantum.Math.AbsSquaredComplex
title: Abssquaredcomplex-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsSquaredComplex
qsharp.summary: Returns the squared absolute value of a complex number of type `Complex`.
ms.openlocfilehash: d48212d7f861b3ff9e37d078742f53f0cd8c71ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195901"
---
# <a name="abssquaredcomplex-function"></a><span data-ttu-id="68c80-102">Abssquaredcomplex-Funktion</span><span class="sxs-lookup"><span data-stu-id="68c80-102">AbsSquaredComplex function</span></span>

<span data-ttu-id="68c80-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="68c80-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="68c80-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="68c80-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="68c80-105">Gibt den quadratischen absoluten Wert einer komplexen Zahl vom Typ zurück `Complex` .</span><span class="sxs-lookup"><span data-stu-id="68c80-105">Returns the squared absolute value of a complex number of type `Complex`.</span></span>

```qsharp
function AbsSquaredComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="68c80-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="68c80-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="68c80-107">Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="68c80-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="68c80-108">Komplexe Zahl $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="68c80-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="68c80-109">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="68c80-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="68c80-110">Der absolute Wert $ | c | ^ 2 = x ^ 2 + y ^ 2 $ wird quadriert.</span><span class="sxs-lookup"><span data-stu-id="68c80-110">Squared absolute value $|c|^2 = x^2 + y^2$.</span></span>