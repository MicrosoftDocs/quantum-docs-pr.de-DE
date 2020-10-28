---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualInPlace
title: Assertoperationsequalinplace-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Extensions.Testing
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  > [!WARNING]

  > AssertOperationsEqualInPlace has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.

  >

  > Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".

  > Note that the order of the arguments to this operation has changed.
ms.openlocfilehash: 6d2ead95a60ed3cc8ee95fb7f91e1aa49d366a48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702198"
---
# <a name="assertoperationsequalinplace-operation"></a>Assertoperationsequalinplace-Vorgang

Namespace: [Microsoft. Quantum. Extensions. testing](xref:Microsoft.Quantum.Extensions.Testing)

Paketen [](https://nuget.org/packages/)


> [!WARNING]
> Assertoperationsequalinplace ist veraltet. Verwenden Sie stattdessen <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace>.
>
> Verwenden Sie @"microsoft.quantum.diagnostics.assertoperationsequalinplace".
> Beachten Sie, dass sich die Reihenfolge der Argumente für diesen Vorgang geändert hat.



```qsharp
operation AssertOperationsEqualInPlace (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--qubit--unit"></a>tatsächlicher Wert: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="expected--qubit--unit-adj"></a>erwartet: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ




### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

