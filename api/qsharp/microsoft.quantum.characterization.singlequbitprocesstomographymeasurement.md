---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Singlequbitprocesstomographymeasurement-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 883b98ad4f2d0ac4a02e55e444c04e8e7cf37af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839654"
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