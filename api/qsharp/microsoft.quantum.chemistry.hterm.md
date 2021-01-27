---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Benutzerdefinierter hterm-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 744668a4fe96ee00fe2f7991f4e1f05eea19d417
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851791"
---
# <a name="hterm-user-defined-type"></a><span data-ttu-id="82807-102">Benutzerdefinierter hterm-Typ</span><span class="sxs-lookup"><span data-stu-id="82807-102">HTerm user defined type</span></span>

<span data-ttu-id="82807-103">Namespace: [Microsoft. Quantum. Chemistry](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="82807-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="82807-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="82807-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="82807-105">Das Format der Daten, die von c# an Q # übergeben werden, um einen Begriff von "hamiltonan" darzustellen.</span><span class="sxs-lookup"><span data-stu-id="82807-105">Format of data passed from C# to Q# to represent a term of the Hamiltonian.</span></span>
<span data-ttu-id="82807-106">Die Bedeutung der dargestellten Daten wird durch den Algorithmus bestimmt, der Sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="82807-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype HTerm = (Int[], Double[]);
```

