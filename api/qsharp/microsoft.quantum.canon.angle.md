---
uid: Microsoft.Quantum.Canon.Angle
title: Angle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 1d8a9c2c19469e4949f043edd1ba91021fa42e78
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219412"
---
# <a name="angle-function"></a><span data-ttu-id="b55b5-102">Angle-Funktion</span><span class="sxs-lookup"><span data-stu-id="b55b5-102">Angle function</span></span>

<span data-ttu-id="b55b5-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b55b5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b55b5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b55b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b55b5-105">Gibt 1 zurück, wenn `index` eine ungerade Zahl von 1 s und-1 aufweist, wenn `index` eine gerade Anzahl von 1 s hat.</span><span class="sxs-lookup"><span data-stu-id="b55b5-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="b55b5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b55b5-106">Description</span></span>

<span data-ttu-id="b55b5-107">Der Wert entspricht dem Vorzeichen des Koeffizienten des Rademacher-Walsh Spektrums der n-Variablen und der Funktion für eine bestimmte Zuweisung, die den Winkel der Drehung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b55b5-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="b55b5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b55b5-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="b55b5-109">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b55b5-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b55b5-110">Eingabe Zuweisung als Ganzzahl (von 0 bis 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="b55b5-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="b55b5-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b55b5-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

