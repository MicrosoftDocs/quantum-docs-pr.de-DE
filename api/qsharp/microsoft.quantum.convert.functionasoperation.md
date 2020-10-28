---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: Functionasoperation-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702984"
---
# <a name="functionasoperation-function"></a>Functionasoperation-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Dies ist vor allem nützlich für das Übergeben von Funktionen an Funktionen oder Vorgänge, die einen Vorgang als Eingabe erwarten.