---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Vorgang "carryoutcorecdkm"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 19a692a3b54a413f25a474c361e773ab6c65579e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223543"
---
# <a name="carryoutcorecdkm-operation"></a><span data-ttu-id="82be0-102">Vorgang "carryoutcorecdkm"</span><span class="sxs-lookup"><span data-stu-id="82be0-102">CarryOutCoreCDKM operation</span></span>

<span data-ttu-id="82be0-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="82be0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="82be0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="82be0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="82be0-105">Der Kern Vorgang in ripplecarryaddercdkm, der mit dem obigen applyoutercdkmadder-Vorgang verwendet wird, der mit diesem Vorgang konjuregiert wurde, um die innere Operation von ripplecarryaddercdkm abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82be0-105">The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM.</span></span> <span data-ttu-id="82be0-106">Mit diesem Vorgang wird das Qubit "ausführen" berechnet und eine Sequenz von "Not Gates" auf einen Teil der Eingabe angewendet `ys` .</span><span class="sxs-lookup"><span data-stu-id="82be0-106">This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.</span></span>

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="82be0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="82be0-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="82be0-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="82be0-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="82be0-109">Erstes Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="82be0-109">First qubit register.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="82be0-110">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="82be0-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="82be0-111">Zweites Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="82be0-111">Second qubit register.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="82be0-112">Ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="82be0-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="82be0-113">Das in ripplecarryaddercdkm verwendete Ancilla-Qubit, das an diesen Vorgang übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="82be0-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="82be0-114">Carry: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="82be0-114">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="82be0-115">Führen Sie Qubit im ripplecarryaddercdkm-Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="82be0-115">Carry out qubit in the RippleCarryAdderCDKM operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82be0-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82be0-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="82be0-117">Referenzen</span><span class="sxs-lookup"><span data-stu-id="82be0-117">References</span></span>

- <span data-ttu-id="82be0-118">Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="82be0-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1