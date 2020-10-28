---
uid: Microsoft.Quantum.Canon.DelayedC
title: Delayedc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704194"
---
# <a name="delayedc-function"></a><span data-ttu-id="14690-102">Delayedc-Funktion</span><span class="sxs-lookup"><span data-stu-id="14690-102">DelayedC function</span></span>

<span data-ttu-id="14690-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="14690-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="14690-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="14690-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="14690-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="14690-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="14690-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14690-106">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="14690-107">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="14690-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="14690-108">Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14690-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="14690-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="14690-109">arg : 'T</span></span>

<span data-ttu-id="14690-110">Die Eingabe, auf die der Vorgang `op` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="14690-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl"></a><span data-ttu-id="14690-111">Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="14690-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="14690-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="14690-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="14690-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="14690-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="14690-114">GIF</span><span class="sxs-lookup"><span data-stu-id="14690-114">'T</span></span>

<span data-ttu-id="14690-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="14690-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="14690-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14690-116">See Also</span></span>

- [<span data-ttu-id="14690-117">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="14690-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="14690-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="14690-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)