---
title: Broombridge-Schema Spezifikation (ver 0,1)
description: Erläutert die Spezifikationen für das broombridge-Quantum-Schema v 0,1 für die Microsoft Quantum Chemistry Library.
author: cgranade
ms.author: chgranad
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
no-loc:
- Q#
- $$v
ms.openlocfilehash: b99c90c434958f7b04712580789b203766cd084d
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835739"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="c0c65-103">Broombridge-Spezifikation v 0,1</span><span class="sxs-lookup"><span data-stu-id="c0c65-103">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="c0c65-104">Die Schlüsselwörter "muss", "darf nicht", "erforderlich", "soll", "soll nicht", "sollte", "sollte nicht", "empfohlen", "Mai" und "optional" in diesem Dokument interpretiert werden, wie in [RFC 2119](https://tools.ietf.org/html/rfc2119)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0c65-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="c0c65-105">Jede Rand Leiste mit den Überschriften "Note", "Information" oder "Warning" ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="c0c65-106">Einführung</span><span class="sxs-lookup"><span data-stu-id="c0c65-106">Introduction</span></span> ##

<span data-ttu-id="c0c65-107">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-107">This section is informative.</span></span>

<span data-ttu-id="c0c65-108">Broombridge-Dokumente sollen Instanzen von Simulations Problemen in der Quantum-Chemie für die Verarbeitung mithilfe der Quantum-Simulation und der Programmier Toolkette kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="c0c65-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="c0c65-109">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="c0c65-109">Serialization</span></span> ##

<span data-ttu-id="c0c65-110">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-110">This section is normative.</span></span>

