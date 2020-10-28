---
uid: Microsoft.Quantum.Canon.AndLadder
title: Andladder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 05a0e8110539742501883fea75ac368d9946164d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705519"
---
# <a name="andladder-operation"></a><span data-ttu-id="af5b4-102">Andladder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5b4-102">AndLadder operation</span></span>

<span data-ttu-id="af5b4-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="af5b4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="af5b4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="af5b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="af5b4-105">Führt eine gesteuerte "and-Leiter" für ein Register der Ziel-Qubits aus.</span><span class="sxs-lookup"><span data-stu-id="af5b4-105">Performs a controlled "AND ladder" on a register of target qubits.</span></span>

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="af5b4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af5b4-106">Description</span></span>

<span data-ttu-id="af5b4-107">Durch diesen Vorgang wird eine Transformation angewendet, die von der folgenden Zuordnung der Berechnungsbasis beschrieben wird. $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \mapsto \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x \_ 1 \land x \_ 2), \dots, y \_ {n-1} \oplus (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{align} $ $, wobei $ \ket{x \_ 1, \dots, x \_ n} $ bezieht sich auf die Berechnungsbasis Zustände von `controls` , und WHERE $ \ket{y \_ 1, \dots, y \_ {n-1}} $ bezieht sich auf die Berechnungsbasis Zustände von `targets` .</span><span class="sxs-lookup"><span data-stu-id="af5b4-107">This operation applies a transformation described by the following mapping of the computational basis, $$ \begin{align} \ket{x\_1, \dots, x\_n} \ket{y\_1, \dots, y\_{n - 1}} \mapsto \ket{x\_1, \dots, x\_n} \ket{ y\_1 \oplus (x\_1 \land x\_2), \dots, y\_{n - 1} \oplus (x\_1 \land x\_2 \land \cdots \land x\_{n - 1} }, \end{align} $$ where $\ket{x\_1, \dots, x\_n}$ refers to the computational basis states of `controls`, and where $\ket{y\_1, \dots, y\_{n - 1}}$ refers to the computational basis states of `targets`.</span></span>

## <a name="input"></a><span data-ttu-id="af5b4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="af5b4-108">Input</span></span>

### <a name="ccnot--ccnotop"></a><span data-ttu-id="af5b4-109">ccnot: [ccnotop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="af5b4-109">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="af5b4-110">Das ccnot-Gate, das für die Konstruktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af5b4-110">The CCNOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="af5b4-111">Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="af5b4-111">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="af5b4-112">Ein Register von Qubits, das als Steuerelemente für die-und-Leiter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af5b4-112">A register of qubits to be used as controls for the and ladder.</span></span>
<span data-ttu-id="af5b4-113">Mit diesem Vorgang bleiben die Berechnungsbasis Zustände `controls` invariant.</span><span class="sxs-lookup"><span data-stu-id="af5b4-113">This operation leaves computational basis states of `controls` invariant.</span></span>
<span data-ttu-id="af5b4-114">Die Länge von `controls` muss mindestens 2 betragen und muss gleich 1 und der Länge von sein `targets` .</span><span class="sxs-lookup"><span data-stu-id="af5b4-114">The length of `controls` must be at least 2, and must be equal to one plus the length of `targets`.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="af5b4-115">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="af5b4-115">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="af5b4-116">Die Länge von `targets` muss mindestens 1 betragen und gleich der Länge von minus 1 sein `controls` .</span><span class="sxs-lookup"><span data-stu-id="af5b4-116">The length of `targets` must be at least 1 and equal to the length of `controls` minus one.</span></span>



## <a name="output--unit"></a><span data-ttu-id="af5b4-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="af5b4-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="af5b4-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af5b4-118">Remarks</span></span>

- <span data-ttu-id="af5b4-119">Wird als Teil von <xref:microsoft.quantum.canon.applymulticontrolledc> und verwendet <xref:microsoft.quantum.canon.applymulticontrolledca> .</span><span class="sxs-lookup"><span data-stu-id="af5b4-119">Used as a part of <xref:microsoft.quantum.canon.applymulticontrolledc> and <xref:microsoft.quantum.canon.applymulticontrolledca>.</span></span>
- <span data-ttu-id="af5b4-120">Eine Erläuterung und ein Leitungs Diagramm finden Sie in Abbildung 4,10, Abschnitt 4,3 in Nielsen & Chuang.</span><span class="sxs-lookup"><span data-stu-id="af5b4-120">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang.</span></span>

## <a name="references"></a><span data-ttu-id="af5b4-121">Referenzen</span><span class="sxs-lookup"><span data-stu-id="af5b4-121">References</span></span>

- [<span data-ttu-id="af5b4-122">*Michael A. Nielsen, ISAL. Chuang* , Quantum-Berechnung und Quantum-Informationen</span><span class="sxs-lookup"><span data-stu-id="af5b4-122"> *Michael A. Nielsen , Isaac L. Chuang* , Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)