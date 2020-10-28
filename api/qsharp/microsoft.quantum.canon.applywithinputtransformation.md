---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Applywithinputtransformation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 2b7863337ef724d9c3ba10201a9a01d0b2226ea8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704567"
---
# <a name="applywithinputtransformation-operation"></a>Applywithinputtransformation-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Bei einem Vorgang, der eine Eingabe akzeptiert, eine Funktion, die eine mit diesem Vorgang kompatible Ausgabe zurückgibt, sowie eine Eingabe für diese Funktion wendet den Vorgang mithilfe der-Funktion an, um die Eingabe in ein vom Vorgang erwartetes Formular umzuwandeln.

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a>Eingabe

### <a name="fn--u---t"></a>FN: ' U-> 't

Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.


### <a name="op--t--unit"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Der anzuwendende Vorgang.


### <a name="input--u"></a>Eingabe: "U

Eine Eingabe für die Funktion.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applywithinputtransformationa](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [Microsoft. Quantum. Canon. applywithinputtransformationc](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [Microsoft. Quantum. Canon. applywithinputtransformationca](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [Microsoft. Quantum. Canon. transformedoperation](xref:Microsoft.Quantum.Canon.TransformedOperation)