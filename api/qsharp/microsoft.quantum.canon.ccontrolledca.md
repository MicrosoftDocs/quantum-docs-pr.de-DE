---
uid: Microsoft.Quantum.Canon.CControlledCA
title: Ccontrolledca-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledCA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 740461ee17bdda281a6bd8572a15d27b17be9535
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840950"
---
# <a name="ccontrolledca-function"></a><span data-ttu-id="64fa4-102">Ccontrolledca-Funktion</span><span class="sxs-lookup"><span data-stu-id="64fa4-102">CControlledCA function</span></span>

<span data-ttu-id="64fa4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="64fa4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="64fa4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64fa4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64fa4-105">Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist.</span><span class="sxs-lookup"><span data-stu-id="64fa4-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="64fa4-106">Gibt an `false` , dass nichts passiert.</span><span class="sxs-lookup"><span data-stu-id="64fa4-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="64fa4-107">Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.</span><span class="sxs-lookup"><span data-stu-id="64fa4-107">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
function CControlledCA<'T> (op : ('T => Unit is Ctl + Adj)) : ((Bool, 'T) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="64fa4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64fa4-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="64fa4-109">OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="64fa4-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="64fa4-110">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64fa4-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit--is-adj--ctl"></a><span data-ttu-id="64fa4-111">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="64fa4-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="64fa4-112">Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement</span><span class="sxs-lookup"><span data-stu-id="64fa4-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="64fa4-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="64fa4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="64fa4-114">GIF</span><span class="sxs-lookup"><span data-stu-id="64fa4-114">'T</span></span>

<span data-ttu-id="64fa4-115">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64fa4-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="64fa4-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64fa4-116">See Also</span></span>

- [<span data-ttu-id="64fa4-117">Microsoft. Quantum. Canon. ckontrollierten</span><span class="sxs-lookup"><span data-stu-id="64fa4-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)