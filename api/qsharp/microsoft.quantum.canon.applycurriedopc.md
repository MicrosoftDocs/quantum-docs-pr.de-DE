---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: Applycurriedopc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: 65e861914b57cf8a32f2321f881248830b72c54e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841905"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="0f990-102">Applycurriedopc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0f990-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="0f990-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0f990-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0f990-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0f990-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="0f990-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f990-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="0f990-106">curriedop: 't-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="0f990-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="0f990-107">zuerst: 't</span><span class="sxs-lookup"><span data-stu-id="0f990-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="0f990-108">Zweitens: "U</span><span class="sxs-lookup"><span data-stu-id="0f990-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="0f990-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0f990-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0f990-110">Typparameter</span><span class="sxs-lookup"><span data-stu-id="0f990-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0f990-111">GIF</span><span class="sxs-lookup"><span data-stu-id="0f990-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="0f990-112">"U</span><span class="sxs-lookup"><span data-stu-id="0f990-112">'U</span></span>

