---
uid: Microsoft.Quantum.Canon.DelayedC
title: Delayedc-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: a1f2582668131816b774bf4a8b7476d9f1ee8cad
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840561"
---
# <a name="delayedc-function"></a><span data-ttu-id="beaf7-102">Delayedc-Funktion</span><span class="sxs-lookup"><span data-stu-id="beaf7-102">DelayedC function</span></span>

<span data-ttu-id="beaf7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="beaf7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="beaf7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="beaf7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="beaf7-105">Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.</span><span class="sxs-lookup"><span data-stu-id="beaf7-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="beaf7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="beaf7-106">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="beaf7-107">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="beaf7-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="beaf7-108">Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="beaf7-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="beaf7-109">arg: 't</span><span class="sxs-lookup"><span data-stu-id="beaf7-109">arg : 'T</span></span>

<span data-ttu-id="beaf7-110">Die Eingabe, auf die der Vorgang `op` angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="beaf7-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-ctl"></a><span data-ttu-id="beaf7-111">Ausgabe: [Einheiten](xref:microsoft.quantum.lang-ref.unit) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="beaf7-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="beaf7-112">Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`</span><span class="sxs-lookup"><span data-stu-id="beaf7-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="beaf7-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="beaf7-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="beaf7-114">GIF</span><span class="sxs-lookup"><span data-stu-id="beaf7-114">'T</span></span>

<span data-ttu-id="beaf7-115">Der Eingabetyp des Vorgangs, der verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="beaf7-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="beaf7-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="beaf7-116">See Also</span></span>

- [<span data-ttu-id="beaf7-117">Microsoft. Quantum. Canon. verzögert</span><span class="sxs-lookup"><span data-stu-id="beaf7-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="beaf7-118">Microsoft. Quantum. Canon. Delay</span><span class="sxs-lookup"><span data-stu-id="beaf7-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)