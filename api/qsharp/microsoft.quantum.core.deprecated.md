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
# <a name="deprecated-user-defined-type"></a>Als veraltet definierter benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paketen [](https://nuget.org/packages/)


Vom Compiler erkanntes Attribut, das verwendet wird, um einen Typ zu kennzeichnen oder als veraltet zu kennzeichnen.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="newname--string"></a>Newname: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Der vollständige Name des Typs oder der Aufruf baren, der stattdessen verwendet werden soll.
Wird auf die leere Zeichenfolge festgelegt, wenn ein Typ oder Aufruf Bare Zeichenfolge ohne Ersetzung veraltet ist.