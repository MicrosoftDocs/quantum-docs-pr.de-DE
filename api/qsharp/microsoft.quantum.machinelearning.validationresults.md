---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Benutzerdefinierter ValidationResults-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 42bfab7fd1f9372d9394f2eaf2d698b39b4307e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211490"
---
# <a name="validationresults-user-defined-type"></a>Benutzerdefinierter ValidationResults-Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Die Ergebnisse aus der Validierung eines Klassifizierers mit einer Reihe von Beispielen.

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="nmisclassifications--int"></a>Nfehlklassifizierungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der während der Validierung beobachteten fehl Klassifizierungen.
### <a name="nvalidationsamples--int"></a>Nvalidationsamples: [int](xref:microsoft.quantum.lang-ref.int)

