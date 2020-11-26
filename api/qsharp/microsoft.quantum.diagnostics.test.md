---
uid: Microsoft.Quantum.Diagnostics.Test
title: Benutzerdefinierten Typ testen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 80821cb46d773d84085838d9ee539a8a45c43e61
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201494"
---
# <a name="test-user-defined-type"></a>Benutzerdefinierten Typ testen

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Vom Compiler erkanntes Attribut, das zum Markieren eines Komponententests verwendet wird.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Test = (ExecutionTarget : String);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="executiontarget--string"></a>Executiontarget: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

