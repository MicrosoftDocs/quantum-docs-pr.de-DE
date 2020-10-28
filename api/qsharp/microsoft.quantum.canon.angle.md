---
uid: Microsoft.Quantum.Canon.Angle
title: Angle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705522"
---
# <a name="angle-function"></a><span data-ttu-id="7e84d-102">Angle-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e84d-102">Angle function</span></span>

<span data-ttu-id="7e84d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7e84d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7e84d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7e84d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7e84d-105">Gibt 1 zurück, wenn `index` eine ungerade Zahl von 1 s und-1 aufweist, wenn `index` eine gerade Anzahl von 1 s hat.</span><span class="sxs-lookup"><span data-stu-id="7e84d-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="7e84d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e84d-106">Description</span></span>

<span data-ttu-id="7e84d-107">Der Wert entspricht dem Vorzeichen des Koeffizienten des Rademacher-Walsh Spektrums der n-Variablen und der Funktion für eine bestimmte Zuweisung, die den Winkel der Drehung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7e84d-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="7e84d-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7e84d-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="7e84d-109">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7e84d-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7e84d-110">Eingabe Zuweisung als Ganzzahl (von 0 bis 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="7e84d-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="7e84d-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7e84d-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

