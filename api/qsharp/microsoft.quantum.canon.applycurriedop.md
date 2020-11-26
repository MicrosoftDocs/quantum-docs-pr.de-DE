---
uid: Microsoft.Quantum.Canon.ApplyCurriedOp
title: Applycurriedop-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOp
qsharp.summary: ''
ms.openlocfilehash: ab652159fa64a95401d07998ed4aaae5c4dbb92e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219021"
---
# <a name="applycurriedop-operation"></a><span data-ttu-id="22726-102">Applycurriedop-Vorgang</span><span class="sxs-lookup"><span data-stu-id="22726-102">ApplyCurriedOp operation</span></span>

<span data-ttu-id="22726-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="22726-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="22726-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="22726-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="22726-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22726-105">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="22726-106">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="22726-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="first--t"></a><span data-ttu-id="22726-107">zuerst: 't</span><span class="sxs-lookup"><span data-stu-id="22726-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="22726-108">Zweitens: "U</span><span class="sxs-lookup"><span data-stu-id="22726-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="22726-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="22726-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="22726-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="22726-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="22726-111">GIF</span><span class="sxs-lookup"><span data-stu-id="22726-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="22726-112">"U</span><span class="sxs-lookup"><span data-stu-id="22726-112">'U</span></span>

