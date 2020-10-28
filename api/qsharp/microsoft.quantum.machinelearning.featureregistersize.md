---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Featureregistersize-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 8f7c47c7547e7a0ac1672f308de445c1b46461e1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723284"
---
# <a name="featureregistersize-function"></a>Featureregistersize-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Gibt die Anzahl von Qubits zurück, die erforderlich sind, um einen bestimmten featurevektor zu codieren.

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="sample--double"></a>Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Beispiel Funktions Vektor, der in ein Qubit-Register codiert werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die zum Codieren `sample` in ein Qubit-Register erforderliche Größe, ausgedrückt als Anzahl von Qubits.