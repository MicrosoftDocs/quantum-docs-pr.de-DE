---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Debug-Funktion (Funktion)
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: e82df36d2e4f3767a152d5c92d7b1897c744a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840685"
---
# <a name="decomposedintotimestepsca-function"></a>Debug-Funktion (Funktion)

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen Vorgang zurück, der den Trotter – Suzuki Integrator für einen angegebenen Vorgang implementiert.

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="nsteps--int"></a>nsteps: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.


### <a name="op--intdoublet--unit--is-adj--ctl"></a>OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ `Double` ) für die Zerlegung akzeptiert werden.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Wählt die Reihenfolge des zu verwendenden Trotter – Suzuki Integrator aus.
Bestellung 1 und sogar Orders 2, 4, 6,... werden zurzeit unterstützt.



## <a name="output--doublet--unit--is-adj--ctl"></a>Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Gibt eine einheitliche-Klasse zurück, die den Trotter – Suzuki Integrator implementiert, wobei der erste Parameter `Double` die Größe des Integrations Schritts ist und der zweite Parameter das Ziel ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .

## <a name="remarks"></a>Bemerkungen

Wenn `order` Diese Funktion mit gleich `1` ist, gibt diese Funktion einen Vorgang zurück, der durch die niedrigste Reihenfolge (Trotter – Suzuki Integrator $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}) simuliert werden kann. \end{align} $ $, wobei die Notation von [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) befolgt wurde und $ \lambda $ die Entwicklungszeit (dargestellt durch die erste Eingabe der zurückgegebenen Operation) ist. und lassen Sie $ \{ H_j \} _ {j = 1} ^ {m} $ den Satz der (Schiefe-hermitian) Dynamical-Generatoren aufweisen, die integriert werden, sodass `op(j, lambda, _)` vom einheitlichen Operator $e ^ {H_j \lambda} $ simuliert wird.

Ebenso gibt ein `order` von `2` den symmetrischen Trotter der zweiten Ordnung zurück – Suzuki Integrator $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.
\end{align} $ $

Höhere gerade Werte von `order` werden mithilfe der rekursiven Konstruktion von [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139)implementiert.

## <a name="references"></a>References

- [*D. W. Beeren, G. ahukas, R. Cleve, B. C. Sanders*](https://arxiv.org/abs/quant-ph/0508139)