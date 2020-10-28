---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Inputencoder-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 771cf01866498f4662864939e6946526c2b5827a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701375"
---
# <a name="inputencoder-function"></a>Inputencoder-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Gibt bei einem Satz von Koeffizienten und einer Toleranz einen Zustands Vorbereitungs Vorgang zurück, bei dem jeder Koeffizient als die entsprechende Amplitude eines Berechnungsbasis Zustands vorbereitet wird.

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Die Koeffizienten, die in einen Eingabe Zustand codiert werden sollen.



## <a name="output--stategenerator"></a>Ausgabe: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Ein Zustands Vorbereitungs Vorgang, bei dem die angegebenen Koeffizienten als Eingabe Zustand für ein bestimmtes Register vorbereitet werden.