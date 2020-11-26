---
uid: Microsoft.Quantum.Convert.Call
title: Aufrufvorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 92c159cef878fb587b0ed514fd6660dd19527cab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214210"
---
# <a name="call-operation"></a>Aufrufvorgang

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Bemerkungen

Dieser Vorgang ist besonders nützlich, um zu erzwingen, dass eine Funktion an einer bestimmten Stelle innerhalb eines Vorgangs aufgerufen wird, oder zum Aufrufen einer Funktion, bei der ein Vorgang erwartet wird.