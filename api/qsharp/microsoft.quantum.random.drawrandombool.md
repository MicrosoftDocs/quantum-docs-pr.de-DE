---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Drawrandombool-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706714"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="7c069-102">Drawrandombool-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7c069-102">DrawRandomBool operation</span></span>

<span data-ttu-id="7c069-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="7c069-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="7c069-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c069-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c069-105">Bei einer Erfolgswahrscheinlichkeit wird eine einzelne Bernoulli-Testversion zurückgegeben, die mit der angegebenen Wahrscheinlichkeit true ist.</span><span class="sxs-lookup"><span data-stu-id="7c069-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="7c069-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7c069-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="7c069-107">erfolgreiche Programmierung: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7c069-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7c069-108">Die Wahrscheinlichkeit, mit der `true` zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c069-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7c069-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c069-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c069-110">`true` mit Wahrscheinlichkeit `successProbability` und `false` mit Wahrscheinlichkeit `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="7c069-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>