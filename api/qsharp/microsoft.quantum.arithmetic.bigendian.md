---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Benutzerdefinierter bigEndian-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 8ea1aefa46a7224ef199baf68f2d6ab2d563e3a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223662"
---
# <a name="bigendian-user-defined-type"></a><span data-ttu-id="55400-102">Benutzerdefinierter bigEndian-Typ</span><span class="sxs-lookup"><span data-stu-id="55400-102">BigEndian user defined type</span></span>

<span data-ttu-id="55400-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="55400-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="55400-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="55400-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="55400-105">Registrieren, das eine Ganzzahl ohne Vorzeichen in Big-d-Reihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="55400-105">Register that encodes an unsigned integer in big-endian order.</span></span> <span data-ttu-id="55400-106">Das Qubit mit Index `0` codiert das höchste Bit einer Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="55400-106">The qubit with index `0` encodes the highest bit of an unsigned integer.</span></span>

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="55400-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55400-107">Remarks</span></span>

<span data-ttu-id="55400-108">Wir kürzen Sie `BigEndian` als `BE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="55400-108">We abbreviate `BigEndian` as `BE` in the documentation.</span></span>