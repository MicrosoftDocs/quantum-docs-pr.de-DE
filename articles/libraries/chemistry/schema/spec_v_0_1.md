---
title: Broombridge-Schema Spezifikation
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
ms.openlocfilehash: a950e04d44e5de8091b034214258d2c2fa663f58
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185357"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="c4a2c-102">Broombridge-Spezifikation v 0,1</span><span class="sxs-lookup"><span data-stu-id="c4a2c-102">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="c4a2c-103">Die Schlüsselwörter "muss", "darf nicht", "erforderlich", "soll", "soll nicht", "sollte", "sollte nicht", "empfohlen", "Mai" und "optional" in diesem Dokument interpretiert werden, wie in [RFC 2119](https://tools.ietf.org/html/rfc2119)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="c4a2c-104">Jede Rand Leiste mit den Überschriften "Note", "Information" oder "Warning" ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="c4a2c-105">Einführung</span><span class="sxs-lookup"><span data-stu-id="c4a2c-105">Introduction</span></span> ##

<span data-ttu-id="c4a2c-106">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-106">This section is informative.</span></span>

<span data-ttu-id="c4a2c-107">Broombridge-Dokumente sollen Instanzen von Simulations Problemen in der Quantum-Chemie für die Verarbeitung mithilfe der Quantum-Simulation und der Programmier Toolkette kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="c4a2c-108">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="c4a2c-108">Serialization</span></span> ##

<span data-ttu-id="c4a2c-109">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-109">This section is normative.</span></span>