<span data-ttu-id="c0c65-111">Ein broombridge-Dokument muss als [YAML 1,2-Dokument](http://yaml.org/spec/) serialisiert werden, das ein JSON-Objekt darstellt, wie in [RFC 4627](https://tools.ietf.org/html/rfc4627) Abschnitt 2,2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0c65-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="c0c65-112">Das in YAML serialisierte-Objekt muss über eine `"$schema"` -Eigenschaft verfügen, deren Wert ist `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"` und gemäß den Spezifikationen des JSON-Schema Entwurfs-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)] gültig sein muss.</span><span class="sxs-lookup"><span data-stu-id="c0c65-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="c0c65-113">Im restlichen Teil dieser Spezifikation verweist "das broombridge-Objekt" auf das JSON-Objekt, das aus einem broombridge-YAML-Dokument deserialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c0c65-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="c0c65-114">Sofern nicht anders angegeben, dürfen Objekte keine zusätzlichen Eigenschaften aufweisen, die über die explizit in diesem Dokument angegebenen verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="c0c65-115">Zusätzliche Definitionen</span><span class="sxs-lookup"><span data-stu-id="c0c65-115">Additional Definitions</span></span> ##

<span data-ttu-id="c0c65-116">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="c0c65-117">Mengen Objekte</span><span class="sxs-lookup"><span data-stu-id="c0c65-117">Quantity Objects</span></span> ###

<span data-ttu-id="c0c65-118">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-118">This section is normative.</span></span>

<span data-ttu-id="c0c65-119">Bei einem _Mengen Objekt_ handelt es sich um ein JSON-Objekt, und es muss über eine Eigenschaft verfügen, `units` deren Wert einem der in Tabelle 1 aufgeführten zulässigen Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="c0c65-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="c0c65-120">Ein Mengen Objekt ist ein _einfaches Mengen Objekt_ , wenn es über eine einzelne Eigenschaft `value` zusätzlich zu seiner- `units` Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="c0c65-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="c0c65-121">Der Wert der- `value` Eigenschaft muss eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="c0c65-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="c0c65-122">Bei einem Mengen Objekt handelt es sich um ein _Objekt mit begrenzter Menge_ , wenn es über die Eigenschaften `lower` und `upper` zusätzlich zur- `units` Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="c0c65-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="c0c65-123">Die Werte der `lower` Eigenschaften und `upper` müssen zahlen sein.</span><span class="sxs-lookup"><span data-stu-id="c0c65-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="c0c65-124">Ein Objekt mit begrenzter Menge kann über eine Eigenschaft verfügen, `value` deren Wert eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="c0c65-125">Bei einem Mengen Objekt handelt es sich um ein _Array Objekt_ mit geringer Dichte `format` , wenn die-Eigenschaft und eine-Eigenschaft `values` zusätzlich zur-Eigenschaft aufweisen `units` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="c0c65-126">Der Wert von `format` muss die Zeichenfolge sein `sparse` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="c0c65-127">Der Wert der `values` Eigenschaft muss ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="c0c65-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="c0c65-128">Jedes Element von `values` muss ein Array sein, das die Indizes und den Wert der Menge an Arrays mit geringer Dichte darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0c65-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="c0c65-129">Die Indizes für jedes Element eines Arrays mit geringer Dichte Menge müssen innerhalb des gesamten Objekts mit geringer Dichte Menge eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c0c65-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="c0c65-130">Wenn ein Index mit dem Wert vorhanden ist `0` , muss ein Parser das Mengen Objekt mit geringer Dichte mit einem Array mit geringer Menge an Mengen Objekten behandeln, in dem dieser Index überhaupt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="c0c65-131">Ein Mengen Objekt muss entweder</span><span class="sxs-lookup"><span data-stu-id="c0c65-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="c0c65-132">ein einfaches Mengen Objekt,</span><span class="sxs-lookup"><span data-stu-id="c0c65-132">a simple quantity object,</span></span>
- <span data-ttu-id="c0c65-133">ein Objekt mit begrenzter Menge oder</span><span class="sxs-lookup"><span data-stu-id="c0c65-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="c0c65-134">ein Mengen Objekt mit geringer Dichte.</span><span class="sxs-lookup"><span data-stu-id="c0c65-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="c0c65-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0c65-135">Examples</span></span> ###

<span data-ttu-id="c0c65-136">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-136">This section is informative.</span></span>

<span data-ttu-id="c0c65-137">Eine einfache Menge, die $1.9844146837 \, \mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="c0c65-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="c0c65-138">Eine begrenzte Menge, die eine einheitliche Verteilung im Intervall von $ [-7,-6] \, \mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="c0c65-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="c0c65-139">Im folgenden finden Sie eine Array Menge mit geringer Dichte, bei der ein `[1, 2]` -Element gleich ist `hello` und ein-Element `[3, 4]` gleich ist `world` :</span><span class="sxs-lookup"><span data-stu-id="c0c65-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="c0c65-140">Abschnitt "Format"</span><span class="sxs-lookup"><span data-stu-id="c0c65-140">Format Section</span></span> ##

<span data-ttu-id="c0c65-141">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-141">This section is normative.</span></span>

<span data-ttu-id="c0c65-142">Das broombridge-Objekt muss über eine-Eigenschaft verfügen, `format` deren Wert ein JSON-Objekt mit einer Eigenschaft namens ist `version` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="c0c65-143">Die- `version` Eigenschaft muss den Wert aufweisen `"0.1"` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-143">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="c0c65-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0c65-144">Example</span></span> ###

<span data-ttu-id="c0c65-145">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="c0c65-146">Abschnitt ganzzahlige Sätze</span><span class="sxs-lookup"><span data-stu-id="c0c65-146">Integral Sets Section</span></span> ##

<span data-ttu-id="c0c65-147">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-147">This section is normative.</span></span>

<span data-ttu-id="c0c65-148">Das broombridge-Objekt muss über eine Eigenschaft verfügen, `integral_sets` deren Wert ein JSON-Array ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-148">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="c0c65-149">Jedes Element im Wert der- `integral_sets` Eigenschaft muss ein JSON-Objekt sein, das einen Satz von inteden beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0c65-149">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="c0c65-150">Im restlichen Teil dieses Abschnitts verweist der Begriff "Integral Set Object" auf ein Element im Wert der- `integral_sets` Eigenschaft des broombridge-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c0c65-150">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="c0c65-151">Jedes integrale Set-Objekt muss über eine-Eigenschaft verfügen, `metadata` deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-151">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="c0c65-152">Der Wert von `metadata` kann das leere JSON-Objekt (d. h `{}` .) sein oder zusätzliche Eigenschaften enthalten, die durch den implemenor definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0c65-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="c0c65-153">Hamiltona-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c0c65-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="c0c65-154">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c0c65-154">Overview</span></span> ####

<span data-ttu-id="c0c65-155">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-155">This section is informative.</span></span>

<span data-ttu-id="c0c65-156">Die-Eigenschaft der einzelnen ganzzahligen Mengen `hamiltonian` Objekte beschreibt den hamiltonan für ein bestimmtes Quantum-Chemie Problem, indem er seine ein-und zwei Text Begriffe als sparsesrearrays von reellen Zahlen auflistet.</span><span class="sxs-lookup"><span data-stu-id="c0c65-156">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="c0c65-157">Die von jedem integralen Satz Objekt beschriebenen hamiltonan-Operatoren haben das Formular</span><span class="sxs-lookup"><span data-stu-id="c0c65-157">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="c0c65-158">$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparser, \downpfeil \\ }} h \_ \{ IJ \} a ^ \{ \dagger \} \_ {i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, l \} \sum \_ {\sigma, \rho\in \\ {\uparser, \downpfeil \\ }} H \_ {IJKL} a ^ \dagger \_ {i, \sigma} a ^ \dagger \_ {k, \rho} a \_ {l, \rho} a \_ {j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="c0c65-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="c0c65-159">Hier $h _ {IJKL} = (IJ | KL) $ in der Mulliken-Konvention.</span><span class="sxs-lookup"><span data-stu-id="c0c65-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="c0c65-160">Aus Gründen der Übersichtlichkeit lautet der Begriff mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="c0c65-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="c0c65-161">$ $ H_ {IJ} = \int {\mathrm d} x \psi ^ \* \_ i (x) \left (\frac {1} {2} \nabla ^ 2 + \sum \_ {A} \bruchteil {z \_ A} {| x-x \_ A |}  \right) \psi \_ j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="c0c65-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="c0c65-162">und der zwei-Elektronen-Begriff ist</span><span class="sxs-lookup"><span data-stu-id="c0c65-162">and the two-electron term is</span></span>

<span data-ttu-id="c0c65-163">$ $ h \_ \{ IJKL \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \frac \{ 1 \} \{ \| x \_ 1-x \_ 2 \| \} \psi \_ k ^ \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).</span><span class="sxs-lookup"><span data-stu-id="c0c65-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="c0c65-164">Wie in der Beschreibung der- [ `basis_set` Eigenschaft](#basis-set-object) der einzelnen Elemente der- `integral_sets` Eigenschaft erwähnt, wird explizit angenommen, dass die verwendeten Basisfunktionen einen echten Wert haben.</span><span class="sxs-lookup"><span data-stu-id="c0c65-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="c0c65-165">Dies ermöglicht es uns, die folgenden Symmetries zwischen den Begriffen zu verwenden, um die Darstellung der hamiltonan zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="c0c65-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="c0c65-166">$ $ H_ {IJKL} = H_ {IJLK} = H_ {jikl} = H_ {jilk} = H_ {klij} = H_ {klji} = H_ {lkij} = H_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="c0c65-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="c0c65-167">Inhalte</span><span class="sxs-lookup"><span data-stu-id="c0c65-167">Contents</span></span> ####

<span data-ttu-id="c0c65-168">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-168">This section is normative.</span></span>

<span data-ttu-id="c0c65-169">Jede ganzzahlige Menge muss über eine Eigenschaft verfügen, `hamiltonian` deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-169">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="c0c65-170">Der Wert der- `hamiltonian` Eigenschaft wird als "hamiltonan"-Objekt bezeichnet und muss über die Eigenschaften und verfügen, `one_electron_integrals` `two_electron_integrals` wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0c65-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="c0c65-171">Ein hamiltonan-Objekt kann auch über eine-Eigenschaft verfügen `particle_hole_representation` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-171">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="c0c65-172">Falls vorhanden, muss der Wert von `particle_hole_representation` dem im restlichen Teil dieses Abschnitts beschriebenen Format entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-172">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="c0c65-173">Integrale Objekt mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="c0c65-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="c0c65-174">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-174">This section is normative.</span></span>

<span data-ttu-id="c0c65-175">Die- `one_electron_integrals` Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte sein, deren Indizes zwei Ganzzahlen und deren Werte Ziffern sind.</span><span class="sxs-lookup"><span data-stu-id="c0c65-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="c0c65-176">Jeder Begriff muss über Indizes verfügen, `[i, j]` bei denen `i >= j` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="c0c65-177">Nebenbei Dies spiegelt die Symmetrie wider, die $h _ {IJ} = H_ {JI} $ liegt. Dies ist eine Folge der Tatsache, dass der hamiltonan hermitian ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="c0c65-178">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0c65-178">Example</span></span> ######

<span data-ttu-id="c0c65-179">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-179">This section is informative.</span></span>

<span data-ttu-id="c0c65-180">Die folgende Menge an Sparse-Arrays repräsentiert die hamiltonan $ $ H = \left (-5,0 (a ^ \{ \dagger \} \_ {1, \uanrow} a \_ {1, \uparamerow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {1, \downarrow}) + 0,17 (a ^ \{ \dagger \} \_ {2, \uparamerow} a \_ {1, \uparamerow} + a ^ \{ \dagger \} \_ {1, \uanrow} a \_ {2, \uparamerow} + a ^ \{ \dagger \} \_ {2, \downarrow} a \_ {1, \downarrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {2, \downarrow}) \right) \\ , \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="c0c65-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="c0c65-181">Broombridge verwendet die 1-basierte Indizierung.</span><span class="sxs-lookup"><span data-stu-id="c0c65-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="c0c65-182">2-Elektronen-inteals-Objekt</span><span class="sxs-lookup"><span data-stu-id="c0c65-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="c0c65-183">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-183">This section is normative.</span></span>

<span data-ttu-id="c0c65-184">Die- `two_electron_integrals` Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte mit einer zusätzlichen Eigenschaft namens sein `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="c0c65-185">Jedes Element des Werts von `two_electron_integrals` muss über vier Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="c0c65-186">Jede `two_electron_integrals` Eigenschaft muss über eine `index_convention` Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="c0c65-187">Der Wert der- `index_convention` Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 1 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c0c65-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="c0c65-188">Wenn der Wert von `index_convention` ist `mulliken` , dann `two_electron_integrals` muss ein Parser, der ein broombridge-Dokument lädt, für jedes Element der Menge an Sparse-Arrays einen Hamilton-Begriff instanziieren, der mit dem zwei-Elektronen-Operator identisch ist, $h _ {i, j, k, l} a ^ \ dagger_i a ^ \ dagger_j a_k a_l $, wobei $i $, $j $, $k $ und $l $ ganzzahlige Werte im inklusiven Bereich zwischen 1 und der Anzahl der von der-Eigenschaft des ganzzahligen Mengen Objekts angegebenen Elektronen sein müssen `n_electrons` und wobei $h _ {i, j, k, l} $ das Element `[i, j, k, l, h(i, j, k, l)]` der Menge mit geringer Dichte ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="c0c65-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="c0c65-189">Symmetries</span></span> ######

<span data-ttu-id="c0c65-190">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-190">This section is normative.</span></span>

<span data-ttu-id="c0c65-191">Wenn die- `index_convention` Eigenschaft eines- `two_electron_integrals` Objekts gleich ist `mulliken` , dann, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, dürfen die folgenden Indizes nicht vorhanden sein, es sei denn, Sie sind gleich `[i, j, k, l]` :</span><span class="sxs-lookup"><span data-stu-id="c0c65-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="c0c65-192">Da die- `index_convention` Eigenschaft ein Objekt mit geringer Dichte ist, werden möglicherweise keine Indizes für verschiedene Elemente wiederholt.</span><span class="sxs-lookup"><span data-stu-id="c0c65-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="c0c65-193">Insbesondere, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, kann kein anderes Element über diese Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="c0c65-194">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0c65-194">Example</span></span> #######

<span data-ttu-id="c0c65-195">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-195">This section is informative.</span></span>

<span data-ttu-id="c0c65-196">Das folgende Objekt gibt den hamiltonan an.</span><span class="sxs-lookup"><span data-stu-id="c0c65-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="c0c65-197">$$ H = \frac12 \sum \_ {\sigma,\rho\in \\ {\uparrow,\downarrow \\ }}\Biggr( 1.6 a^{\dagger} \_ {1,\sigma} a^{\dagger} \_ {1,\rho} a \_ {1,\rho} a \_ {1,\sigma}- 0.1 a^{\dagger} \_ {6,\sigma} a^{\dagger} \_ {1,\rho} a \_ {3,\rho} a \_ {2,\sigma}- 0.1 a^{\dagger} \_ {6,\sigma} a^{\dagger} \_ {1,\rho} a \_ {2,\rho} a \_ {3,\sigma}- 0.1 a^{\dagger} \_ {1,\sigma} a^{\dagger} \_ {6,\rho} a \_ {3,\rho} a \_ {2,\sigma}- 0.1 a^{\dagger} \_ {1,\sigma} a^{\dagger} \_ {6,\rho} a \_ {2,\rho} a \_ {3,\sigma} $$ $$- 0.1 a^{\dagger} \_ {3,\sigma} a^{\dagger} \_ {2,\rho} a \_ {6,\rho} a \_ {1,\sigma}- 0.1 a^{\dagger} \_ {3,\sigma} a^{\dagger} \_ {2,\rho} a \_ {1,\rho} a \_ {6,\sigma}- 0.1 a^{\dagger} \_ {2,\sigma} a^{\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="c0c65-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

##### <a name="particlehole-representation-object"></a><span data-ttu-id="c0c65-198">Partikel – Loch-Darstellungs Objekt</span><span class="sxs-lookup"><span data-stu-id="c0c65-198">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="c0c65-199">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-199">This section is normative.</span></span>

<span data-ttu-id="c0c65-200">Das Objekt "Partikel – Block-Darstellung" gibt an, dass die gespeicherten inteder in Bezug auf die Darstellung von Partikel Löchern definiert werden, wobei die Erstellungs-und Vernichtungs Operatoren die Entfernung vom verwendeten Verweis Zustand, z. b. einem Hartree – Fock-Zustand, beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c0c65-200">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="c0c65-201">Das-Objekt ist optional.</span><span class="sxs-lookup"><span data-stu-id="c0c65-201">The object is OPTIONAL.</span></span>
<span data-ttu-id="c0c65-202">Wenn das-Objekt nicht angegeben wird, wird die hamiltonan als nicht in der Darstellung eines Partikel Lochs angegeben interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c0c65-202">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="c0c65-203">Falls vorhanden, muss der Wert von `particle_hole_representation` ein Array mit geringer Array Menge sein, dessen Indizes vier ganze Zahlen und deren Werte eine Zahl und eine Zeichenfolge sind.</span><span class="sxs-lookup"><span data-stu-id="c0c65-203">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="c0c65-204">Der Zeichen folgen Teil des Werts der einzelnen Elemente darf nur die Zeichen enthalten `'+'` `'-'` , und gibt an, ob ein angegebener Faktor im Begriff ein Erstellungs-oder Vernichtungs Operator in der Partikel –-Loch Darstellung ist.</span><span class="sxs-lookup"><span data-stu-id="c0c65-204">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="c0c65-205">Beispielsweise `"-+++"` kann coresteiche auf eine Lücke erstellt werden, die an Standort $i $ erstellt wird, und an den Standorten erstellte Partikel $j, k $ und $l $.</span><span class="sxs-lookup"><span data-stu-id="c0c65-205">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c65-206">Da der Wert von `particle_hole_representation` ein Array Objekt mit geringer Dichte ist, `unit` müssen die-Eigenschaft und die-Eigenschaft `format` angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c0c65-206">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="c0c65-207">Zulässige Einheiten sind in Tabelle 1 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0c65-207">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="c0c65-208">Die `format` -Eigenschaft ist erforderlich und gibt an, ob die hamiltona-Koeffizienten als Array mit fester oder geringer Dichte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c0c65-208">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="c0c65-209">In der aktuellen Version werden nur sparsearrays unterstützt, wobei interpretiert wird, dass alle nicht angegebenen Elemente $0 $ sind. zukünftige Versionen können jedoch Unterstützung für zusätzliche Werte der Eigenschaft hinzufügen `format` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-209">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="c0c65-210">Abschnitt "Anfangszustand"</span><span class="sxs-lookup"><span data-stu-id="c0c65-210">Initial State Section</span></span> ###

<span data-ttu-id="c0c65-211">Das initial_state_suggestion-Objekt gibt die anfänglichen Quantum-Zustände an, die für die angegebene hamiltonan von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="c0c65-211">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="c0c65-212">Dieses Objekt muss ein Array von JSON- `state` Objekten sein.</span><span class="sxs-lookup"><span data-stu-id="c0c65-212">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="c0c65-213">State-Objekt</span><span class="sxs-lookup"><span data-stu-id="c0c65-213">State object</span></span> ####

<span data-ttu-id="c0c65-214">Jeder Status stellt eine übergeordnete Position der belegten Orbitals dar.</span><span class="sxs-lookup"><span data-stu-id="c0c65-214">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="c0c65-215">Jedes Zustands Objekt muss über eine Eigenschaft verfügen, die `label` eine Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="c0c65-215">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="c0c65-216">Jedes Zustands Objekt muss über eine Eigenschaft verfügen, die `superposition` ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.</span><span class="sxs-lookup"><span data-stu-id="c0c65-216">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="c0c65-217">Der anfängliche Status lautet z. b. $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket $ $ $ {0} \ket{e} = \bruchteil {0,1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0.2 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0.2 | ^ 2}} \ket {0} $ $ wird dargestellt durch</span><span class="sxs-lookup"><span data-stu-id="c0c65-217">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
    - state:
        label: "|G0>"
        superposition:
            - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G1>"
        superposition:
            - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G2>"
        superposition:
            - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
    - state:
        label: "|E>"
        superposition:
            - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
            - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="c0c65-218">Basis Objekt festlegen</span><span class="sxs-lookup"><span data-stu-id="c0c65-218">Basis Set Object</span></span> ####

<span data-ttu-id="c0c65-219">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-219">This section is normative.</span></span>

<span data-ttu-id="c0c65-220">Jedes ganzzahlige Set-Objekt kann über eine- `basis_set` Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-220">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="c0c65-221">Falls vorhanden, muss der Wert der `basis_set` -Eigenschaft ein-Objekt mit zwei Eigenschaften, `type` und sein `name` .</span><span class="sxs-lookup"><span data-stu-id="c0c65-221">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="c0c65-222">Die Basisfunktionen, die durch den Wert der- `basis_set` Eigenschaft identifiziert werden, müssen einen echten Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c0c65-222">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c65-223">Die Annahme, dass alle Basisfunktionen in Wirklichkeit sind, kann in zukünftigen Versionen dieser Spezifikation gelockert werden.</span><span class="sxs-lookup"><span data-stu-id="c0c65-223">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="c0c65-224">Tabellen und Listen</span><span class="sxs-lookup"><span data-stu-id="c0c65-224">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="c0c65-225">Tabelle 1.</span><span class="sxs-lookup"><span data-stu-id="c0c65-225">Table 1.</span></span> <span data-ttu-id="c0c65-226">Zulässige physische Einheiten</span><span class="sxs-lookup"><span data-stu-id="c0c65-226">Allowed Physical Units</span></span> ###

<span data-ttu-id="c0c65-227">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-227">This section is normative.</span></span>

<span data-ttu-id="c0c65-228">Jede Zeichenfolge, die eine Einheit angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="c0c65-228">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="c0c65-229">Parser und Producer müssen die folgenden einfachen Mengen Objekte als gleichwertig behandeln:</span><span class="sxs-lookup"><span data-stu-id="c0c65-229">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="c0c65-230">Tabelle 2:</span><span class="sxs-lookup"><span data-stu-id="c0c65-230">Table 2.</span></span> <span data-ttu-id="c0c65-231">Zulässige Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="c0c65-231">Allowed Index Conventions</span></span> ###

<span data-ttu-id="c0c65-232">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-232">This section is normative.</span></span>

<span data-ttu-id="c0c65-233">Jede Zeichenfolge, die eine Index Konvention angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="c0c65-233">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="c0c65-234">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-234">This section is informative.</span></span>

<span data-ttu-id="c0c65-235">In zukünftigen Versionen dieser Spezifikation können zusätzliche Index Konventionen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c0c65-235">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="c0c65-236">Interpretation von Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="c0c65-236">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="c0c65-237">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c0c65-237">This section is informative.</span></span>
