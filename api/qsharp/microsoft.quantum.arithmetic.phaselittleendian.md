---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Benutzerdefinierter Typ "phaselittleenddian"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 59df1db31090f875ccd261fe6cc43995ba57b963
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842997"
---
# <a name="phaselittleendian-user-defined-type"></a>Benutzerdefinierter Typ "phaselittleenddian"

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Little-in-tdian-Ganzzahlen ohne Vorzeichen in QFT.

Wenn z. b. $ \ket{x} $ die Little-Endian-Codierung der Ganzzahl $x $ auf Berechnungsbasis ist, dann ist $ \operatschmue{qftle} \ket{x} $ die Codierung von $x $ in der QFT-Basis.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Bemerkungen

Wir kürzen Sie `PhaseLittleEndian` als `PhaseLE` in der-Dokumentation.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. qft](xref:Microsoft.Quantum.Canon.QFT)
- [Microsoft. Quantum. Canon. qftle](xref:Microsoft.Quantum.Canon.QFTLE)