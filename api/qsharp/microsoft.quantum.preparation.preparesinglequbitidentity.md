---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Preparesinglequbitidentity-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: 12a650568aa5682e8fb6498808d188b154527acb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724880"
---
# <a name="preparesinglequbitidentity-operation"></a>Preparesinglequbitidentity-Vorgang

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Bereitet ein Qubit im maximale gemischten Zustand vor.

Sie bereitet das angegebene Qubit im Zustand "$ \boldone/$2" vor, indem der%% amp; quot;%% amp; quot;%% amp; quot; \omega (\rho) \mathrel{: =} \frac {1} {4} \ sum_ {\mu \ auf 0 festgelegt \{ wird. 1, 2, 3 \} } \sigma \_ {\mu} \rho \sigma \_ {\mu} ^ {\dagger}, \end{align} $ $, wobei $ \sigma \_ i $ der $i $ th-Pauli-Operator ist und $ \rho $ ein Dichte Operator ist, der einen gemischten Zustand darstellt.

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, dessen Zustand in der oben beschriebenen Weise depolarisiert werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Der gemischte Status $ \boldone/$2, der das Ergebnis der Anwendung dieses Vorgangs auf einen Zustand beschreibt, beschreibt implizit einen Erwartungswert gegenüber zufälligen Entscheidungen, die in diesem Vorgang vorgenommen werden.
Folglich ordnet dieser Vorgang für jede einzelne Anwendung reine Zustände reinen Zuständen zu, aber Sie verhält sich wie erwartet.
Insbesondere kann dieser Vorgang in der Prozess Tomographie zum Messen der *nicht unitalen* Komponenten eines Kanals verwendet werden.