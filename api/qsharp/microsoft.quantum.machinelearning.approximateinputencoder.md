---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Näheratinput Encoder-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 67ef7a47a2e036f0953d946b4ace0e6673b173bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706887"
---
# <a name="approximateinputencoder-function"></a>Näheratinput Encoder-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


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