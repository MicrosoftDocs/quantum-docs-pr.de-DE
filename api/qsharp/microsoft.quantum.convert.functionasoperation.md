---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Functionasoperation-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 10703818242cf6b3853f08a45bfb9094f397f6c2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224376"
---
# <a name="functionasoperation-function"></a>Functionasoperation-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert Funktionen in Vorgänge.

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a>BESCHREIBUNG

Gibt bei Angabe einer Funktion einen Vorgang zurück, der diese Funktion aufruft, und der nichts anderes bewirkt.

## <a name="input"></a>Eingabe

### <a name="fn--input---output"></a>FN: "Input->"-Ausgabe

Eine Funktion, die in einen Vorgang konvertiert werden soll.



## <a name="output--input--output"></a>Ausgabe: Eingabe => Ausgabe 

Ein Vorgang `op` , der `op(input)` mit `fn(input)` for all identisch ist `input` .

## <a name="type-parameters"></a>Typparameter

### <a name="input"></a>' Eingabe

Der Eingabetyp der Funktion, die konvertiert werden soll.
### <a name="output"></a>' Ausgabe

Der Ausgabetyp der Funktion, die konvertiert werden soll.

## <a name="remarks"></a>Bemerkungen

Dies ist vor allem nützlich für das Übergeben von Funktionen an Funktionen oder Vorgänge, die einen Vorgang als Eingabe erwarten.