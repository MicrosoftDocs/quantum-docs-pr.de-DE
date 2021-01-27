---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Benutzerdefinierter bigEndian-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843390"
---
# <a name="bigendian-user-defined-type"></a><span data-ttu-id="5869e-102">Benutzerdefinierter bigEndian-Typ</span><span class="sxs-lookup"><span data-stu-id="5869e-102">BigEndian user defined type</span></span>

<span data-ttu-id="5869e-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5869e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5869e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5869e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5869e-105">Registrieren, das eine Ganzzahl ohne Vorzeichen in Big-d-Reihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="5869e-105">Register that encodes an unsigned integer in big-endian order.</span></span> <span data-ttu-id="5869e-106">Das Qubit mit Index `0` codiert das höchste Bit einer Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5869e-106">The qubit with index `0` encodes the highest bit of an unsigned integer.</span></span>

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="5869e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5869e-107">Remarks</span></span>

<span data-ttu-id="5869e-108">Wir kürzen Sie `BigEndian` als `BE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="5869e-108">We abbreviate `BigEndian` as `BE` in the documentation.</span></span>