---
uid: Microsoft.Quantum.Intrinsic.Message
title: Message-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 4eb55dd4fd8d78e4b5a9bb289dacfbdb3aa4beb8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199011"
---
# <a name="message-function"></a>Message-Funktion

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Protokolliert eine Meldung.

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="msg--string"></a>msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Die Meldung, die gemeldet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Das spezifische Verhalten dieser Funktion ist simulatorabhängig, aber in den meisten Fällen wird die angegebene Nachricht in die Konsole geschrieben.