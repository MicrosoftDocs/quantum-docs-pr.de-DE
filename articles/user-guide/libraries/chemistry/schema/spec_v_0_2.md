---
title: Broombridge-Schema Spezifikation (ver 0,2)
description: Erläutert die Spezifikationen für das broombridge-Quantum-Schema v 0,2 für die Microsoft Quantum Chemistry Library.
author: guanghaolow
ms.author: gulow
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
no-loc:
- Q#
- $$v
ms.openlocfilehash: 851d10c0137deecf8e861aad30b5e08a9ae61754
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833763"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="d8a94-103">Broombridge-Spezifikation v 0,2</span><span class="sxs-lookup"><span data-stu-id="d8a94-103">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="d8a94-104">Die Schlüsselwörter "muss", "darf nicht", "erforderlich", "soll", "soll nicht", "sollte", "sollte nicht", "empfohlen", "Mai" und "optional" in diesem Dokument interpretiert werden, wie in [RFC 2119](https://tools.ietf.org/html/rfc2119)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8a94-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="d8a94-105">Jede Rand Leiste mit den Überschriften "Note", "Information" oder "Warning" ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="d8a94-106">Einführung</span><span class="sxs-lookup"><span data-stu-id="d8a94-106">Introduction</span></span> ##

<span data-ttu-id="d8a94-107">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-107">This section is informative.</span></span>

<span data-ttu-id="d8a94-108">Broombridge-Dokumente sollen Instanzen von Simulations Problemen in der Quantum-Chemie für die Verarbeitung mithilfe der Quantum-Simulation und der Programmier Toolkette kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d8a94-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="d8a94-109">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="d8a94-109">Serialization</span></span> ##

<span data-ttu-id="d8a94-110">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-110">This section is normative.</span></span>

