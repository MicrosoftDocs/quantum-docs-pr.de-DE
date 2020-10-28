---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: Blochspherekoordinaten-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 6614b78c8e64c205cc94052cc64dd957814ab3d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724081"
---
# <a name="blochspherecoordinates-function"></a>Blochspherekoordinaten-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Berechnet die Bloch-Kugel Koordinaten für einen Single-Qubit-Zustand.

Wenn zwei komplexe Zahlen $a 0 sind, a1 $, die den Qubit-Status darstellen, berechnet Koordinaten auf der Bloch-Kugel, sodass $a 0 \ket {0} + a1 \ket {1} = r e ^ {IT} (e ^ {-i \phi/2}\cos{(\ der TA/2)} \ket {0} + e ^ {i \phi/2}\sin{(\-Ta/2)} \ket {1} ) $.

```qsharp
function BlochSphereCoordinates (a0 : Microsoft.Quantum.Math.ComplexPolar, a1 : Microsoft.Quantum.Math.ComplexPolar) : (Microsoft.Quantum.Math.ComplexPolar, Double, Double)
```


## <a name="input"></a>Eingabe

### <a name="a0--complexpolar"></a>a0: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Komplexer Koeffizient des Zustands $ \ket {0} $.


### <a name="a1--complexpolar"></a>a1: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Komplexer Koeffizient des Zustands $ \ket {1} $.



## <a name="output--complexpolardoubledouble"></a>Ausgabe: ([complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar),[Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))

Ein Tupel, das enthält `(ComplexPolar(r, t), phi, theta)` .