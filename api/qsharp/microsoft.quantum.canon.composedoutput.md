---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: Composedoutput-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: d39fcd6b2987b3a4f69df13fa83b69a199d6eddb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840889"
---
# <a name="composedoutput-function"></a><span data-ttu-id="7ffcd-102">Composedoutput-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ffcd-102">ComposedOutput function</span></span>

<span data-ttu-id="7ffcd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7ffcd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7ffcd-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7ffcd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7ffcd-105">Gibt die Ausgabe der Komposition von `inner` und `outer` für eine angegebene Eingabe zurück.</span><span class="sxs-lookup"><span data-stu-id="7ffcd-105">Returns the output of the composition of `inner` and `outer` for a given input.</span></span>

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a><span data-ttu-id="7ffcd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ffcd-106">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="7ffcd-107">Outer: "U->" V</span><span class="sxs-lookup"><span data-stu-id="7ffcd-107">outer : 'U -> 'V</span></span>




### <a name="inner--t---u"></a><span data-ttu-id="7ffcd-108">innere: 't-> ' U</span><span class="sxs-lookup"><span data-stu-id="7ffcd-108">inner : 'T -> 'U</span></span>




### <a name="target--t"></a><span data-ttu-id="7ffcd-109">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="7ffcd-109">target : 'T</span></span>





## <a name="output--v"></a><span data-ttu-id="7ffcd-110">Ausgabe: "V</span><span class="sxs-lookup"><span data-stu-id="7ffcd-110">Output : 'V</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7ffcd-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7ffcd-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7ffcd-112">GIF</span><span class="sxs-lookup"><span data-stu-id="7ffcd-112">'T</span></span>


### <a name="u"></a><span data-ttu-id="7ffcd-113">"U</span><span class="sxs-lookup"><span data-stu-id="7ffcd-113">'U</span></span>


### <a name="v"></a><span data-ttu-id="7ffcd-114">"V</span><span class="sxs-lookup"><span data-stu-id="7ffcd-114">'V</span></span>

