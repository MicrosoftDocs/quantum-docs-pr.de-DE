---
uid: Microsoft.Quantum.Convert.ResultArrayAsBoolArray
title: Resultarrayasboolarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultArrayAsBoolArray
qsharp.summary: Converts a `Result[]` type to a `Bool[]` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 384531137474562ebc8cc24dcd1ac976dc91ad9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832592"
---
# <a name="resultarrayasboolarray-function"></a>Resultarrayasboolarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert einen `Result[]` Typ in einen `Bool[]` -Typ, wobei `One` zugeordnet ist `true` und `Zero` zugeordnet ist `false` .

```qsharp
function ResultArrayAsBoolArray (input : Result[]) : Bool[]
```


## <a name="input"></a>Eingabe

### <a name="input--__invalidresult__"></a>Eingabe: __ungültig <Result>__[]

`Result[]` , das konvertiert werden soll.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Die `Bool[]`, die das `input` darstellt.