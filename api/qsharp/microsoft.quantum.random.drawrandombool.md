---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Drawrandombool-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853688"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="778b2-102">Drawrandombool-Vorgang</span><span class="sxs-lookup"><span data-stu-id="778b2-102">DrawRandomBool operation</span></span>

<span data-ttu-id="778b2-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="778b2-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="778b2-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="778b2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="778b2-105">Bei einer Erfolgswahrscheinlichkeit wird eine einzelne Bernoulli-Testversion zurückgegeben, die mit der angegebenen Wahrscheinlichkeit true ist.</span><span class="sxs-lookup"><span data-stu-id="778b2-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="778b2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="778b2-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="778b2-107">erfolgreiche Programmierung: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="778b2-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="778b2-108">Die Wahrscheinlichkeit, mit der `true` zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="778b2-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="778b2-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="778b2-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="778b2-110">`true` mit Wahrscheinlichkeit `successProbability` und `false` mit Wahrscheinlichkeit `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="778b2-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>

## <a name="example"></a><span data-ttu-id="778b2-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="778b2-111">Example</span></span>

<span data-ttu-id="778b2-112">Die folgenden Q # Ausschnitt-Beispiele werden aus einer unausgewogenen Münze gedreht:</span><span class="sxs-lookup"><span data-stu-id="778b2-112">The following Q# snippet samples flips from a biased coin:</span></span>

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```