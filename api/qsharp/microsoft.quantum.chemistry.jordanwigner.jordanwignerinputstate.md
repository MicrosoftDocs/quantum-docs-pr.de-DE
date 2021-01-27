---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Benutzerdefinierter jordanwignerinputstate-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 18adf28b4e99c825f14e9271791ded069e687901
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837694"
---
# <a name="jordanwignerinputstate-user-defined-type"></a>Benutzerdefinierter jordanwignerinputstate-Typ

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Format der Daten, die von c# an Q # übergeben werden, um die Vorbereitung des Anfangs Zustands darzustellen. die Bedeutung der dargestellten Daten wird durch den Algorithmus bestimmt, der Sie empfängt.

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

