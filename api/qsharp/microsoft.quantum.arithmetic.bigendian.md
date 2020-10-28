---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Benutzerdefinierter bigEndian-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 64590606f7c36e0598a9d29c5c6a7ba6d6451aa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707434"
---
# <a name="bigendian-user-defined-type"></a><span data-ttu-id="b411b-102">Benutzerdefinierter bigEndian-Typ</span><span class="sxs-lookup"><span data-stu-id="b411b-102">BigEndian user defined type</span></span>

<span data-ttu-id="b411b-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b411b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b411b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b411b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b411b-105">Registrieren, das eine Ganzzahl ohne Vorzeichen in Big-d-Reihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="b411b-105">Register that encodes an unsigned integer in big-endian order.</span></span> <span data-ttu-id="b411b-106">Das Qubit mit Index `0` codiert das höchste Bit einer Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b411b-106">The qubit with index `0` encodes the highest bit of an unsigned integer.</span></span>

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="b411b-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b411b-107">Remarks</span></span>

<span data-ttu-id="b411b-108">Wir kürzen Sie `BigEndian` als `BE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b411b-108">We abbreviate `BigEndian` as `BE` in the documentation.</span></span>