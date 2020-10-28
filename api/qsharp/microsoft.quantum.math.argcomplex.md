---
uid: Microsoft.Quantum.Math.ArgComplex
title: Argcomplex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 629aa32ad80e5aa3d6f5ff75ac65df9b1a96fc15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723269"
---
# <a name="argcomplex-function"></a><span data-ttu-id="7f013-102">Argcomplex-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f013-102">ArgComplex function</span></span>

<span data-ttu-id="7f013-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7f013-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7f013-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7f013-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7f013-105">Gibt die Phase einer komplexen Zahl vom Typ zurück `Complex` .</span><span class="sxs-lookup"><span data-stu-id="7f013-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="7f013-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7f013-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="7f013-107">Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="7f013-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="7f013-108">Komplexe Zahl $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="7f013-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="7f013-109">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7f013-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7f013-110">Phase $ \text{Arg} [c] = \text{ARCTAN} (y, x) \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="7f013-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>