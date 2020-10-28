---
uid: Microsoft.Quantum.Canon.CControlledC
title: Ccontrolledc-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e5975455385e182236d7e2864e26ca00795a40c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704402"
---
# <a name="ccontrolledc-function"></a><span data-ttu-id="5e086-102">Ccontrolledc-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e086-102">CControlledC function</span></span>

<span data-ttu-id="5e086-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5e086-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5e086-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5e086-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5e086-105">Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist.</span><span class="sxs-lookup"><span data-stu-id="5e086-105">Given an operation op, returns a new operation which applies the op if a classical control bit is true.</span></span> <span data-ttu-id="5e086-106">Gibt an `false` , dass nichts passiert.</span><span class="sxs-lookup"><span data-stu-id="5e086-106">If `false`, nothing happens.</span></span>
<span data-ttu-id="5e086-107">Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="5e086-107">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="5e086-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e086-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="5e086-109">OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="5e086-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5e086-110">Ein Vorgang, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e086-110">An operation to be conditionally applied.</span></span>



## <a name="output--boolt--unit-ctl"></a><span data-ttu-id="5e086-111">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="5e086-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5e086-112">Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5e086-112">A new operation which is op if the classical control bit is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5e086-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5e086-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5e086-114">GIF</span><span class="sxs-lookup"><span data-stu-id="5e086-114">'T</span></span>

<span data-ttu-id="5e086-115">Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e086-115">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e086-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e086-116">See Also</span></span>

- [<span data-ttu-id="5e086-117">Microsoft. Quantum. Canon. ckontrollierten</span><span class="sxs-lookup"><span data-stu-id="5e086-117">Microsoft.Quantum.Canon.CControlled</span></span>](xref:Microsoft.Quantum.Canon.CControlled)