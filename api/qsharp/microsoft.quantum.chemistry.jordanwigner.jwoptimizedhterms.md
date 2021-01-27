---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms
title: Jwoptimizedhterms-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JWOptimizedHTerms
qsharp.summary: Format of data passed from C# to Q# to represent terms of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 1588adc0edb95e347616dd6260200c09fee0f190
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837628"
---
# <a name="jwoptimizedhterms-user-defined-type"></a><span data-ttu-id="f9f4d-102">Jwoptimizedhterms-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="f9f4d-102">JWOptimizedHTerms user defined type</span></span>

<span data-ttu-id="f9f4d-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="f9f4d-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="f9f4d-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f9f4d-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f9f4d-105">Format der Daten, die von c# an Q # übergeben werden, um die Begriffe der hamiltonan darzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9f4d-105">Format of data passed from C# to Q# to represent terms of the Hamiltonian.</span></span>
<span data-ttu-id="f9f4d-106">Die Bedeutung der dargestellten Daten wird durch den Algorithmus bestimmt, der Sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="f9f4d-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JWOptimizedHTerms = (Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[]);
```

