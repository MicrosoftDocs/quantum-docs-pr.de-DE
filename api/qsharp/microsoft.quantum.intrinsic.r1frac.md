---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: R1Frac-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfa6cd60eebd05feec8cfa2bf71e09dc0d02843a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707130"
---
# <a name="r1frac-operation"></a>R1Frac-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paketen [](https://nuget.org/packages/)


Wendet eine Drehung über den $ \ket {1} $-Zustand um einen als dyadic-Bruchteil angegebenen Winkel an.

\begin{align} R_1 (n, k) \mathrel{: =} \operatschmue{Diag} (1, e ^ {i \pi k/2 ^ n}).
\end{align}

> [!WARNING]
> Bei diesem Vorgang wird die **gegenüberliegende** Zeichen Konvention aus verwendet @"microsoft.quantum.intrinsic.r" , und der in enthaltene Faktor von $1/2 $ ist nicht enthalten @"microsoft.quantum.intrinsic.r1" .

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="numerator--int"></a>Zähler: [int](xref:microsoft.quantum.lang-ref.int)

Der Zähler in der dyadic-Bruch Darstellung des Winkels, um den das Qubit gedreht werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Potenz von zwei, die den Nenner des Winkels angibt, um den das Qubit gedreht werden soll.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, auf das das Gate angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Äquivalent zu:

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```