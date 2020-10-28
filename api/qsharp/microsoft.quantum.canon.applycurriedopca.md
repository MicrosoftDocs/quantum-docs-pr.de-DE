---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpCA
title: Applycurriedopca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpCA
qsharp.summary: ''
ms.openlocfilehash: 4e57772bc5440a473c28279ac125170caaa120f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705407"
---
# <a name="applycurriedopca-operation"></a><span data-ttu-id="3a5a6-102">Applycurriedopca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3a5a6-102">ApplyCurriedOpCA operation</span></span>

<span data-ttu-id="3a5a6-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3a5a6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3a5a6-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3a5a6-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyCurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="3a5a6-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3a5a6-105">Input</span></span>

### <a name="curriedop--t---u--unit-ctl--adj"></a><span data-ttu-id="3a5a6-106">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="3a5a6-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="first--t"></a><span data-ttu-id="3a5a6-107">zuerst: 't</span><span class="sxs-lookup"><span data-stu-id="3a5a6-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="3a5a6-108">Zweitens: "U</span><span class="sxs-lookup"><span data-stu-id="3a5a6-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="3a5a6-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3a5a6-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3a5a6-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3a5a6-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3a5a6-111">GIF</span><span class="sxs-lookup"><span data-stu-id="3a5a6-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="3a5a6-112">"U</span><span class="sxs-lookup"><span data-stu-id="3a5a6-112">'U</span></span>

