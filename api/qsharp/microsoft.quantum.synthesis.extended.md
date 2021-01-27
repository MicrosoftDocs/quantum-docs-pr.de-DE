---
uid: Microsoft.Quantum.Synthesis.Extended
title: Erweiterte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855472"
---
# <a name="extended-function"></a>Erweiterte Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erweitert ein Spektrum durch invertierte Koeffizienten

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="spectrum--int"></a>Spektrum: [int](xref:microsoft.quantum.lang-ref.int)[]

Spektral Koeffizienten



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Koeffizienten gefolgt von umgekehrter Kopie

## <a name="example"></a>Beispiel

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```