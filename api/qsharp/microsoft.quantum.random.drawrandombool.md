---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Drawrandombool-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192960"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="c230d-102">Drawrandombool-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c230d-102">DrawRandomBool operation</span></span>

<span data-ttu-id="c230d-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="c230d-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="c230d-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c230d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c230d-105">Bei einer Erfolgswahrscheinlichkeit wird eine einzelne Bernoulli-Testversion zurückgegeben, die mit der angegebenen Wahrscheinlichkeit true ist.</span><span class="sxs-lookup"><span data-stu-id="c230d-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="c230d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c230d-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="c230d-107">erfolgreiche Programmierung: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c230d-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c230d-108">Die Wahrscheinlichkeit, mit der `true` zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c230d-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c230d-109">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c230d-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c230d-110">`true` mit Wahrscheinlichkeit `successProbability` und `false` mit Wahrscheinlichkeit `1.0 - successProbability` .</span><span class="sxs-lookup"><span data-stu-id="c230d-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>