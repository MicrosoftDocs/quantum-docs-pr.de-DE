---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Applytoriesta-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 99a18e835115491cc3451a4e3b44a6ff70e9dc6c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704690"
---
# <a name="applytoresta-operation"></a>Applytoriesta-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf alle außer auf das erste Element eines Arrays an.

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Rest(targets))` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit-adj"></a>OP: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein anzuwendende Vorgang.


### <a name="targets--t"></a>Ziele: 't []

Ein Array von Zielen, von denen alle außer der ersten übernommen werden `op` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applytor EST](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [Microsoft. Quantum. Canon. applytor](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [Microsoft. Quantum. Canon. applytor estca](xref:Microsoft.Quantum.Canon.ApplyToRestCA)