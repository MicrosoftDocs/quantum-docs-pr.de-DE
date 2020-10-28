---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Expandebug-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 8f5a2319b5839d0d9e47972389330dc16dffcaf0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703073"
---
# <a name="expandedcoefficients-function"></a>Expandebug-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paketen [](https://nuget.org/packages/)


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