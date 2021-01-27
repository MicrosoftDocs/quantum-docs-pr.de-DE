---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Assertoperationsequalreferenzierter Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 045f00a720e9f4d2e6993c66ace44a81e192ff30
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853463"
---
# <a name="assertoperationsequalreferenced-operation"></a>Assertoperationsequalreferenzierter Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Bei zwei Vorgängen wird von bestätigt, dass Sie für alle Eingabe Zustände identisch agieren.

Diese Assertionen werden mithilfe von "Choi – jamiołkowski" (isomorphism) implementiert, um die Behauptung auf eine der Qubit-Zustands Assertionen für zwei entkoppelt-Register zu reduzieren.
Folglich benötigt dieser Vorgang nur einen einzelnen Vorgang für jeden zu testenden Vorgang, erfordert jedoch doppelt so viele Qubits, die zugewiesen werden müssen.
Diese Assertion kann beispielsweise verwendet werden, um sicherzustellen, dass eine optimierte Version eines Vorgangs identisch mit der naive Implementierung verhält oder dass ein Vorgang, der für einen Bereich von nicht-Quantum-Eingaben agiert, mit bekannten Fällen übereinstimmt.

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl von Qubits, die an jeden Vorgang übergeben werden sollen.


### <a name="actual--qubit--unit"></a>tatsächlicher Wert: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Zu testender Vorgang.


### <a name="expected--qubit--unit--is-adj"></a>erwartet: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Vorgang, der das erwartete Verhalten für den zu testenden Vorgang definiert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Dieser Vorgang erfordert, dass der Vorgang, der das erwartete Verhalten modelliert, adjointable ist, sodass die Umkehrung nur für das Ziel Register ausgeführt werden kann.
Formal kann ein Vorgang zum Austauschen angegeben werden, der diese Anforderung lockert, aber der Vorgang zum Austauschen ist nicht im allgemeinen physisch für beliebige Quantum-Vorgänge physisch realisierbar und daher hier nicht als Option enthalten.