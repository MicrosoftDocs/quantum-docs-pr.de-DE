---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Näheratinput Encoder-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 2e39318cfaf3321c33b08f742bb25a9276b7e660
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196598"
---
# <a name="approximateinputencoder-function"></a>Näheratinput Encoder-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt anhand eines Satzes von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, der jeden Koeffizienten als die entsprechende Amplitude eines Berechnungsbasis Zustands bis zur angegebenen Toleranz vorbereitet.

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Eingabe

### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Näherungs Toleranz, die beim Codieren der angegebenen Koeffizienten in einen Eingabe Zustand verwendet werden soll.


### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.



## <a name="output--stategenerator"></a>Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.