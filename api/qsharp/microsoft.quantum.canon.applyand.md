---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Applyand-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705503"
---
# <a name="applyand-operation"></a><span data-ttu-id="b6bdd-102">Applyand-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b6bdd-102">ApplyAnd operation</span></span>

<span data-ttu-id="b6bdd-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b6bdd-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6bdd-105">Kehrt ein angegebenes Ziel-Qubit nur dann ein, wenn beide Steuerelement-Qubits den Status 1 aufweisen, wobei die Messung zum Ausführen des Adjoint-Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="b6bdd-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6bdd-106">Description</span></span>

<span data-ttu-id="b6bdd-107">Kehrt `target` nur dann zu, wenn beide Steuerelemente 1 sind, jedoch wird davon ausgegangen, dass `target` sich der Status 0 (null) befindet.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="b6bdd-108">Der Vorgang hat t-count 4, T-Tiefe 2 und erfordert kein Hilfsobjekt und ist daher möglicherweise einem ccnot-Vorgang vorzuziehen, wenn `target` bekanntermaßen 0 ist.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-108">The operation has T-count 4, T-depth 2 and requires no helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="b6bdd-109">Das Adjoint-Ergebnis dieses Vorgangs ist Messungs basiert und erfordert keine T-Gates.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-109">The adjoint of this operation is measurement based and requires no T gates.</span></span>

<span data-ttu-id="b6bdd-110">Die kontrollierte Anwendung dieses Vorgangs erfordert kein Hilfsobjekt, `2^c` `Rz` Gates und ist nicht für die Tiefe optimiert, wobei `c` die Anzahl der allgemeinen Steuerungs Qubits einschließlich der beiden Steuerelemente des `ApplyAnd` Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-110">The controlled application of this operation requires no helper qubit, `2^c` `Rz` gates and is not optimized for depth, where `c` is the number of overall control qubits including the two controls from the `ApplyAnd` operation.</span></span>  <span data-ttu-id="b6bdd-111">Die Adjoint-gesteuerte Anwendung erfordert `2^c - 1` `Rz` Gates (bei einem doppelten Winkel die Größe des nicht-Adjoint-Vorgangs), kein hilfssbit und ist nicht für die Tiefe optimiert.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-111">The adjoint controlled application requires `2^c - 1` `Rz` gates (with an angle twice the size of the non-adjoint operation), no helper qubit and is not optimized for depth.</span></span>

## <a name="input"></a><span data-ttu-id="b6bdd-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b6bdd-112">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="b6bdd-113">Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-113">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b6bdd-114">Qubit für erstes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b6bdd-114">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="b6bdd-115">Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-115">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b6bdd-116">Qubit für zweites Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b6bdd-116">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b6bdd-117">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b6bdd-118">Zusätzliches Qubit für Ziel muss den Status 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b6bdd-118">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="b6bdd-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="b6bdd-120">Referenzen</span><span class="sxs-lookup"><span data-stu-id="b6bdd-120">References</span></span>

- <span data-ttu-id="b6bdd-121">Cody Jones: "neuartige Konstruktionen für das Fault-tolerante yffoli Gate", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/physreva. 87.022328</span><span class="sxs-lookup"><span data-stu-id="b6bdd-121">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="b6bdd-122">Craig Gidney: "halbieren der Kosten der Quantum-Addition", Quantum 2, Seite 74, 2018 [arXiv: 1709.06648](https://arxiv.org/abs/1709.06648) doi: 10.1103/physreva. 85.044302</span><span class="sxs-lookup"><span data-stu-id="b6bdd-122">Craig Gidney: "Halving the cost of quantum addition", Quantum 2, page 74, 2018 [arXiv:1709.06648](https://arxiv.org/abs/1709.06648) doi:10.1103/PhysRevA.85.044302</span></span>
- <span data-ttu-id="b6bdd-123">Mathias soeken: "Quantum Oracle-Leitungen und das Weihnachtsbaum Muster", [Blog-Artikel vom 19. Dezember 2019](https://msoeken.github.io/blog_qac.html) (Hinweis: erläutert die mehrfach gesteuerte Konstruktion)</span><span class="sxs-lookup"><span data-stu-id="b6bdd-123">Mathias Soeken: "Quantum Oracle Circuits and the Christmas Tree Pattern", [Blog article from December 19, 2019](https://msoeken.github.io/blog_qac.html) (note: explains the multiple controlled construction)</span></span>