---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualReferenced
title: Assertoperationsequalreferenzierter Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Extensions.Testing
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  > [!WARNING]

  > AssertOperationsEqualReferenced has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced> instead.

  >

  > Please use @"microsoft.quantum.diagnostics.assertoperationsequalreferenced".

  > Note that the order of the arguments to this operation has changed.
ms.openlocfilehash: 2d39f74c68e48d2f2b8003b76885c9444056f8d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702174"
---
# <a name="assertoperationsequalreferenced-operation"></a>Assertoperationsequalreferenzierter Vorgang

Namespace: [Microsoft. Quantum. Extensions. testing](xref:Microsoft.Quantum.Extensions.Testing)

Paketen [](https://nuget.org/packages/)


> [!WARNING]
> Assertoperationsequalreferenziert ist veraltet. Verwenden Sie stattdessen <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced>.
>
> Verwenden Sie @"microsoft.quantum.diagnostics.assertoperationsequalreferenced".
> Beachten Sie, dass sich die Reihenfolge der Argumente für diesen Vorgang geändert hat.



```qsharp
operation AssertOperationsEqualReferenced (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a>Eingabe

### <a name="actual--qubit--unit"></a>tatsächlicher Wert: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="expected--qubit--unit-adj"></a>erwartet: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ




### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

