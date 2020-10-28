---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Applydetail-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 72b55ec7161d5f6af5e4cb512c648078516c3b4e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704634"
---
# <a name="applytotail-operation"></a>Applydetail-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf das letzte Element eines Arrays an.

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Array von Zielen `targets` gilt `op(Tail(targets))` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Ein anzuwendende Vorgang.


### <a name="targets--t"></a>Ziele: 't []

Ein Array von Zielen, auf das der letzte angewendet wird `op` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyumtaila](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [Microsoft. Quantum. Canon. Apply| tailc](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [Microsoft. Quantum. Canon. applyumtailca](xref:Microsoft.Quantum.Canon.ApplyToTailCA)