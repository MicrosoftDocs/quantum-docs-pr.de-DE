---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Applydetailc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 631e08666002d8077c6f8b78525b06b104dd4c7c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704626"
---
# <a name="applytotailc-operation"></a>Applydetailc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf das letzte Element eines Arrays an.

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit-ctl"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Ein anzuwendende Vorgang.


### <a name="targets--t"></a>Ziele: 't []

Ein Array von Zielen, auf das der letzte angewendet wird `op` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyumtail](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [Microsoft. Quantum. Canon. applyumtaila](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [Microsoft. Quantum. Canon. applyumtailca](xref:Microsoft.Quantum.Canon.ApplyToTailCA)