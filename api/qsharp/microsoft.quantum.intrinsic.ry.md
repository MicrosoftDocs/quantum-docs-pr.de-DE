---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Ry-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 9966693eb7283e855f7b72e910aa3604d6c2bd61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706535"
---
# <a name="ry-operation"></a>Ry-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paketen [](https://nuget.org/packages/)


Wendet eine Drehung zum $y $-Achse um einen angegebenen Winkel an.

\begin{align} R_y (\orta) \mathrel{: =} e ^ {-i \erta \ sigma_y/2} = \begin{bmatrix} \cos \bruchteil {\thta} {2} &-\sin \bruchteil {\thta} {2} \\ \\ \sin \bruchteil {\thta} {2} & \cos \bruchteil {\thta} {2} \end{bmatrix}.  
\end{align}

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="theta--double"></a>-Ta: [Double](xref:microsoft.quantum.lang-ref.double)

Der Winkel, um den das Qubit gedreht werden soll.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, auf das das Gate angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Äquivalent zu:

```qsharp
R(PauliY, theta, qubit);
```