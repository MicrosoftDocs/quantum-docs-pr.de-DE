---
uid: Microsoft.Quantum.Math.RealMod
title: Realmod-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848344"
---
# <a name="realmod-function"></a><span data-ttu-id="740b7-102">Realmod-Funktion</span><span class="sxs-lookup"><span data-stu-id="740b7-102">RealMod function</span></span>

<span data-ttu-id="740b7-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="740b7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="740b7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="740b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="740b7-105">Berechnet den Modulo zwischen zwei reellen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="740b7-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="740b7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="740b7-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="740b7-107">Wert: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="740b7-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="740b7-108">Eine reelle Zahl $x $, um das Modul zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="740b7-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="740b7-109">Modulo: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="740b7-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="740b7-110">Eine reelle Zahl, mit der der-Wert $x $ in Bezug auf übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="740b7-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="740b7-111">MinValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="740b7-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="740b7-112">Der kleinste Wert, der von dieser Funktion zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="740b7-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="740b7-113">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="740b7-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="example"></a><span data-ttu-id="740b7-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="740b7-114">Example</span></span>

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a><span data-ttu-id="740b7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="740b7-115">Remarks</span></span>

<span data-ttu-id="740b7-116">Diese Funktion berechnet den tatsächlichen Modulo, indem die reelle Linie über den Einheits Kreis umschließt und dann den Winkel des Einheits Kreises für die Eingabe findet.</span><span class="sxs-lookup"><span data-stu-id="740b7-116">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="740b7-117">Die `minValue` Eingabe gibt dann effektiv an, wo der Einheits Kreis abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="740b7-117">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>