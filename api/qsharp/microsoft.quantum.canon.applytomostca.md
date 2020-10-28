---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Applytomostca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 797cbd835446f31b2df60dbb184f888e6d0356aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704738"
---
# <a name="applytomostca-operation"></a>Applytomostca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf alle bis auf das letzte Element eines Arrays an.

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Most(targets))` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit-adj--ctl"></a>OP: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein anzuwendende Vorgang.


### <a name="targets--t"></a>Ziele: 't []

Ein Array von Zielen, von denen alle außer der letzten angewendet werden `op` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applytomost](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [Microsoft. Quantum. Canon. applytomosta](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [Microsoft. Quantum. Canon. applytomostc](xref:Microsoft.Quantum.Canon.ApplyToMostC)