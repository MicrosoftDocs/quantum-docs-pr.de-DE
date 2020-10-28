---
uid: Microsoft.Quantum.Convert.Call
title: Aufrufvorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 8630f846b4b9823ce1c1dfd61dc8ca81e468517d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702995"
---
# <a name="call-operation"></a>Aufrufvorgang

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paketen [](https://nuget.org/packages/)


Ruft eine Funktion mit einer angegebenen Eingabe auf.

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a>BESCHREIBUNG

Wenn eine Funktion und eine Eingabe für diese Funktion angegeben sind, ruft die Funktion auf und gibt Ihre Ausgabe zurück.

## <a name="input"></a>Eingabe

### <a name="fn--input---output"></a>FN: "Input->"-Ausgabe

Eine Funktion, die aufgerufen werden soll.


### <a name="input--input"></a>Eingabe: ' Eingabe

Die Eingabe, die an die Funktion übermittelt werden soll.



## <a name="output--output"></a>Ausgabe: "Output

Das Ergebnis des Aufrufs von `fn`.

## <a name="type-parameters"></a>Typparameter

### <a name="input"></a>' Eingabe


### <a name="output"></a>' Ausgabe



## <a name="remarks"></a>Hinweise

Dieser Vorgang ist besonders nützlich, um zu erzwingen, dass eine Funktion an einer bestimmten Stelle innerhalb eines Vorgangs aufgerufen wird, oder zum Aufrufen einer Funktion, bei der ein Vorgang erwartet wird.