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
# <a name="jordanwignerinputstate-user-defined-type"></a><span data-ttu-id="b40dd-102">Benutzerdefinierter jordanwignerinputstate-Typ</span><span class="sxs-lookup"><span data-stu-id="b40dd-102">JordanWignerInputState user defined type</span></span>

<span data-ttu-id="b40dd-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="b40dd-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="b40dd-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="b40dd-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="b40dd-105">Format der Daten, die von c# an Q # übergeben werden, um die Vorbereitung des Anfangs Zustands darzustellen. die Bedeutung der dargestellten Daten wird durch den Algorithmus bestimmt, der Sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="b40dd-105">Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

