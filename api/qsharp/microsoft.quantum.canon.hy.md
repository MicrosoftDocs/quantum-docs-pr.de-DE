---
uid: Microsoft.Quantum.Canon.HY
title: HY-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: HY
qsharp.summary: >-
  Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.

  The Y Hadamard transformation $H_Y = S H$ on a single qubit is:

  \begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}. \end{align}
ms.openlocfilehash: 119d78c4cd8d5e5d92cb54ff652b082a1b99ae06
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840439"
---
# <a name="hy-operation"></a>HY-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet die y-Basis-analog auf die Hadamard-Transformation an, die die Z-und Y-Achse interändert.

Die Y Hadamard-Transformation $H _Y = S H $ für ein einzelnes Qubit ist:

\begin{align} H_Y \mathrel{: =} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ i &-i \end{bmatrix}.
\end{align}

```qsharp
operation HY (target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, auf das das Gate angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. intrinsisch. H](xref:Microsoft.Quantum.Intrinsic.H)