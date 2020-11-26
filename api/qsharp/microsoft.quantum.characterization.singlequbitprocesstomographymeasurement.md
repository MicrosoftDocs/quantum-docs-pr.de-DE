---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Singlequbitprocesstomographymeasurement-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 3756040df8e34ecee1e968428b08387e0096ab7b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204197"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a>Singlequbitprocesstomographymeasurement-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt eine Single-Qubit-Prozess-Tomographie-Messung auf der Grundlage eines bestimmten relevanten Kanals aus.

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a>Eingabe

### <a name="preparation--pauli"></a>Vorbereitung: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Das Pauli-Basiselement $P $, in dem ein Qubit vorbereitet werden soll.


### <a name="measurement--pauli"></a>Messung: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Das Pauli-Basiselement $Q $, in dem ein Qubit gemessen werden soll.


### <a name="channel--qubit--unit"></a>Channel: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein einzelner Qubit-Kanal $ \lambda $, dessen Verhalten mit der Prozess Tomographie geschätzt wird.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis `Zero` mit der Wahrscheinlichkeit $ $ \begin{align} \pr (\texttt{Zero} | \lambda; P, Q) = \operatorname{TR}\left (\bruch {\boldone + Q} {2} \lambda\left [\bruchteil {\boldone + P} {2} \right] \right).
\end{align} $ $

## <a name="remarks"></a>Bemerkungen

Die Verteilung der Ergebnisse, die von diesem Vorgang zurückgegeben werden, ist ein Sonderfall von zwei-Qubit-Zustands-Tomographie. Let $ \rho = J (\lambda)/$2 ist der Bundesstaat Choi – jamiłkowski für $ \lambda $. Anschließend ist die obige Verteilung mit $ $ \begin{align} \pr (\texttt{Zero} | \rho;) identisch. M) = \operatorname{TR} (m \rho), \end{align} $ $ WHERE $M = 2 (\boldone + P) ^ \mathrm{t}/2 \cdot (\boldone + Q)/$2 ist das effektive Maß, das $P $ und $Q $ entspricht.