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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="edd6d-102">Benutzerdefinierter Typ "phaselittleenddian"</span><span class="sxs-lookup"><span data-stu-id="edd6d-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="edd6d-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="edd6d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="edd6d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="edd6d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="edd6d-105">Little-in-tdian-Ganzzahlen ohne Vorzeichen in QFT.</span><span class="sxs-lookup"><span data-stu-id="edd6d-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="edd6d-106">Wenn z. b. $ \ket{x} $ die Little-Endian-Codierung der Ganzzahl $x $ auf Berechnungsbasis ist, dann ist $ \operatschmue{qftle} \ket{x} $ die Codierung von $x $ in der QFT-Basis.</span><span class="sxs-lookup"><span data-stu-id="edd6d-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="edd6d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edd6d-107">Remarks</span></span>

<span data-ttu-id="edd6d-108">Wir kürzen Sie `PhaseLittleEndian` als `PhaseLE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="edd6d-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="edd6d-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="edd6d-109">See Also</span></span>

- [<span data-ttu-id="edd6d-110">Microsoft. Quantum. Canon. qft</span><span class="sxs-lookup"><span data-stu-id="edd6d-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="edd6d-111">Microsoft. Quantum. Canon. qftle</span><span class="sxs-lookup"><span data-stu-id="edd6d-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)