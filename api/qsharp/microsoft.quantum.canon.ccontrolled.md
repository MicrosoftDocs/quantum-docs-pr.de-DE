---
uid: Microsoft.Quantum.Canon.CControlled
title: C-gesteuerte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: a155b00806b17258b3f87629659bc7d786e4e11d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704410"
---
# <a name="ccontrolled-function"></a><span data-ttu-id="70f04-102">C-gesteuerte Funktion</span><span class="sxs-lookup"><span data-stu-id="70f04-102">CControlled function</span></span>

<span data-ttu-id="70f04-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="70f04-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="70f04-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="70f04-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="70f04-105">Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist.</span><span class="sxs-lookup"><span data-stu-id="70f04-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="70f04-106">Gibt an `false` , dass nichts passiert.</span><span class="sxs-lookup"><span data-stu-id="70f04-106">If `false`, nothing happens.</span></span>

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a><span data-ttu-id="70f04-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70f04-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="70f04-108">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="70f04-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="70f04-109">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70f04-109">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit"></a><span data-ttu-id="70f04-110">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="70f04-110">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="70f04-111">Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement</span><span class="sxs-lookup"><span data-stu-id="70f04-111">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="70f04-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="70f04-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="70f04-113">GIF</span><span class="sxs-lookup"><span data-stu-id="70f04-113">'T</span></span>

<span data-ttu-id="70f04-114">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70f04-114">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="70f04-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70f04-115">See Also</span></span>

- [<span data-ttu-id="70f04-116">Microsoft. Quantum. Canon. ccontrolledc</span><span class="sxs-lookup"><span data-stu-id="70f04-116">Microsoft.Quantum.Canon.CControlledC</span></span>](xref:Microsoft.Quantum.Canon.CControlledC)
- [<span data-ttu-id="70f04-117">Microsoft. Quantum. Canon. ccontrolleda</span><span class="sxs-lookup"><span data-stu-id="70f04-117">Microsoft.Quantum.Canon.CControlledA</span></span>](xref:Microsoft.Quantum.Canon.CControlledA)
- [<span data-ttu-id="70f04-118">Microsoft. Quantum. Canon. ccontrolledca</span><span class="sxs-lookup"><span data-stu-id="70f04-118">Microsoft.Quantum.Canon.CControlledCA</span></span>](xref:Microsoft.Quantum.Canon.CControlledCA)