<span data-ttu-id="c4a2c-110">Ein broombridge-Dokument muss als [YAML 1,2-Dokument](http://yaml.org/spec/) serialisiert werden, das ein JSON-Objekt darstellt, wie in [RFC 4627](https://tools.ietf.org/html/rfc4627) Abschnitt 2,2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="c4a2c-111">Das an YAML serialisierte Objekt muss über eine Eigenschaft `"$schema"` verfügen, deren Wert `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`ist und gemäß den Spezifikationen des JSON-Schema Entwurfs-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)] gültig sein muss.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="c4a2c-112">Im restlichen Teil dieser Spezifikation verweist "das broombridge-Objekt" auf das JSON-Objekt, das aus einem broombridge-YAML-Dokument deserialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="c4a2c-113">Sofern nicht anders angegeben, dürfen Objekte keine zusätzlichen Eigenschaften aufweisen, die über die explizit in diesem Dokument angegebenen verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="c4a2c-114">Weitere Definitionen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-114">Additional Definitions</span></span> ##

<span data-ttu-id="c4a2c-115">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="c4a2c-116">Mengen Objekte</span><span class="sxs-lookup"><span data-stu-id="c4a2c-116">Quantity Objects</span></span> ###

<span data-ttu-id="c4a2c-117">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-117">This section is normative.</span></span>

<span data-ttu-id="c4a2c-118">Bei einem _Mengen Objekt_ handelt es sich um ein JSON-Objekt, und es muss über eine Eigenschaft `units` verfügen, deren Wert einem der in Tabelle 1 aufgeführten zulässigen Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="c4a2c-119">Bei einem Mengen Objekt handelt es sich um ein _einfaches Mengen Objekt_ , wenn zusätzlich zu seiner `units`-Eigenschaft eine einzelne Eigenschaft `value`.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="c4a2c-120">Der Wert der `value`-Eigenschaft muss eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="c4a2c-121">Ein Mengen Objekt ist ein gebundenes _Mengen_ Objekt, wenn es über die Eigenschaften `lower` und `upper` zusätzlich zu seiner `units` Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="c4a2c-122">Die Werte der Eigenschaften `lower` und `upper` müssen zahlen sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="c4a2c-123">Ein Objekt mit begrenzter Menge kann eine Eigenschaft `value` haben, deren Wert eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="c4a2c-124">Bei einem Mengen Objekt handelt es sich um ein _Array Objekt_ mit geringer Dichte, wenn es die-Eigenschaft `format` und eine-Eigenschaft `values` zusätzlich zu seiner `units`-Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="c4a2c-125">Der Wert von `format` muss die Zeichenfolge `sparse`sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="c4a2c-126">Der Wert der `values`-Eigenschaft muss ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="c4a2c-127">Jedes Element von `values` muss ein Array sein, das die Indizes und den Wert der Menge an Arrays mit geringer Dichte darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="c4a2c-128">Die Indizes für jedes Element eines Arrays mit geringer Dichte Menge müssen innerhalb des gesamten Objekts mit geringer Dichte Menge eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="c4a2c-129">Wenn ein Index mit dem Wert `0`vorhanden ist, muss ein Parser das Mengen Objekt mit geringer Dichte mit einem Array mit geringer Menge an Mengen Objekten behandeln, in dem dieser Index überhaupt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="c4a2c-130">Ein Mengen Objekt muss entweder</span><span class="sxs-lookup"><span data-stu-id="c4a2c-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="c4a2c-131">ein einfaches Mengen Objekt,</span><span class="sxs-lookup"><span data-stu-id="c4a2c-131">a simple quantity object,</span></span>
- <span data-ttu-id="c4a2c-132">ein Objekt mit begrenzter Menge oder</span><span class="sxs-lookup"><span data-stu-id="c4a2c-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="c4a2c-133">ein Mengen Objekt mit geringer Dichte.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="c4a2c-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4a2c-134">Examples</span></span> ###

<span data-ttu-id="c4a2c-135">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-135">This section is informative.</span></span>

<span data-ttu-id="c4a2c-136">Eine einfache Menge, die $1.9844146837\,\mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="c4a2c-137">Eine begrenzte Menge, die eine einheitliche Verteilung im Intervall von $ [-7,-6]\,\mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="c4a2c-138">Im folgenden finden Sie eine Array Menge mit geringer Dichte, bei der ein-Element `[1, 2]` gleich `hello` und ein-Element `[3, 4]` gleich `world`sind:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="c4a2c-139">Abschnitt "Format"</span><span class="sxs-lookup"><span data-stu-id="c4a2c-139">Format Section</span></span> ##

<span data-ttu-id="c4a2c-140">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-140">This section is normative.</span></span>

<span data-ttu-id="c4a2c-141">Das broombridge-Objekt muss über eine Eigenschaft `format` verfügen, deren Wert ein JSON-Objekt mit einer Eigenschaft namens `version`ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="c4a2c-142">Die `version`-Eigenschaft muss den Wert `"0.1"`haben.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-142">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="c4a2c-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4a2c-143">Example</span></span> ###

<span data-ttu-id="c4a2c-144">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="c4a2c-145">Abschnitt ganzzahlige Sätze</span><span class="sxs-lookup"><span data-stu-id="c4a2c-145">Integral Sets Section</span></span> ##

<span data-ttu-id="c4a2c-146">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-146">This section is normative.</span></span>

<span data-ttu-id="c4a2c-147">Das broombridge-Objekt muss über eine Eigenschaft `integral_sets` verfügen, deren Wert ein JSON-Array ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-147">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="c4a2c-148">Jedes Element im Wert der `integral_sets`-Eigenschaft muss ein JSON-Objekt sein, das einen Satz von inteden beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-148">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="c4a2c-149">Im restlichen Teil dieses Abschnitts verweist der Begriff "Integral Set Object" auf ein Element im Wert der `integral_sets`-Eigenschaft des broombridge-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-149">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="c4a2c-150">Jedes ganzzahlige Set-Objekt muss über eine Eigenschaft `metadata` verfügen, deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-150">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="c4a2c-151">Der Wert von `metadata` kann das leere JSON-Objekt (`{}`) sein oder zusätzliche Eigenschaften enthalten, die durch den implemenor definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="c4a2c-152">Hamiltona-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c4a2c-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="c4a2c-153">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c4a2c-153">Overview</span></span> ####

<span data-ttu-id="c4a2c-154">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-154">This section is informative.</span></span>

<span data-ttu-id="c4a2c-155">Die `hamiltonian`-Eigenschaft jedes ganzzahligen Mengen Objekts beschreibt den hamiltonan für ein bestimmtes Quantum-Chemie Problem, indem er seine ein-und zwei Text Begriffe als sparsesreellen von reellen Zahlen auflistet.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-155">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="c4a2c-156">Die von jedem integralen Satz Objekt beschriebenen hamiltonan-Operatoren haben das Formular</span><span class="sxs-lookup"><span data-stu-id="c4a2c-156">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="c4a2c-157">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparamerow, \downpfeil\\}} h\_\{IJ\} a ^\{\dagger\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparser, \downpfeil\\}} h\_{IJKL} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l, \rho} a\_{j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="c4a2c-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="c4a2c-158">Hier $h _ {IJKL} = (IJ | KL) $ in der Mulliken-Konvention.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="c4a2c-159">Aus Gründen der Übersichtlichkeit lautet der Begriff mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="c4a2c-160">$ $ H_ {IJ} = \int {\mathrm d} x \psi ^ \*\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \bruchteil {z\_a} {| x-x\_a |}  \right) \psi\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="c4a2c-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="c4a2c-161">und der zwei-Elektronen-Begriff ist</span><span class="sxs-lookup"><span data-stu-id="c4a2c-161">and the two-electron term is</span></span>

