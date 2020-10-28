---
uid: Microsoft.Quantum.Canon.CControlledCA
title: Ccontrolledca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 20a8c9ccf931261f7bc6e347ccc144c92f0d0545
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704399"
---
# <a name="ccontrolledca-function"></a><span data-ttu-id="2a27e-102">Ccontrolledca-Funktion</span><span class="sxs-lookup"><span data-stu-id="2a27e-102">CControlledCA function</span></span>

<span data-ttu-id="2a27e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a27e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a27e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a27e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a27e-105">Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist.</span><span class="sxs-lookup"><span data-stu-id="2a27e-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="2a27e-106">Gibt an `false` , dass nichts passiert.</span><span class="sxs-lookup"><span data-stu-id="2a27e-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="2a27e-107">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="2a27e-107">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="2a27e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2a27e-108">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="2a27e-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="2a27e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="2a27e-110">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a27e-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-ctl--adj"></a><span data-ttu-id="2a27e-111">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="2a27e-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="2a27e-112">Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2a27e-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2a27e-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="2a27e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a27e-114">GIF</span><span class="sxs-lookup"><span data-stu-id="2a27e-114">'T</span></span>

<span data-ttu-id="2a27e-115">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a27e-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a27e-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2a27e-116">See Also</span></span>

- [<span data-ttu-id="2a27e-117">Microsoft. Quantum. Canon. ckontrollierten</span><span class="sxs-lookup"><span data-stu-id="2a27e-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)