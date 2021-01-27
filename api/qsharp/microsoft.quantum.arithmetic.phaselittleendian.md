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
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="18329-102">Benutzerdefinierter Typ "phaselittleenddian"</span><span class="sxs-lookup"><span data-stu-id="18329-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="18329-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="18329-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="18329-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="18329-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="18329-105">Little-in-tdian-Ganzzahlen ohne Vorzeichen in QFT.</span><span class="sxs-lookup"><span data-stu-id="18329-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="18329-106">Wenn z. b. $ \ket{x} $ die Little-Endian-Codierung der Ganzzahl $x $ auf Berechnungsbasis ist, dann ist $ \operatschmue{qftle} \ket{x} $ die Codierung von $x $ in der QFT-Basis.</span><span class="sxs-lookup"><span data-stu-id="18329-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="18329-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18329-107">Remarks</span></span>

<span data-ttu-id="18329-108">Wir kürzen Sie `PhaseLittleEndian` als `PhaseLE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="18329-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="18329-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18329-109">See Also</span></span>

- [<span data-ttu-id="18329-110">Microsoft. Quantum. Canon. qft</span><span class="sxs-lookup"><span data-stu-id="18329-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="18329-111">Microsoft. Quantum. Canon. qftle</span><span class="sxs-lookup"><span data-stu-id="18329-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)