---
uid: Microsoft.Quantum.Math.AbsComplex
title: Abscomplex-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: AbsComplex
qsharp.summary: Returns the absolute value of a complex number of type `Complex`.
ms.openlocfilehash: d9afb4b9b37b6cdd83bfd3829d3174d769c5f41b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211388"
---
# <a name="abscomplex-function"></a><span data-ttu-id="f0f96-102">Abscomplex-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0f96-102">AbsComplex function</span></span>

<span data-ttu-id="f0f96-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f0f96-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f0f96-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f0f96-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f0f96-105">Gibt den absoluten Wert einer komplexen Zahl vom Typ zurück `Complex` .</span><span class="sxs-lookup"><span data-stu-id="f0f96-105">Returns the absolute value of a complex number of type `Complex`.</span></span>

```qsharp
function AbsComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="f0f96-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f0f96-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="f0f96-107">Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="f0f96-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="f0f96-108">Komplexe Zahl $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="f0f96-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="f0f96-109">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f0f96-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f0f96-110">Absoluter Wert $ | c | = \sqrt{x ^ 2 + y ^ 2} $.</span><span class="sxs-lookup"><span data-stu-id="f0f96-110">Absolute value $|c| = \sqrt{x^2 + y^2}$.</span></span>