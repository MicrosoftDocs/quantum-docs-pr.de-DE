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
# <a name="deprecated-user-defined-type"></a>Als veraltet definierter benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Vom Compiler erkanntes Attribut, das verwendet wird, um einen Typ zu kennzeichnen oder als veraltet zu kennzeichnen.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Deprecated = (NewName : String);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="newname--string"></a>Newname: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Der vollständige Name des Typs oder der Aufruf baren, der stattdessen verwendet werden soll.
Wird auf die leere Zeichenfolge festgelegt, wenn ein Typ oder Aufruf Bare Zeichenfolge ohne Ersetzung veraltet ist.