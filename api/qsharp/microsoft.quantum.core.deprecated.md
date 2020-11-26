---
uid: Microsoft.Quantum.Core.Deprecated
title: Als veraltet definierter benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 122cbc113a68cec107558d68a6fb145cf6bbd9db
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224087"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="c53bb-102">Als veraltet definierter benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="c53bb-102">Deprecated user defined type</span></span>

<span data-ttu-id="c53bb-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="c53bb-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="c53bb-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c53bb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c53bb-105">Vom Compiler erkanntes Attribut, das verwendet wird, um einen Typ zu kennzeichnen oder als veraltet zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="c53bb-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="c53bb-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="c53bb-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="c53bb-107">Newname: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c53bb-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c53bb-108">Der vollständige Name des Typs oder der Aufruf baren, der stattdessen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c53bb-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="c53bb-109">Wird auf die leere Zeichenfolge festgelegt, wenn ein Typ oder Aufruf Bare Zeichenfolge ohne Ersetzung veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="c53bb-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>