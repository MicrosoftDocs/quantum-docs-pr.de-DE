---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: Benutzerdefinierter Typ "Requirements scapability"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 5e0db49d6f73398ac36003eb0f44e3a6520b7f1e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855152"
---
# <a name="requirescapability-user-defined-type"></a>Benutzerdefinierter Typ "Requirements scapability"

Namespace: [Microsoft. Quantum. Targeting](xref:Microsoft.Quantum.Targeting)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Vom Compiler erkanntes Attribut, das verwendet wird, um eine Aufruf Bare mit den erforderlichen Lauf Zeitfunktionen zu markieren.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="level--string"></a>Ebene: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Der Name der Lauf Zeit Funktionsebene, die für die Aufruf Bare-Funktion erforderlich ist.
### <a name="reason--string"></a>Ursache: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Beschreibung, warum die Aufruf Bare Funktion diese Lauf Zeitfunktion erfordert.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird automatisch aufrufen durch den Compiler hinzugefügt, es sei denn, es ist bereits eine Instanz dieses Attributs für die Aufruf Bare Instanz vorhanden. Es sollte nicht verwendet werden, außer in seltenen Fällen, in denen der Compiler die erforderliche Funktion nicht ordnungsgemäß ableiten kann.

Im folgenden finden Sie eine Liste der Funktionsebenen, in der Reihenfolge, in der die Funktionen erhöht werden, oder zum verringern

## `"BasicQuantumFunctionality"`

Die Messergebnisse können nicht auf Gleichheit verglichen werden.

## `"BasicMeasurementFeedback"`

Messergebnisse können nur bei bedingten Ausdrücken der if-Anweisung in-Vorgängen auf Gleichheit verglichen werden. Der-Block einer if-Anweisung, die von einem Ergebnis abhängt, kann keine Set-Anweisungen für änderbare Variablen enthalten, die außerhalb des-Blocks deklariert werden, oder Return-Anweisungen.

## `"FullComputation"`

Keine Lauf Zeiteinschränkungen. Alle f #-Programme können ausgeführt werden.