---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Inputencoder-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: ed70d9f24af06f8918083307c98a5f6c4671f1c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852940"
---
# <a name="inputencoder-function"></a>Inputencoder-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt bei einem Satz von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, bei dem jeder Koeffizient als die entsprechende Amplitude eines Berechnungsbasis Zustands vorbereitet wird.

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.



## <a name="output--stategenerator"></a>Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.