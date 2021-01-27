---
uid: Microsoft.Quantum.Core.Deprecated
title: Als veraltet definierter benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: Deprecated
qsharp.summary: Compiler-recognized attribute used to mark a type or callable as deprecated.
ms.openlocfilehash: 1a32d98f5d034c2673d42301b45379da1302ca7f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832085"
---
# <a name="deprecated-user-defined-type"></a><span data-ttu-id="47613-102">Als veraltet definierter benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="47613-102">Deprecated user defined type</span></span>

<span data-ttu-id="47613-103">Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="47613-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="47613-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="47613-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="47613-105">Vom Compiler erkanntes Attribut, das verwendet wird, um einen Typ zu kennzeichnen oder als veraltet zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="47613-105">Compiler-recognized attribute used to mark a type or callable as deprecated.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a><span data-ttu-id="47613-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="47613-106">Named Items</span></span>

### <a name="newname--string"></a><span data-ttu-id="47613-107">Newname: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="47613-107">NewName : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="47613-108">Der vollständige Name des Typs oder der Aufruf baren, der stattdessen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47613-108">The full name of the type or callable to use instead.</span></span>
<span data-ttu-id="47613-109">Wird auf die leere Zeichenfolge festgelegt, wenn ein Typ oder Aufruf Bare Zeichenfolge ohne Ersetzung veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="47613-109">Is set to the empty String if a type or callable has been deprecated without substitution.</span></span>