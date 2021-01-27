---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Featureregistersize-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 2754e901d74175c1841a38d795f5de02dabc9b8d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848438"
---
# <a name="featureregistersize-function"></a>Featureregistersize-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt die Anzahl von Qubits zurück, die erforderlich sind, um einen bestimmten featurevektor zu codieren.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="sample--double"></a>Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Beispiel Funktions Vektor, der in ein Qubit-Register codiert werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die zum Codieren `sample` in ein Qubit-Register erforderliche Größe, ausgedrückt als Anzahl von Qubits.