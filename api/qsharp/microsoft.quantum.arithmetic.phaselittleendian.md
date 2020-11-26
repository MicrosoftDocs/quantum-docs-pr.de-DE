---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: Benutzerdefinierter Typ "phaselittleenddian"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 45b824a74d664df0d5707264a3c616fb27c477b3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222421"
---
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="83b35-102">Benutzerdefinierter Typ "phaselittleenddian"</span><span class="sxs-lookup"><span data-stu-id="83b35-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="83b35-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="83b35-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="83b35-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="83b35-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="83b35-105">Little-in-tdian-Ganzzahlen ohne Vorzeichen in QFT.</span><span class="sxs-lookup"><span data-stu-id="83b35-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="83b35-106">Wenn z. b. $ \ket{x} $ die Little-Endian-Codierung der Ganzzahl $x $ auf Berechnungsbasis ist, dann ist $ \operatschmue{qftle} \ket{x} $ die Codierung von $x $ in der QFT-Basis.</span><span class="sxs-lookup"><span data-stu-id="83b35-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="83b35-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83b35-107">Remarks</span></span>

<span data-ttu-id="83b35-108">Wir kürzen Sie `PhaseLittleEndian` als `PhaseLE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="83b35-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="83b35-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83b35-109">See Also</span></span>

- [<span data-ttu-id="83b35-110">Microsoft. Quantum. Canon. qft</span><span class="sxs-lookup"><span data-stu-id="83b35-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="83b35-111">Microsoft. Quantum. Canon. qftle</span><span class="sxs-lookup"><span data-stu-id="83b35-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)