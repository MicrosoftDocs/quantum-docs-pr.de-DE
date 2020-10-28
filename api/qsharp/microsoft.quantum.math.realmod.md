---
uid: Microsoft.Quantum.Math.RealMod
title: Realmod-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706799"
---
# <a name="realmod-function"></a><span data-ttu-id="bcd8a-102">Realmod-Funktion</span><span class="sxs-lookup"><span data-stu-id="bcd8a-102">RealMod function</span></span>

<span data-ttu-id="bcd8a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="bcd8a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="bcd8a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bcd8a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bcd8a-105">Berechnet den Modulo zwischen zwei reellen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="bcd8a-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="bcd8a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bcd8a-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="bcd8a-107">Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bcd8a-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bcd8a-108">Eine reelle Zahl $x $, um das Modul zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bcd8a-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="bcd8a-109">Modulo: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bcd8a-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bcd8a-110">Eine reelle Zahl, mit der der-Wert $x $ in Bezug auf übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="bcd8a-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="bcd8a-111">MinValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bcd8a-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bcd8a-112">Der kleinste Wert, der von dieser Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcd8a-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="bcd8a-113">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bcd8a-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="bcd8a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bcd8a-114">Remarks</span></span>

<span data-ttu-id="bcd8a-115">Diese Funktion berechnet den tatsächlichen Modulo, indem die reelle Linie über den Einheits Kreis umschließt und dann den Winkel des Einheits Kreises für die Eingabe findet.</span><span class="sxs-lookup"><span data-stu-id="bcd8a-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="bcd8a-116">Die `minValue` Eingabe gibt dann effektiv an, wo der Einheits Kreis abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcd8a-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>