<span data-ttu-id="c4a2c-162">$ $ h\_\{IJKL\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="c4a2c-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="c4a2c-163">Wie in der Beschreibung der`basis_set`- [Eigenschaft](#basis-set-object) der einzelnen Elemente der `integral_sets`-Eigenschaft erwähnt, wird explizit angenommen, dass die verwendeten Basisfunktionen einen echten Wert haben.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="c4a2c-164">Dies ermöglicht es uns, die folgenden Symmetries zwischen den Begriffen zu verwenden, um die Darstellung der hamiltonan zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="c4a2c-165">$ $ H_ {IJKL} = H_ {IJLK} = H_ {jikl} = H_ {jilk} = H_ {klij} = H_ {klji} = H_ {lkij} = H_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="c4a2c-166">Inhalt</span><span class="sxs-lookup"><span data-stu-id="c4a2c-166">Contents</span></span> ####

<span data-ttu-id="c4a2c-167">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-167">This section is normative.</span></span>

<span data-ttu-id="c4a2c-168">Jede ganzzahlige Menge muss eine Eigenschaft `hamiltonian` haben, deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-168">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="c4a2c-169">Der Wert der `hamiltonian`-Eigenschaft wird als "hamiltonan" bezeichnet und muss die Eigenschaften `one_electron_integrals` und `two_electron_integrals` aufweisen, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="c4a2c-170">Ein hamiltonan-Objekt kann auch über eine `particle_hole_representation`-Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-170">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="c4a2c-171">Falls vorhanden, muss der Wert von `particle_hole_representation` dem im restlichen Teil dieses Abschnitts beschriebenen Format entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-171">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="c4a2c-172">Integrale Objekt mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-172">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="c4a2c-173">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-173">This section is normative.</span></span>

<span data-ttu-id="c4a2c-174">Die `one_electron_integrals`-Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte sein, deren Indizes zwei Ganzzahlen und deren Werte Ziffern sind.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-174">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="c4a2c-175">Jeder Begriff muss über Indizes `[i, j]`, wo `i >= j`.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-175">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="c4a2c-176">Nebenbei Dies spiegelt die Symmetrie wider, die $h _ {IJ} = H_ {JI} $ liegt. Dies ist eine Folge der Tatsache, dass der hamiltonan hermitian ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-176">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="c4a2c-177">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4a2c-177">Example</span></span> ######

<span data-ttu-id="c4a2c-178">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-178">This section is informative.</span></span>

<span data-ttu-id="c4a2c-179">Die folgende Menge an Arrays mit geringer Dichte repräsentiert das hamiltonan $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1 , \downarrow}) + 0,17 (a ^\{\dagger\}\_{2, \uparamerow} a\_{1, \uanrow} + a ^\{\dagger\}\_{1, \uparamerow} a\_{2, \uparamerow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-179">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="c4a2c-180">Broombridge verwendet die 1-basierte Indizierung.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-180">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="c4a2c-181">2-Elektronen-inteals-Objekt</span><span class="sxs-lookup"><span data-stu-id="c4a2c-181">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="c4a2c-182">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-182">This section is normative.</span></span>

<span data-ttu-id="c4a2c-183">Die `two_electron_integrals`-Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte mit einer zusätzlichen Eigenschaft namens `index_convention`sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-183">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="c4a2c-184">Jedes Element des Werts `two_electron_integrals` muss vier Indizes aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-184">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="c4a2c-185">Jede `two_electron_integrals` Eigenschaft muss über eine `index_convention`-Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-185">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="c4a2c-186">Der Wert der `index_convention`-Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 1 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-186">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="c4a2c-187">Wenn der Wert von `index_convention` `mulliken`ist, muss ein Parser, der ein broombridge-Dokument lädt, für jedes Element der Menge der `two_electron_integrals` Sparse-Arrays einen Hamilton-Begriff instanziieren, der mit dem zwei-Elektronen-Operator identisch ist $h _ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k a_l $ , wobei $i $, $j $, $k $ und $l $ ganzzahlige Werte im inklusiven Bereich zwischen 1 und der Anzahl der von der `n_electrons`-Eigenschaft des ganzzahligen festgelegten Objekts angegebenen Elektronen sein müssen und wobei $h _ {i, j, k, l} $ das Element `[i, j, k, l, h(i, j, k, l)]` der Menge an geringer Dichte ist.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-187">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="c4a2c-188">Symmetries</span><span class="sxs-lookup"><span data-stu-id="c4a2c-188">Symmetries</span></span> ######

<span data-ttu-id="c4a2c-189">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-189">This section is normative.</span></span>

<span data-ttu-id="c4a2c-190">Wenn die `index_convention`-Eigenschaft eines `two_electron_integrals` Objekts gleich `mulliken`ist und ein Element mit Indizes `[i, j, k, l]` vorhanden ist, dürfen die folgenden Indizes nur vorhanden sein, wenn Sie `[i, j, k, l]`sind:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-190">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="c4a2c-191">Da die `index_convention`-Eigenschaft ein Objekt mit geringer Menge ist, können für unterschiedliche Elemente keine Indizes wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-191">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="c4a2c-192">Insbesondere, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, kann kein anderes Element über diese Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-192">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="c4a2c-193">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4a2c-193">Example</span></span> #######

<span data-ttu-id="c4a2c-194">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-194">This section is informative.</span></span>

<span data-ttu-id="c4a2c-195">Das folgende Objekt gibt den hamiltonan an.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-195">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="c4a2c-196">$ $ H = \bruch12 \sum\_{\sigma, \rho\in\\{\ubirow, \downpfeil\\}} \biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{2 , \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1, \rho} a\_{6, \sigma}\Biggr)\\, \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-196">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

##### <a name="particlehole-representation-object"></a><span data-ttu-id="c4a2c-197">Partikel – Loch-Darstellungs Objekt</span><span class="sxs-lookup"><span data-stu-id="c4a2c-197">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="c4a2c-198">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-198">This section is normative.</span></span>

<span data-ttu-id="c4a2c-199">Das Objekt "Partikel – Hole-Darstellung" gibt an, dass die gespeicherten inteder in Bezug auf die Darstellung von Partikel Löchern definiert werden, wobei die Erstellungs-und Vernichtungs Operatoren die Entfernung vom verwendeten Verweis Zustand (z. b. einer Hartree) beschreiben. Fock-Zustand.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-199">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="c4a2c-200">Das-Objekt ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-200">The object is OPTIONAL.</span></span>
<span data-ttu-id="c4a2c-201">Wenn das-Objekt nicht angegeben wird, wird die hamiltonan als nicht in der Darstellung eines Partikel Lochs angegeben interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-201">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="c4a2c-202">Falls vorhanden, muss der Wert `particle_hole_representation` ein Array mit geringer Array Menge sein, dessen Indizes vier ganze Zahlen und deren Werte eine Zahl und eine Zeichenfolge sind.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-202">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="c4a2c-203">Der Zeichen folgen Teil des Werts der einzelnen Elemente darf nur die Zeichen `'+'` und `'-'` enthalten, der angibt, ob es sich bei einem angegebenen Faktor im Begriff um einen Erstellungs-oder Vernichtungs Operator in der Partikel – Loch-Darstellung handelt.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-203">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="c4a2c-204">Beispielsweise `"-+++"` coresteiche auf eine Lücke, die an Site $i $ erstellt wird, und an den Standorten erstellte Partikel $j, k $ und $l $.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-204">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="c4a2c-205">Da der Wert des `particle_hole_representation` ein Array Objekt mit geringer Dichte ist, müssen die Eigenschaften `unit` und `format` angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-205">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="c4a2c-206">Zulässige Einheiten sind in Tabelle 1 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-206">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="c4a2c-207">Die `format`-Eigenschaft ist erforderlich und gibt an, ob die hamiltona-Koeffizienten als Array mit fester oder geringer Dichte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-207">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="c4a2c-208">In der aktuellen Version werden nur sparsearrays unterstützt, wobei interpretiert wird, dass alle nicht angegebenen Elemente $0 $ sind. zukünftige Versionen können jedoch Unterstützung für zusätzliche Werte der `format`-Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-208">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="c4a2c-209">Abschnitt "Anfangszustand"</span><span class="sxs-lookup"><span data-stu-id="c4a2c-209">Initial State Section</span></span> ###

<span data-ttu-id="c4a2c-210">Das initial_state_suggestion-Objekt gibt die anfänglichen Quantum-Zustände an, die für die angegebene hamiltonan von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-210">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="c4a2c-211">Bei diesem Objekt muss es sich um ein Array von JSON-`state` Objekten handeln.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-211">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="c4a2c-212">State-Objekt</span><span class="sxs-lookup"><span data-stu-id="c4a2c-212">State object</span></span> ####

<span data-ttu-id="c4a2c-213">Jeder Status stellt eine übergeordnete Position der belegten Orbitals dar.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-213">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="c4a2c-214">Jedes Zustands Objekt muss über eine `label`-Eigenschaft verfügen, die eine Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-214">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="c4a2c-215">Jedes Zustands Objekt muss über eine `superposition`-Eigenschaft verfügen, die ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-215">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="c4a2c-216">Der anfängliche Status lautet z. b. $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{e} = \bruchteil {0,1 (a ^ {\dagger}\_{1 , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket{0} $ $ dargestellt durch</span><span class="sxs-lookup"><span data-stu-id="c4a2c-216">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
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

#### <a name="basis-set-object"></a><span data-ttu-id="c4a2c-217">Basis Objekt festlegen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-217">Basis Set Object</span></span> ####

<span data-ttu-id="c4a2c-218">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-218">This section is normative.</span></span>

<span data-ttu-id="c4a2c-219">Jedes ganzzahlige Set-Objekt kann über eine `basis_set`-Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-219">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="c4a2c-220">Wenn der Wert der `basis_set`-Eigenschaft vorhanden ist, muss es sich um ein Objekt mit zwei Eigenschaften handeln, `type` und `name`.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-220">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="c4a2c-221">Die Basisfunktionen, die durch den Wert der `basis_set`-Eigenschaft identifiziert werden, müssen ein echter Wert sein.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-221">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="c4a2c-222">Die Annahme, dass alle Basisfunktionen in Wirklichkeit sind, kann in zukünftigen Versionen dieser Spezifikation gelockert werden.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-222">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="c4a2c-223">Tabellen und Listen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-223">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="c4a2c-224">Tabelle 1.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-224">Table 1.</span></span> <span data-ttu-id="c4a2c-225">Zulässige physische Einheiten</span><span class="sxs-lookup"><span data-stu-id="c4a2c-225">Allowed Physical Units</span></span> ###

<span data-ttu-id="c4a2c-226">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-226">This section is normative.</span></span>

<span data-ttu-id="c4a2c-227">Jede Zeichenfolge, die eine Einheit angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-227">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="c4a2c-228">Parser und Producer müssen die folgenden einfachen Mengen Objekte als gleichwertig behandeln:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-228">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="c4a2c-229">Tabelle 2:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-229">Table 2.</span></span> <span data-ttu-id="c4a2c-230">Zulässige Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-230">Allowed Index Conventions</span></span> ###

<span data-ttu-id="c4a2c-231">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-231">This section is normative.</span></span>

<span data-ttu-id="c4a2c-232">Jede Zeichenfolge, die eine Index Konvention angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="c4a2c-232">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="c4a2c-233">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-233">This section is informative.</span></span>

<span data-ttu-id="c4a2c-234">In zukünftigen Versionen dieser Spezifikation können zusätzliche Index Konventionen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-234">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="c4a2c-235">Interpretation von Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="c4a2c-235">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="c4a2c-236">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="c4a2c-236">This section is informative.</span></span>
