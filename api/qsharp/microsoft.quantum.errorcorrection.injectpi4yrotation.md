---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: InjectPi4YRotation-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 4ff0abe67a6d18204e417a45f8d8f1d092d02b88
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200797"
---
# <a name="injectpi4yrotation-operation"></a>InjectPi4YRotation-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dreht ein einzelnes Qubit um die Y-Achse.

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a>BESCHREIBUNG

Führt eine Drehung/4-Drehung um durch `Y` .

Die Drehung erfolgt durch die Verwendung eines magischen Zustands. Das heißt, eine Kopie des Zustands $ $ \begin{align} \cos\bruchteil {\pi} {8} \ket {0} + \sin \bruchteil {\pi} {8} \ket {1} .
\end{align} $ $

## <a name="input"></a>Eingabe

### <a name="data--qubit"></a>Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, das um $Y $ um $ \pi/$4 gedreht werden soll.


### <a name="magic--qubit"></a>Magic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, das sich anfänglich im Magic-Zustand befindet. Die folgende Anwendung dieses Vorgangs `magic` wird an den Status "$ \ket $" zurückgegeben {0} .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
Ry(PI() / 4.0, data);
```

and

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

Dieser Vorgang unterstützt das `Adjoint` Funktor. in diesem Fall wird derselbe magische Zustand verwendet, aber die Auswirkung auf das Daten-Qubit ist eine $-\ pi/4 $ $Y $-Rotation.