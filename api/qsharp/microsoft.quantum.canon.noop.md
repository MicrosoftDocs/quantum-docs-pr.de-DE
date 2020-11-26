---
uid: Microsoft.Quantum.Canon.NoOp
title: NOOP-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 35b6b62cab35f941f04b150dcca763457ddaa084
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205965"
---
# <a name="noop-operation"></a>NOOP-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Führt den Identitäts Vorgang (No-OP) für ein Argument aus.

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Bei diesem Vorgang wird ein beliebiger Typ verwendet, und es wird keine Aktion ausgeführt.
Dies kann hilfreich sein, wenn eine Eingabe eines Vorgangs Typs erwartet wird, aber keine Aktion ausgeführt werden soll.
Wenn beispielsweise ein bestimmtes Fehlerkorrektur-Syndrom anzeigt, dass kein Fehler aufgetreten ist, ist `NoOp<Qubit[]>` möglicherweise die richtige Wiederherstellungs Prozedur.
Ebenso kann, wenn ein Vorgang ein Zustands Vorbereitungsverfahren erwartet, als Eingabe `NoOp<Qubit[]>` verwendet werden, um den Status $ \ket{0 \cdots 0} $ vorzubereiten.

## <a name="input"></a>Eingabe

### <a name="input--t"></a>Eingabe: 't

Ein Wert, der ignoriert werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

In fast allen Fällen muss der Typparameter für `NoOp` explizit angegeben werden. Beispielsweise `NoOp<Qubit>` ist identisch mit <xref:microsoft.quantum.intrinsic.i> .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. intrinsisch. I](xref:Microsoft.Quantum.Intrinsic.I)