---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Benutzerdefinierter ValidationResults-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 1e54a5a086035f5f8d36d777badb306156d99600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706815"
---
# <a name="validationresults-user-defined-type"></a>Benutzerdefinierter ValidationResults-Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Die Ergebnisse aus der Validierung eines Klassifizierers mit einer Reihe von Beispielen.

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="nmisclassifications--int"></a>Nfehlklassifizierungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der während der Validierung beobachteten fehl Klassifizierungen.
### <a name="nvalidationsamples--int"></a>Nvalidationsamples: [int](xref:microsoft.quantum.lang-ref.int)

