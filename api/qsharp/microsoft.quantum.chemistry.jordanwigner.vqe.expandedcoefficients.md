---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Expandebug-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835623"
---
# <a name="expandedcoefficients-function"></a>Expandebug-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Erweitert die kompakte Darstellung der Jordan-Wigner Koeffizienten, um eine eins-zu-Eins-Zuordnung zwischen diesen und den Pauli-Begriffen zu erhalten.

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a>Eingabe

### <a name="coeff--double"></a>coeff: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Koeffizienten, das aus der Jordan-Wigner hamiltonan-Datenstruktur gelesen wird.


### <a name="termtype--int"></a>Termtype: [int](xref:microsoft.quantum.lang-ref.int)

Der Typ des Jordan-Wigner Begriffs.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]

Erweiterte Arrays von Koeffizienten, 1 pro Pauli-Begriff.