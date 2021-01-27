---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: Standardnormaldistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857798"
---
# <a name="standardnormaldistribution-function"></a>Standardnormaldistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt eine normale Verteilung mit dem Mittelwert 0 und der Varianz 1 zurück.

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a>Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>Beispiel

Der folgende Code zeichnet 10 Beispiele aus der standardmäßigen Normalverteilung:

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Random. normaldistribution](xref:Microsoft.Quantum.Random.NormalDistribution)