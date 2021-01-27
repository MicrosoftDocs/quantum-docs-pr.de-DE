---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Benutzerdefinierter ValidationResults-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 923fd80333b6bf77daeaac2bf205db620e61cfd0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846090"
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

