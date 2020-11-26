---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: Boolarrayasresultarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: 388fb67ba33810fc813fb646577bfa7f4a2b51ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224461"
---
# <a name="boolarrayasresultarray-function"></a>Boolarrayasresultarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert einen `Bool[]` Typ in einen `Result[]` -Typ, wobei `true` zugeordnet ist `One` und `false` zugeordnet ist `Zero` .

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a>Eingabe

### <a name="input--bool"></a>Eingabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

`Bool[]` , das konvertiert werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__[]

Die `Result[]`, die das `input` darstellt.