<span data-ttu-id="d8a94-111">Ein broombridge-Dokument muss als [YAML 1,2-Dokument](http://yaml.org/spec/) serialisiert werden, das ein JSON-Objekt darstellt, wie in [RFC 4627](https://tools.ietf.org/html/rfc4627) Abschnitt 2,2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8a94-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="d8a94-112">Das in YAML serialisierte-Objekt muss über eine `"$schema"` -Eigenschaft verfügen, deren Wert ist `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"` und gemäß den Spezifikationen des JSON-Schema Entwurfs-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)] gültig sein muss.</span><span class="sxs-lookup"><span data-stu-id="d8a94-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="d8a94-113">Im restlichen Teil dieser Spezifikation verweist "das broombridge-Objekt" auf das JSON-Objekt, das aus einem broombridge-YAML-Dokument deserialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d8a94-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="d8a94-114">Sofern nicht anders angegeben, dürfen Objekte keine zusätzlichen Eigenschaften aufweisen, die über die explizit in diesem Dokument angegebenen verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="d8a94-115">Zusätzliche Definitionen</span><span class="sxs-lookup"><span data-stu-id="d8a94-115">Additional Definitions</span></span> ##

<span data-ttu-id="d8a94-116">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="d8a94-117">Mengen Objekte</span><span class="sxs-lookup"><span data-stu-id="d8a94-117">Quantity Objects</span></span> ###

<span data-ttu-id="d8a94-118">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-118">This section is normative.</span></span>

<span data-ttu-id="d8a94-119">Bei einem _Mengen Objekt_ handelt es sich um ein JSON-Objekt, und es muss über eine Eigenschaft verfügen, `units` deren Wert einem der in Tabelle 1 aufgeführten zulässigen Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="d8a94-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="d8a94-120">Ein Mengen Objekt ist ein _einfaches Mengen Objekt_ , wenn es über eine einzelne Eigenschaft `value` zusätzlich zu seiner- `units` Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8a94-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="d8a94-121">Der Wert der- `value` Eigenschaft muss eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="d8a94-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="d8a94-122">Bei einem Mengen Objekt handelt es sich um ein _Objekt mit begrenzter Menge_ , wenn es über die Eigenschaften `lower` und `upper` zusätzlich zur- `units` Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8a94-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="d8a94-123">Die Werte der `lower` Eigenschaften und `upper` müssen zahlen sein.</span><span class="sxs-lookup"><span data-stu-id="d8a94-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="d8a94-124">Ein Objekt mit begrenzter Menge kann über eine Eigenschaft verfügen, `value` deren Wert eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="d8a94-125">Bei einem Mengen Objekt handelt es sich um ein _Array Objekt_ mit geringer Dichte `format` , wenn die-Eigenschaft und eine-Eigenschaft `values` zusätzlich zur-Eigenschaft aufweisen `units` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="d8a94-126">Der Wert von `format` muss die Zeichenfolge sein `sparse` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="d8a94-127">Der Wert der `values` Eigenschaft muss ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="d8a94-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="d8a94-128">Jedes Element von `values` muss ein Array sein, das die Indizes und den Wert der Menge an Arrays mit geringer Dichte darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8a94-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="d8a94-129">Die Indizes für jedes Element eines Arrays mit geringer Dichte Menge müssen innerhalb des gesamten Objekts mit geringer Dichte Menge eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d8a94-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="d8a94-130">Wenn ein Index mit dem Wert vorhanden ist `0` , muss ein Parser das Mengen Objekt mit geringer Dichte mit einem Array mit geringer Menge an Mengen Objekten behandeln, in dem dieser Index überhaupt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="d8a94-131">Ein Mengen Objekt muss entweder</span><span class="sxs-lookup"><span data-stu-id="d8a94-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="d8a94-132">ein einfaches Mengen Objekt,</span><span class="sxs-lookup"><span data-stu-id="d8a94-132">a simple quantity object,</span></span>
- <span data-ttu-id="d8a94-133">ein Objekt mit begrenzter Menge oder</span><span class="sxs-lookup"><span data-stu-id="d8a94-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="d8a94-134">ein Mengen Objekt mit geringer Dichte.</span><span class="sxs-lookup"><span data-stu-id="d8a94-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="d8a94-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8a94-135">Examples</span></span> ###

<span data-ttu-id="d8a94-136">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-136">This section is informative.</span></span>

<span data-ttu-id="d8a94-137">Eine einfache Menge, die $1.9844146837 \, \mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="d8a94-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="d8a94-138">Eine begrenzte Menge, die eine einheitliche Verteilung im Intervall von $ [-7,-6] \, \mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="d8a94-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="d8a94-139">Im folgenden finden Sie eine Array Menge mit geringer Dichte, bei der ein `[1, 2]` -Element gleich ist `hello` und ein-Element `[3, 4]` gleich ist `world` :</span><span class="sxs-lookup"><span data-stu-id="d8a94-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="d8a94-140">Abschnitt "Format"</span><span class="sxs-lookup"><span data-stu-id="d8a94-140">Format Section</span></span> ##

<span data-ttu-id="d8a94-141">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-141">This section is normative.</span></span>

<span data-ttu-id="d8a94-142">Das broombridge-Objekt muss über eine-Eigenschaft verfügen, `format` deren Wert ein JSON-Objekt mit einer Eigenschaft namens ist `version` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="d8a94-143">Die- `version` Eigenschaft muss den Wert aufweisen `"0.2"` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-143">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="d8a94-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d8a94-144">Example</span></span> ###

<span data-ttu-id="d8a94-145">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="d8a94-146">Problem Beschreibungs Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d8a94-146">Problem Description Section</span></span> ##

<span data-ttu-id="d8a94-147">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-147">This section is normative.</span></span>

<span data-ttu-id="d8a94-148">Das broombridge-Objekt muss über eine Eigenschaft verfügen, `problem_description` deren Wert ein JSON-Array ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-148">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="d8a94-149">Jedes Element im Wert der- `problem_description` Eigenschaft muss ein JSON-Objekt sein, das einen Satz von inteden beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8a94-149">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="d8a94-150">Im restlichen Teil dieses Abschnitts verweist der Begriff "problembeschreibungs-Objekt" auf ein Element im Wert der- `problem_description` Eigenschaft des broombridge-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8a94-150">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="d8a94-151">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft verfügen, `metadata` deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-151">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="d8a94-152">Der Wert von `metadata` kann das leere JSON-Objekt (d. h `{}` .) sein oder zusätzliche Eigenschaften enthalten, die durch den implemenor definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8a94-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="d8a94-153">Hamiltona-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d8a94-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="d8a94-154">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d8a94-154">Overview</span></span> ####

<span data-ttu-id="d8a94-155">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-155">This section is informative.</span></span>

<span data-ttu-id="d8a94-156">Die- `hamiltonian` Eigenschaft der einzelnen problembeschreibungs Objekte beschreibt den hamiltonan für ein bestimmtes Quantum-Chemie Problem, indem er seine ein-und zwei Text Begriffe als sparsesrearrays von reellen Zahlen auflistet.</span><span class="sxs-lookup"><span data-stu-id="d8a94-156">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="d8a94-157">Die von den einzelnen problembeschreibungs-Objekten beschriebenen hamiltonan-Operatoren haben das Formular.</span><span class="sxs-lookup"><span data-stu-id="d8a94-157">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="d8a94-158">$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparser, \downpfeil \\ }} h \_ \{ IJ \} a ^ \{ \dagger \} \_ {i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, l \} \sum \_ {\sigma, \rho\in \\ {\uparser, \downpfeil \\ }} H \_ {IJKL} a ^ \dagger \_ {i, \sigma} a ^ \dagger \_ {k, \rho} a \_ {l, \rho} a \_ {j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="d8a94-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="d8a94-159">Hier $h _ {IJKL} = (IJ | KL) $ in der Mulliken-Konvention.</span><span class="sxs-lookup"><span data-stu-id="d8a94-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="d8a94-160">Aus Gründen der Übersichtlichkeit lautet der Begriff mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="d8a94-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="d8a94-161">$ $ H_ {IJ} = \int {\mathrm d} x \psi ^ \* \_ i (x) \left (\frac {1} {2} \nabla ^ 2 + \sum \_ {A} \bruchteil {z \_ A} {| x-x \_ A |}  \right) \psi \_ j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="d8a94-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="d8a94-162">und der zwei-Elektronen-Begriff ist</span><span class="sxs-lookup"><span data-stu-id="d8a94-162">and the two-electron term is</span></span>

<span data-ttu-id="d8a94-163">$ $ h \_ \{ IJKL \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \frac \{ 1 \} \{ \| x \_ 1-x \_ 2 \| \} \psi \_ k ^ \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).</span><span class="sxs-lookup"><span data-stu-id="d8a94-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="d8a94-164">Wie in der Beschreibung der- [ `basis_set` Eigenschaft](#basis-set-object) der einzelnen Elemente der- `integral_sets` Eigenschaft erwähnt, wird explizit angenommen, dass die verwendeten Basisfunktionen einen echten Wert haben.</span><span class="sxs-lookup"><span data-stu-id="d8a94-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="d8a94-165">Dies ermöglicht es uns, die folgenden Symmetries zwischen den Begriffen zu verwenden, um die Darstellung der hamiltonan zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="d8a94-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="d8a94-166">$ $ H_ {IJKL} = H_ {IJLK} = H_ {jikl} = H_ {jilk} = H_ {klij} = H_ {klji} = H_ {lkij} = H_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="d8a94-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="d8a94-167">Inhalte</span><span class="sxs-lookup"><span data-stu-id="d8a94-167">Contents</span></span> ####

<span data-ttu-id="d8a94-168">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-168">This section is normative.</span></span>

<span data-ttu-id="d8a94-169">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft verfügen, `hamiltonian` deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-169">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="d8a94-170">Der Wert der- `hamiltonian` Eigenschaft wird als "hamiltonan"-Objekt bezeichnet und muss über die Eigenschaften und verfügen, `one_electron_integrals` `two_electron_integrals` wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8a94-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="d8a94-171">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft verfügen, `coulomb_repulsion` deren Wert ein einfaches Mengen Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-171">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="d8a94-172">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft verfügen, `energy_offet` deren Wert ein einfaches Mengen Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-172">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="d8a94-173">Nebenbei Die Werte von und, die addiert werden, `coulomb_repulsion` `energy_offet` erfassen den Identitätsbegriff der hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="d8a94-173">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="d8a94-174">Integrale Objekt mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="d8a94-174">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="d8a94-175">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-175">This section is normative.</span></span>

<span data-ttu-id="d8a94-176">Die- `one_electron_integrals` Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte sein, deren Indizes zwei Ganzzahlen und deren Werte Ziffern sind.</span><span class="sxs-lookup"><span data-stu-id="d8a94-176">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="d8a94-177">Jeder Begriff muss über Indizes verfügen, `[i, j]` bei denen `i >= j` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-177">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="d8a94-178">Nebenbei Dies spiegelt die Symmetrie wider, die $h _ {IJ} = H_ {JI} $ liegt. Dies ist eine Folge der Tatsache, dass der hamiltonan hermitian ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-178">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="d8a94-179">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d8a94-179">Example</span></span> ######

<span data-ttu-id="d8a94-180">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-180">This section is informative.</span></span>

<span data-ttu-id="d8a94-181">Die folgende Menge an Sparse-Arrays repräsentiert die hamiltonan $ $ H = \left (-5,0 (a ^ \{ \dagger \} \_ {1, \uanrow} a \_ {1, \uparamerow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {1, \downarrow}) + 0,17 (a ^ \{ \dagger \} \_ {2, \uparamerow} a \_ {1, \uparamerow} + a ^ \{ \dagger \} \_ {1, \uanrow} a \_ {2, \uparamerow} + a ^ \{ \dagger \} \_ {2, \downarrow} a \_ {1, \downarrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {2, \downarrow}) \right) \\ , \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="d8a94-181">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
$$

```yaml
one_electron_integrals:     # required
    units: hartree          # required
    format: sparse          # required
    values:                 # required
        # i j f(i,j)
        - [1, 1, -5.0]
        - [2, 1,  0.17]
```
> [!NOTE]
> <span data-ttu-id="d8a94-182">Broombridge verwendet die 1-basierte Indizierung.</span><span class="sxs-lookup"><span data-stu-id="d8a94-182">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="d8a94-183">2-Elektronen-inteals-Objekt</span><span class="sxs-lookup"><span data-stu-id="d8a94-183">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="d8a94-184">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-184">This section is normative.</span></span>

<span data-ttu-id="d8a94-185">Die- `two_electron_integrals` Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte mit einer zusätzlichen Eigenschaft namens sein `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-185">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="d8a94-186">Jedes Element des Werts von `two_electron_integrals` muss über vier Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-186">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="d8a94-187">Jede `two_electron_integrals` Eigenschaft muss über eine `index_convention` Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-187">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="d8a94-188">Der Wert der- `index_convention` Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 1 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d8a94-188">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="d8a94-189">Wenn der Wert von `index_convention` auf festgestellt wird `mulliken` , `two_electron_integrals` muss ein Parser, der ein broombridge-Dokument lädt, für jedes Element der Menge an Sparse-Arrays einen "hamiltona"-Begriff instanziieren, der gleich dem zwei-Elektronen-Operator ist $h _ {i, j, k, l} a ^ \ dagger_i a ^ \ dagger_j a_k a_l $, wobei $i $, $j $, $k $ und $l $ ganzzahlige Werte von mindestens 1 sein müssen und wobei $h _ {i, j, k, l} $ das Element `[i, j, k, l, h(i, j, k, l)]` der Menge an geringer Dichte ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-189">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="d8a94-190">Symmetries</span><span class="sxs-lookup"><span data-stu-id="d8a94-190">Symmetries</span></span> ######

<span data-ttu-id="d8a94-191">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-191">This section is normative.</span></span>

<span data-ttu-id="d8a94-192">Wenn die- `index_convention` Eigenschaft eines- `two_electron_integrals` Objekts gleich ist `mulliken` , dann, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, dürfen die folgenden Indizes nicht vorhanden sein, es sei denn, Sie sind gleich `[i, j, k, l]` :</span><span class="sxs-lookup"><span data-stu-id="d8a94-192">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="d8a94-193">Da die- `index_convention` Eigenschaft ein Objekt mit geringer Dichte ist, werden möglicherweise keine Indizes für verschiedene Elemente wiederholt.</span><span class="sxs-lookup"><span data-stu-id="d8a94-193">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="d8a94-194">Insbesondere, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, kann kein anderes Element über diese Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-194">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="d8a94-195">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d8a94-195">Example</span></span> #######

<span data-ttu-id="d8a94-196">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-196">This section is informative.</span></span>

<span data-ttu-id="d8a94-197">Das folgende Objekt gibt den hamiltonan an.</span><span class="sxs-lookup"><span data-stu-id="d8a94-197">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="d8a94-198">$$ H = \frac12 \sum \_ {\sigma,\rho\in \\ {\uparrow,\downarrow \\ }}\Biggr( 1.6 a^{\dagger} \_ {1,\sigma} a^{\dagger} \_ {1,\rho} a \_ {1,\rho} a \_ {1,\sigma}- 0.1 a^{\dagger} \_ {6,\sigma} a^{\dagger} \_ {1,\rho} a \_ {3,\rho} a \_ {2,\sigma}- 0.1 a^{\dagger} \_ {6,\sigma} a^{\dagger} \_ {1,\rho} a \_ {2,\rho} a \_ {3,\sigma}- 0.1 a^{\dagger} \_ {1,\sigma} a^{\dagger} \_ {6,\rho} a \_ {3,\rho} a \_ {2,\sigma}- 0.1 a^{\dagger} \_ {1,\sigma} a^{\dagger} \_ {6,\rho} a \_ {2,\rho} a \_ {3,\sigma} $$ $$- 0.1 a^{\dagger} \_ {3,\sigma} a^{\dagger} \_ {2,\rho} a \_ {6,\rho} a \_ {1,\sigma}- 0.1 a^{\dagger} \_ {3,\sigma} a^{\dagger} \_ {2,\rho} a \_ {1,\rho} a \_ {6,\sigma}- 0.1 a^{\dagger} \_ {2,\sigma} a^{\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="d8a94-198">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
$$

```yaml
two_electron_integrals:
    index_convention: mulliken
    units: hartree
    format: sparse
    values:
        - [1, 1, 1, 1,  1.6]
        - [6, 1, 3, 2, -0.1]
```

### <a name="initial-state-section"></a><span data-ttu-id="d8a94-199">Abschnitt "Anfangszustand"</span><span class="sxs-lookup"><span data-stu-id="d8a94-199">Initial State Section</span></span> ###

<span data-ttu-id="d8a94-200">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-200">This section is normative.</span></span>

<span data-ttu-id="d8a94-201">Das `initial_state_suggestion` Objekt, dessen Wert ein JSON-Array ist, gibt die anfänglichen Quantum-Zustände an, die für die angegebene hamiltonan von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="d8a94-201">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="d8a94-202">Jedes Element im Wert der- `initial_state_suggestion` Eigenschaft muss ein JSON-Objekt sein, das einen Quantenzustand beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8a94-202">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="d8a94-203">Im restlichen Teil dieses Abschnitts verweist der Begriff "State Object" auf ein Element im Wert der- `initial_state_suggestion` Eigenschaft des broombridge-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8a94-203">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="d8a94-204">State-Objekt</span><span class="sxs-lookup"><span data-stu-id="d8a94-204">State object</span></span> ####

<span data-ttu-id="d8a94-205">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-205">This section is normative.</span></span>

<span data-ttu-id="d8a94-206">Jedes Zustands Objekt muss über eine Eigenschaft verfügen, die `label` eine Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="d8a94-206">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="d8a94-207">Jedes Zustands Objekt muss über eine- `method` Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-207">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="d8a94-208">Der Wert der- `method` Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 3 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d8a94-208">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="d8a94-209">Jedes Zustands Objekt kann über eine Eigenschaft verfügen, `energy` deren Wert ein einfaches Mengen Objekt sein muss.</span><span class="sxs-lookup"><span data-stu-id="d8a94-209">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="d8a94-210">Wenn der Wert der- `method` Eigenschaft ist `sparse_multi_configurational` , muss das State-Objekt über eine-Eigenschaft verfügen, die `superposition` ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.</span><span class="sxs-lookup"><span data-stu-id="d8a94-210">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="d8a94-211">Der anfängliche Status lautet z. b. $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket $ $ $ {0} \ket{e} = \bruchteil {0,1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0.2 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket {0} , $ $, wobei $ \ket{e} $ den Wert "Energy $0,987 \textrm{ha} $" hat, werden durch</span><span class="sxs-lookup"><span data-stu-id="d8a94-211">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "|G0>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
  - label: "|G1>"
    method: sparse_multi_configurational
    superposition:
      - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
  - label: "|G2>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
  - label: "|E>"
    energy: {units: hartree, value: 0.987}
    method: sparse_multi_configurational
    superposition:
      - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
      - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

<span data-ttu-id="d8a94-212">Wenn der Wert der- `method` Eigenschaft ist `unitary_coupled_cluster` , muss das State-Objekt über eine-Eigenschaft verfügen, `cluster_operator` deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-212">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="d8a94-213">Das JSON-Objekt muss über eine-Eigenschaft verfügen, `reference_state` deren Wert ein Basiszustand ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-213">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="d8a94-214">Das JSON-Objekt kann über eine `one_body_amplitudes` -Eigenschaft verfügen, deren Wert ein Array von Einzel Text Cluster-Operatoren und deren Verstärkung ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-214">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="d8a94-215">Das JSON-Objekt verfügt möglicherweise über eine `two_body_amplitudes` -Eigenschaft, deren Wert ein Array von zwei Text Cluster Operatoren und deren Verstärkung ist.</span><span class="sxs-lookup"><span data-stu-id="d8a94-215">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="d8a94-216">, das ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.</span><span class="sxs-lookup"><span data-stu-id="d8a94-216">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="d8a94-217">Beispielsweise der Status $ $ \ket{\text{Reference}} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket {0} , $ $</span><span class="sxs-lookup"><span data-stu-id="d8a94-217">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="d8a94-218">$ $ \ket{\text{UCCSD}} = e ^ {T-t ^ \dagger}\ket{\text{Reference}}, $ $</span><span class="sxs-lookup"><span data-stu-id="d8a94-218">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="d8a94-219">$ $ T = 0,1 a ^ {\dagger} \_ {3, \uparrow}a \_ {2, \downarrow} + 0,2 a ^ {\dagger} \_ {2, \uparrow}a \_ {2, \downarrow}-0,3 a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \downarrow}a \_ {3, \uparrow}a \_ {2, \downarrow} $ $ wird dargestellt durch</span><span class="sxs-lookup"><span data-stu-id="d8a94-219">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "UCCSD"
    method: unitary_coupled_cluster
    cluster_operator: # Initial state that cluster operator is applied to.
        reference_state: 
          [1.0, "(1a)+", "(2a)+", "(2b)+", '|vacuum>']
        one_body_amplitudes: # A one-body cluster term is t^{q}_{p} a^\dag_p a_q   
            - [0.1, "(3a)+", "(2b)"]
            - [-0.2, "(2a)+", "(2b)"]
        two_body_amplitudes: # A two-body unitary cluster term is t^{rs}_{pq} a^\dag_p a^\dag_q a_r a_s
            - [-0.3, "(1a)+", "(3b)+", "(3a)", "(2b)"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="d8a94-220">Basis Objekt festlegen</span><span class="sxs-lookup"><span data-stu-id="d8a94-220">Basis Set Object</span></span> ####

<span data-ttu-id="d8a94-221">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-221">This section is normative.</span></span>

<span data-ttu-id="d8a94-222">Jedes Problem Beschreibungs Objekt kann eine `basis_set` Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-222">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="d8a94-223">Falls vorhanden, muss der Wert der `basis_set` -Eigenschaft ein-Objekt mit zwei Eigenschaften, `type` und sein `name` .</span><span class="sxs-lookup"><span data-stu-id="d8a94-223">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="d8a94-224">Die Basisfunktionen, die durch den Wert der- `basis_set` Eigenschaft identifiziert werden, müssen einen echten Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8a94-224">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="d8a94-225">Die Annahme, dass alle Basisfunktionen in Wirklichkeit sind, kann in zukünftigen Versionen dieser Spezifikation gelockert werden.</span><span class="sxs-lookup"><span data-stu-id="d8a94-225">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="d8a94-226">Tabellen und Listen</span><span class="sxs-lookup"><span data-stu-id="d8a94-226">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="d8a94-227">Tabelle 1.</span><span class="sxs-lookup"><span data-stu-id="d8a94-227">Table 1.</span></span> <span data-ttu-id="d8a94-228">Zulässige physische Einheiten</span><span class="sxs-lookup"><span data-stu-id="d8a94-228">Allowed Physical Units</span></span> ###

<span data-ttu-id="d8a94-229">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-229">This section is normative.</span></span>

<span data-ttu-id="d8a94-230">Jede Zeichenfolge, die eine Einheit angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="d8a94-230">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="d8a94-231">Parser und Producer müssen die folgenden einfachen Mengen Objekte als gleichwertig behandeln:</span><span class="sxs-lookup"><span data-stu-id="d8a94-231">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="d8a94-232">Tabelle 2:</span><span class="sxs-lookup"><span data-stu-id="d8a94-232">Table 2.</span></span> <span data-ttu-id="d8a94-233">Zulässige Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="d8a94-233">Allowed Index Conventions</span></span> ###

<span data-ttu-id="d8a94-234">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-234">This section is normative.</span></span>

<span data-ttu-id="d8a94-235">Jede Zeichenfolge, die eine Index Konvention angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="d8a94-235">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="d8a94-236">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-236">This section is informative.</span></span>

<span data-ttu-id="d8a94-237">In zukünftigen Versionen dieser Spezifikation können zusätzliche Index Konventionen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8a94-237">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="d8a94-238">Interpretation von Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="d8a94-238">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="d8a94-239">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-239">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="d8a94-240">Tabelle 3:</span><span class="sxs-lookup"><span data-stu-id="d8a94-240">Table 3.</span></span> <span data-ttu-id="d8a94-241">Zulässige Zustands Methoden</span><span class="sxs-lookup"><span data-stu-id="d8a94-241">Allowed State methods</span></span> ###

<span data-ttu-id="d8a94-242">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-242">This section is normative.</span></span>

<span data-ttu-id="d8a94-243">Jede Zeichenfolge, die eine Zustands Methode angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="d8a94-243">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="d8a94-244">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="d8a94-244">This section is informative.</span></span>

<span data-ttu-id="d8a94-245">Weitere Zustands Methoden können in zukünftigen Versionen dieser Spezifikation eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8a94-245">Additional state methods may be introduced in future versions of this specification.</span></span>
