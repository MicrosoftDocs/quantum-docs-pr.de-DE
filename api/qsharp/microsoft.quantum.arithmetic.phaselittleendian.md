---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Benutzerdefinierter Typ "phaselittleenddian"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: f1f792d62004a2765d4e63870f5a41a4377b0d34
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706351"
---
# <a name="phaselittleendian-user-defined-type"></a>Benutzerdefinierter Typ "phaselittleenddian"

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Little-in-tdian-Ganzzahlen ohne Vorzeichen in QFT.

Wenn z. b. $ \ket{x} $ die Little-Endian-Codierung der Ganzzahl $x $ auf Berechnungsbasis ist, dann ist $ \operatschmue{qftle} \ket{x} $ die Codierung von $x $ in der QFT-Basis.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Hinweise

Wir kürzen Sie `PhaseLittleEndian` als `PhaseLE` in der-Dokumentation.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. qft](xref:Microsoft.Quantum.Canon.QFT)
- [Microsoft. Quantum. Canon. qftle](xref:Microsoft.Quantum.Canon.QFTLE)