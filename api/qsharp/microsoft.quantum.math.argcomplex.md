---
uid: Microsoft.Quantum.Math.ArgComplex
title: Argcomplex-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: e8ce73a43940ab0ed66338f962cc6f76fc2b694b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842754"
---
# <a name="argcomplex-function"></a><span data-ttu-id="158da-102">Argcomplex-Funktion</span><span class="sxs-lookup"><span data-stu-id="158da-102">ArgComplex function</span></span>

<span data-ttu-id="158da-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="158da-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="158da-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="158da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="158da-105">Gibt die Phase einer komplexen Zahl vom Typ zurück `Complex` .</span><span class="sxs-lookup"><span data-stu-id="158da-105">Returns the phase of a complex number of type `Complex`.</span></span>

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a><span data-ttu-id="158da-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="158da-106">Input</span></span>

### <a name="input--complex"></a><span data-ttu-id="158da-107">Eingabe: [Komplex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="158da-107">input : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="158da-108">Komplexe Zahl $c = x + i y $.</span><span class="sxs-lookup"><span data-stu-id="158da-108">Complex number $c = x + i y$.</span></span>



## <a name="output--double"></a><span data-ttu-id="158da-109">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="158da-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="158da-110">Phase $ \text{Arg} [c] = \text{ARCTAN} (y, x) \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="158da-110">Phase $\text{Arg}[c] = \text{ArcTan}(y,x) \in (-\pi,\pi]$.</span></span>