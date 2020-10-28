---
uid: Microsoft.Quantum.Core.Deprecated
title: Als veraltet definierter benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: b1fcae9647b2a655d25773386ecffa826515516e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702882"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="a60ea-102">Als veraltet definierter benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="a60ea-102">Deprecated user defined type</span></span>

<span data-ttu-id="a60ea-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="a60ea-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="a60ea-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a60ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a60ea-105">Vom Compiler erkanntes Attribut, das verwendet wird, um einen Typ zu kennzeichnen oder als veraltet zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="a60ea-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="a60ea-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="a60ea-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="a60ea-107">Newname: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a60ea-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a60ea-108">Der vollständige Name des Typs oder der Aufruf baren, der stattdessen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a60ea-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="a60ea-109">Wird auf die leere Zeichenfolge festgelegt, wenn ein Typ oder Aufruf Bare Zeichenfolge ohne Ersetzung veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a60ea-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>