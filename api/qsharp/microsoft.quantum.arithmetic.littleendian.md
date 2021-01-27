---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Benutzerdefinierter Typ "littleenddian"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 12bc4dbf830e426365545826575d66a9683cb694
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846567"
---
# <a name="littleendian-user-defined-type"></a><span data-ttu-id="b5dcf-102">Benutzerdefinierter Typ "littleenddian"</span><span class="sxs-lookup"><span data-stu-id="b5dcf-102">LittleEndian user defined type</span></span>

<span data-ttu-id="b5dcf-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b5dcf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b5dcf-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b5dcf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b5dcf-105">Registrieren, das eine Ganzzahl ohne Vorzeichen in Little-in-der-Reihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="b5dcf-105">Register that encodes an unsigned integer in little-endian order.</span></span> <span data-ttu-id="b5dcf-106">Das Qubit mit Index `0` codiert das niedrigste Bit einer Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b5dcf-106">The qubit with index `0` encodes the lowest bit of an unsigned integer.</span></span>

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="b5dcf-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5dcf-107">Remarks</span></span>

<span data-ttu-id="b5dcf-108">Wir kürzen Sie `LittleEndian` als `LE` in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b5dcf-108">We abbreviate `LittleEndian` as `LE` in the documentation.</span></span>