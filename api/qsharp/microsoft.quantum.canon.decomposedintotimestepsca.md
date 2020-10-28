---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Debug-Funktion (Funktion)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: cfd563c1c6350255364de1e227442624acc98c22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704266"
---
# <a name="decomposedintotimestepsca-function"></a>Debug-Funktion (Funktion)

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt einen Vorgang zurück, der den Trotter – Suzuki Integrator für einen angegebenen Vorgang implementiert.

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="nsteps--int"></a>nsteps: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Vorgänge, die in Zeitschritten zerlegt werden sollen.


### <a name="op--intdoublet--unit-adj--ctl"></a>OP: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein Vorgang, bei dem eine Index Eingabe (Type `Int` ) und eine Zeiteingabe (Typ `Double` ) für die Zerlegung akzeptiert werden.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Wählt die Reihenfolge des zu verwendenden Trotter – Suzuki Integrator aus.
Bestellung 1 und sogar Orders 2, 4, 6,... werden zurzeit unterstützt.



## <a name="output--doublet--unit-adj--ctl"></a>Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Gibt eine einheitliche-Klasse zurück, die den Trotter – Suzuki Integrator implementiert, wobei der erste Parameter `Double` die Größe des Integrations Schritts ist und der zweite Parameter das Ziel ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ, auf den jeder Zeit Schritt reagieren soll. in der Regel entweder `Qubit[]` oder `Qubit` .

## <a name="remarks"></a>Hinweise

Wenn `order` Diese Funktion mit gleich `1` ist, gibt diese Funktion einen Vorgang zurück, der durch die niedrigste Reihenfolge (Trotter – Suzuki Integrator $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}) simuliert werden kann. \end{align} $ $, wobei die Notation von [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) befolgt wurde und $ \lambda $ die Entwicklungszeit (dargestellt durch die erste Eingabe der zurückgegebenen Operation) ist. und lassen Sie $ \{ H_j \} _ {j = 1} ^ {m} $ den Satz der (Schiefe-hermitian) Dynamical-Generatoren aufweisen, die integriert werden, sodass `op(j, lambda, _)` vom einheitlichen Operator $e ^ {H_j \lambda} $ simuliert wird.

Ebenso gibt ein `order` von `2` den symmetrischen Trotter der zweiten Ordnung zurück – Suzuki Integrator $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.
\end{align} $ $

Höhere gerade Werte von `order` werden mithilfe der rekursiven Konstruktion von [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139)implementiert.

## <a name="references"></a>Referenzen

- [*D. W. Beeren, G. ahukas, R. Cleve, B. C. Sanders*](https://arxiv.org/abs/quant-ph/0508139)