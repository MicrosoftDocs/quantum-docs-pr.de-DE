---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Complexpolar-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701328"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="8173f-102">Complexpolar-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="8173f-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="8173f-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8173f-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8173f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8173f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8173f-105">Stellt eine komplexe Zahl in Polar Form dar.</span><span class="sxs-lookup"><span data-stu-id="8173f-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="8173f-106">Die Polar Darstellung einer komplexen Zahl ist $c = r e ^ {i t} $.</span><span class="sxs-lookup"><span data-stu-id="8173f-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="8173f-107">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="8173f-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="8173f-108">Größe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8173f-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8173f-109">Der absolute Wert $r \ge $0 von $c $.</span><span class="sxs-lookup"><span data-stu-id="8173f-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="8173f-110">Argument: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8173f-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8173f-111">Die Phase $t \in \mathbb R $ von $c $.</span><span class="sxs-lookup"><span data-stu-id="8173f-111">The phase $t \in \mathbb R$ of $c$.</span></span>