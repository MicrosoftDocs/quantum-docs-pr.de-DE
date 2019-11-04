---
title: Broombridge-Schema Spezifikation
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
ms.openlocfilehash: 2f4be96bc6f1e8e6fe21b93bc0d9ab2aa367fd53
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185306"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="84637-102">Broombridge-Spezifikation v 0,2</span><span class="sxs-lookup"><span data-stu-id="84637-102">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="84637-103">Die Schlüsselwörter "muss", "darf nicht", "erforderlich", "soll", "soll nicht", "sollte", "sollte nicht", "empfohlen", "Mai" und "optional" in diesem Dokument interpretiert werden, wie in [RFC 2119](https://tools.ietf.org/html/rfc2119)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84637-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="84637-104">Jede Rand Leiste mit den Überschriften "Note", "Information" oder "Warning" ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="84637-105">Einführung</span><span class="sxs-lookup"><span data-stu-id="84637-105">Introduction</span></span> ##

<span data-ttu-id="84637-106">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-106">This section is informative.</span></span>

<span data-ttu-id="84637-107">Broombridge-Dokumente sollen Instanzen von Simulations Problemen in der Quantum-Chemie für die Verarbeitung mithilfe der Quantum-Simulation und der Programmier Toolkette kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="84637-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="84637-108">Serialisierung</span><span class="sxs-lookup"><span data-stu-id="84637-108">Serialization</span></span> ##

<span data-ttu-id="84637-109">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-109">This section is normative.</span></span>

<span data-ttu-id="84637-110">Ein broombridge-Dokument muss als [YAML 1,2-Dokument](http://yaml.org/spec/) serialisiert werden, das ein JSON-Objekt darstellt, wie in [RFC 4627](https://tools.ietf.org/html/rfc4627) Abschnitt 2,2 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84637-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="84637-111">Das an YAML serialisierte Objekt muss über eine Eigenschaft `"$schema"` verfügen, deren Wert `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`ist und gemäß den Spezifikationen des JSON-Schema Entwurfs-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)] gültig sein muss.</span><span class="sxs-lookup"><span data-stu-id="84637-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="84637-112">Im restlichen Teil dieser Spezifikation verweist "das broombridge-Objekt" auf das JSON-Objekt, das aus einem broombridge-YAML-Dokument deserialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="84637-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="84637-113">Sofern nicht anders angegeben, dürfen Objekte keine zusätzlichen Eigenschaften aufweisen, die über die explizit in diesem Dokument angegebenen verfügen.</span><span class="sxs-lookup"><span data-stu-id="84637-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="84637-114">Weitere Definitionen</span><span class="sxs-lookup"><span data-stu-id="84637-114">Additional Definitions</span></span> ##

<span data-ttu-id="84637-115">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="84637-116">Mengen Objekte</span><span class="sxs-lookup"><span data-stu-id="84637-116">Quantity Objects</span></span> ###

<span data-ttu-id="84637-117">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-117">This section is normative.</span></span>

<span data-ttu-id="84637-118">Bei einem _Mengen Objekt_ handelt es sich um ein JSON-Objekt, und es muss über eine Eigenschaft `units` verfügen, deren Wert einem der in Tabelle 1 aufgeführten zulässigen Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="84637-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="84637-119">Bei einem Mengen Objekt handelt es sich um ein _einfaches Mengen Objekt_ , wenn zusätzlich zu seiner `units`-Eigenschaft eine einzelne Eigenschaft `value`.</span><span class="sxs-lookup"><span data-stu-id="84637-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="84637-120">Der Wert der `value`-Eigenschaft muss eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="84637-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="84637-121">Ein Mengen Objekt ist ein gebundenes _Mengen_ Objekt, wenn es über die Eigenschaften `lower` und `upper` zusätzlich zu seiner `units` Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="84637-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="84637-122">Die Werte der Eigenschaften `lower` und `upper` müssen zahlen sein.</span><span class="sxs-lookup"><span data-stu-id="84637-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="84637-123">Ein Objekt mit begrenzter Menge kann eine Eigenschaft `value` haben, deren Wert eine Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="84637-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="84637-124">Bei einem Mengen Objekt handelt es sich um ein _Array Objekt_ mit geringer Dichte, wenn es die-Eigenschaft `format` und eine-Eigenschaft `values` zusätzlich zu seiner `units`-Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="84637-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="84637-125">Der Wert von `format` muss die Zeichenfolge `sparse`sein.</span><span class="sxs-lookup"><span data-stu-id="84637-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="84637-126">Der Wert der `values`-Eigenschaft muss ein Array sein.</span><span class="sxs-lookup"><span data-stu-id="84637-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="84637-127">Jedes Element von `values` muss ein Array sein, das die Indizes und den Wert der Menge an Arrays mit geringer Dichte darstellt.</span><span class="sxs-lookup"><span data-stu-id="84637-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="84637-128">Die Indizes für jedes Element eines Arrays mit geringer Dichte Menge müssen innerhalb des gesamten Objekts mit geringer Dichte Menge eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="84637-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="84637-129">Wenn ein Index mit dem Wert `0`vorhanden ist, muss ein Parser das Mengen Objekt mit geringer Dichte mit einem Array mit geringer Menge an Mengen Objekten behandeln, in dem dieser Index überhaupt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="84637-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="84637-130">Ein Mengen Objekt muss entweder</span><span class="sxs-lookup"><span data-stu-id="84637-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="84637-131">ein einfaches Mengen Objekt,</span><span class="sxs-lookup"><span data-stu-id="84637-131">a simple quantity object,</span></span>
- <span data-ttu-id="84637-132">ein Objekt mit begrenzter Menge oder</span><span class="sxs-lookup"><span data-stu-id="84637-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="84637-133">ein Mengen Objekt mit geringer Dichte.</span><span class="sxs-lookup"><span data-stu-id="84637-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="84637-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84637-134">Examples</span></span> ###

<span data-ttu-id="84637-135">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-135">This section is informative.</span></span>

<span data-ttu-id="84637-136">Eine einfache Menge, die $1.9844146837\,\mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="84637-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="84637-137">Eine begrenzte Menge, die eine einheitliche Verteilung im Intervall von $ [-7,-6]\,\mathrm{ha} $ darstellt:</span><span class="sxs-lookup"><span data-stu-id="84637-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="84637-138">Im folgenden finden Sie eine Array Menge mit geringer Dichte, bei der ein-Element `[1, 2]` gleich `hello` und ein-Element `[3, 4]` gleich `world`sind:</span><span class="sxs-lookup"><span data-stu-id="84637-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="84637-139">Abschnitt "Format"</span><span class="sxs-lookup"><span data-stu-id="84637-139">Format Section</span></span> ##

<span data-ttu-id="84637-140">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-140">This section is normative.</span></span>

<span data-ttu-id="84637-141">Das broombridge-Objekt muss über eine Eigenschaft `format` verfügen, deren Wert ein JSON-Objekt mit einer Eigenschaft namens `version`ist.</span><span class="sxs-lookup"><span data-stu-id="84637-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="84637-142">Die `version`-Eigenschaft muss den Wert `"0.2"`haben.</span><span class="sxs-lookup"><span data-stu-id="84637-142">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="84637-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="84637-143">Example</span></span> ###

<span data-ttu-id="84637-144">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="84637-145">Problem Beschreibungs Abschnitt</span><span class="sxs-lookup"><span data-stu-id="84637-145">Problem Description Section</span></span> ##

<span data-ttu-id="84637-146">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-146">This section is normative.</span></span>

<span data-ttu-id="84637-147">Das broombridge-Objekt muss über eine Eigenschaft `problem_description` verfügen, deren Wert ein JSON-Array ist.</span><span class="sxs-lookup"><span data-stu-id="84637-147">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="84637-148">Jedes Element im Wert der `problem_description`-Eigenschaft muss ein JSON-Objekt sein, das einen Satz von inteden beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84637-148">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="84637-149">Im restlichen Teil dieses Abschnitts verweist der Begriff "problembeschreibungs-Objekt" auf ein Element im Wert der `problem_description`-Eigenschaft des broombridge-Objekts.</span><span class="sxs-lookup"><span data-stu-id="84637-149">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="84637-150">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `metadata` verfügen, deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="84637-150">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="84637-151">Der Wert von `metadata` kann das leere JSON-Objekt (`{}`) sein oder zusätzliche Eigenschaften enthalten, die durch den implemenor definiert werden.</span><span class="sxs-lookup"><span data-stu-id="84637-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="84637-152">Hamiltona-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="84637-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="84637-153">Übersicht</span><span class="sxs-lookup"><span data-stu-id="84637-153">Overview</span></span> ####

<span data-ttu-id="84637-154">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-154">This section is informative.</span></span>

<span data-ttu-id="84637-155">Die `hamiltonian`-Eigenschaft jedes problembeschreibungs Objekts beschreibt den hamiltonan für ein bestimmtes Quantum-Chemie Problem, indem er seine ein-und zwei Text Begriffe als sparsesreellen von reellen Zahlen auflistet.</span><span class="sxs-lookup"><span data-stu-id="84637-155">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="84637-156">Die von den einzelnen problembeschreibungs-Objekten beschriebenen hamiltonan-Operatoren haben das Formular.</span><span class="sxs-lookup"><span data-stu-id="84637-156">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="84637-157">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparamerow, \downpfeil\\}} h\_\{IJ\} a ^\{\dagger\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparser, \downpfeil\\}} h\_{IJKL} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l, \rho} a\_{j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="84637-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="84637-158">Hier $h _ {IJKL} = (IJ | KL) $ in der Mulliken-Konvention.</span><span class="sxs-lookup"><span data-stu-id="84637-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="84637-159">Aus Gründen der Übersichtlichkeit lautet der Begriff mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="84637-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="84637-160">$ $ H_ {IJ} = \int {\mathrm d} x \psi ^ \*\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \bruchteil {z\_a} {| x-x\_a |}  \right) \psi\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="84637-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="84637-161">und der zwei-Elektronen-Begriff ist</span><span class="sxs-lookup"><span data-stu-id="84637-161">and the two-electron term is</span></span>

<span data-ttu-id="84637-162">$ $ h\_\{IJKL\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="84637-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="84637-163">Wie in der Beschreibung der`basis_set`- [Eigenschaft](#basis-set-object) der einzelnen Elemente der `integral_sets`-Eigenschaft erwähnt, wird explizit angenommen, dass die verwendeten Basisfunktionen einen echten Wert haben.</span><span class="sxs-lookup"><span data-stu-id="84637-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="84637-164">Dies ermöglicht es uns, die folgenden Symmetries zwischen den Begriffen zu verwenden, um die Darstellung der hamiltonan zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="84637-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="84637-165">$ $ H_ {IJKL} = H_ {IJLK} = H_ {jikl} = H_ {jilk} = H_ {klij} = H_ {klji} = H_ {lkij} = H_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="84637-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="84637-166">Inhalt</span><span class="sxs-lookup"><span data-stu-id="84637-166">Contents</span></span> ####

<span data-ttu-id="84637-167">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-167">This section is normative.</span></span>

<span data-ttu-id="84637-168">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `hamiltonian` verfügen, deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="84637-168">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="84637-169">Der Wert der `hamiltonian`-Eigenschaft wird als "hamiltonan" bezeichnet und muss die Eigenschaften `one_electron_integrals` und `two_electron_integrals` aufweisen, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84637-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="84637-170">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `coulomb_repulsion` verfügen, deren Wert ein einfaches Mengen Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="84637-170">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="84637-171">Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `energy_offet` verfügen, deren Wert ein einfaches Mengen Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="84637-171">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="84637-172">Nebenbei Die Werte von `coulomb_repulsion` und `energy_offet` addiert die Identitäts Laufzeit der hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="84637-172">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="84637-173">Integrale Objekt mit einem-Elektronen</span><span class="sxs-lookup"><span data-stu-id="84637-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="84637-174">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-174">This section is normative.</span></span>

<span data-ttu-id="84637-175">Die `one_electron_integrals`-Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte sein, deren Indizes zwei Ganzzahlen und deren Werte Ziffern sind.</span><span class="sxs-lookup"><span data-stu-id="84637-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="84637-176">Jeder Begriff muss über Indizes `[i, j]`, wo `i >= j`.</span><span class="sxs-lookup"><span data-stu-id="84637-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="84637-177">Nebenbei Dies spiegelt die Symmetrie wider, die $h _ {IJ} = H_ {JI} $ liegt. Dies ist eine Folge der Tatsache, dass der hamiltonan hermitian ist.</span><span class="sxs-lookup"><span data-stu-id="84637-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="84637-178">Beispiel</span><span class="sxs-lookup"><span data-stu-id="84637-178">Example</span></span> ######

<span data-ttu-id="84637-179">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-179">This section is informative.</span></span>

<span data-ttu-id="84637-180">Die folgende Menge an Arrays mit geringer Dichte repräsentiert das hamiltonan $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1 , \downarrow}) + 0,17 (a ^\{\dagger\}\_{2, \uparamerow} a\_{1, \uanrow} + a ^\{\dagger\}\_{1, \uparamerow} a\_{2, \uparamerow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="84637-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="84637-181">Broombridge verwendet die 1-basierte Indizierung.</span><span class="sxs-lookup"><span data-stu-id="84637-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="84637-182">2-Elektronen-inteals-Objekt</span><span class="sxs-lookup"><span data-stu-id="84637-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="84637-183">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-183">This section is normative.</span></span>

<span data-ttu-id="84637-184">Die `two_electron_integrals`-Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte mit einer zusätzlichen Eigenschaft namens `index_convention`sein.</span><span class="sxs-lookup"><span data-stu-id="84637-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="84637-185">Jedes Element des Werts `two_electron_integrals` muss vier Indizes aufweisen.</span><span class="sxs-lookup"><span data-stu-id="84637-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="84637-186">Jede `two_electron_integrals` Eigenschaft muss über eine `index_convention`-Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="84637-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="84637-187">Der Wert der `index_convention`-Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 1 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="84637-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="84637-188">Wenn der Wert von `index_convention` `mulliken`ist, muss ein Parser, der ein broombridge-Dokument lädt, für jedes Element der Menge der `two_electron_integrals` Sparse-Arrays einen Hamilton-Begriff instanziieren, der mit dem zwei-Elektronen-Operator identisch ist $h _ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k a_l $ , wobei $i $, $j $, $k $ und $l $ ganze Zahlen mit einem Wert von mindestens 1 sein müssen und wobei $h _ {i, j, k, l} $ das Element `[i, j, k, l, h(i, j, k, l)]` der Menge an geringer Dichte ist.</span><span class="sxs-lookup"><span data-stu-id="84637-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="84637-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="84637-189">Symmetries</span></span> ######

<span data-ttu-id="84637-190">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-190">This section is normative.</span></span>

<span data-ttu-id="84637-191">Wenn die `index_convention`-Eigenschaft eines `two_electron_integrals` Objekts gleich `mulliken`ist und ein Element mit Indizes `[i, j, k, l]` vorhanden ist, dürfen die folgenden Indizes nur vorhanden sein, wenn Sie `[i, j, k, l]`sind:</span><span class="sxs-lookup"><span data-stu-id="84637-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="84637-192">Da die `index_convention`-Eigenschaft ein Objekt mit geringer Menge ist, können für unterschiedliche Elemente keine Indizes wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="84637-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="84637-193">Insbesondere, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, kann kein anderes Element über diese Indizes verfügen.</span><span class="sxs-lookup"><span data-stu-id="84637-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="84637-194">Beispiel</span><span class="sxs-lookup"><span data-stu-id="84637-194">Example</span></span> #######

<span data-ttu-id="84637-195">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-195">This section is informative.</span></span>

<span data-ttu-id="84637-196">Das folgende Objekt gibt den hamiltonan an.</span><span class="sxs-lookup"><span data-stu-id="84637-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="84637-197">$ $ H = \bruch12 \sum\_{\sigma, \rho\in\\{\ubirow, \downpfeil\\}} \biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{2 , \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1, \rho} a\_{6, \sigma}\Biggr)\\, \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="84637-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

### <a name="initial-state-section"></a><span data-ttu-id="84637-198">Abschnitt "Anfangszustand"</span><span class="sxs-lookup"><span data-stu-id="84637-198">Initial State Section</span></span> ###

<span data-ttu-id="84637-199">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-199">This section is normative.</span></span>

<span data-ttu-id="84637-200">Das `initial_state_suggestion` Objekt, dessen Wert ein JSON-Array ist, gibt die anfänglichen Quantum-Zustände an, die für die angegebene hamiltonan von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="84637-200">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="84637-201">Jedes Element im Wert der `initial_state_suggestion`-Eigenschaft muss ein JSON-Objekt sein, das einen Quantenzustand beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84637-201">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="84637-202">Im restlichen Teil dieses Abschnitts verweist der Begriff "State Object" auf ein Element im Wert der `initial_state_suggestion`-Eigenschaft des broombridge-Objekts.</span><span class="sxs-lookup"><span data-stu-id="84637-202">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="84637-203">State-Objekt</span><span class="sxs-lookup"><span data-stu-id="84637-203">State object</span></span> ####

<span data-ttu-id="84637-204">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-204">This section is normative.</span></span>

<span data-ttu-id="84637-205">Jedes Zustands Objekt muss über eine `label`-Eigenschaft verfügen, die eine Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="84637-205">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="84637-206">Jedes Zustands Objekt muss über eine `method`-Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="84637-206">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="84637-207">Der Wert der `method`-Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 3 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="84637-207">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="84637-208">Jedes Zustands Objekt verfügt möglicherweise über eine Eigenschaft `energy`, deren Wert ein einfaches Mengen Objekt sein muss.</span><span class="sxs-lookup"><span data-stu-id="84637-208">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="84637-209">Wenn der Wert der `method`-Eigenschaft `sparse_multi_configurational`ist, muss das State-Objekt über eine `superposition`-Eigenschaft verfügen, die ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.</span><span class="sxs-lookup"><span data-stu-id="84637-209">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="84637-210">Der anfängliche Status lautet z. b. $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{e} = \bruchteil {0,1 (a ^ {\dagger}\_{1 , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket{0}, $ $, wobei "$ \ket{e} $" den Wert "Energy $0,987 \textrm{ha} $" hat, wird durch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="84637-210">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
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

<span data-ttu-id="84637-211">Wenn der Wert der `method`-Eigenschaft `unitary_coupled_cluster`ist, muss das State-Objekt über eine `cluster_operator`-Eigenschaft verfügen, deren Wert ein JSON-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="84637-211">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="84637-212">Das JSON-Objekt muss über eine `reference_state`-Eigenschaft verfügen, deren Wert ein Basiszustand ist.</span><span class="sxs-lookup"><span data-stu-id="84637-212">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="84637-213">Das JSON-Objekt verfügt möglicherweise über eine `one_body_amplitudes`-Eigenschaft, deren Wert ein Array von Einzel Text Cluster-Operatoren und deren Verstärkung ist.</span><span class="sxs-lookup"><span data-stu-id="84637-213">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="84637-214">Das JSON-Objekt verfügt möglicherweise über eine `two_body_amplitudes`-Eigenschaft, deren Wert ein Array aus zwei Text-Cluster Operatoren und deren Verstärkung ist.</span><span class="sxs-lookup"><span data-stu-id="84637-214">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="84637-215">, das ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.</span><span class="sxs-lookup"><span data-stu-id="84637-215">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="84637-216">Beispielsweise der Status $ $ \ket{\text{Reference}} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0}, $ $</span><span class="sxs-lookup"><span data-stu-id="84637-216">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="84637-217">$ $ \ket{\text{UCCSD}} = e ^ {T-t ^ \dagger}\ket{\text{Reference}}, $ $</span><span class="sxs-lookup"><span data-stu-id="84637-217">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="84637-218">$ $ T = 0,1 a ^ {\dagger}\_{3, \uparrow}a\_{2, \downarrow} + 0,2 a ^ {\dagger}\_{2, \uparrow}a\_{2, \downarrow}-0,3 a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \downarrow}a\_{3 , \uparrow}a\_{2, \downarrow} $ $ wird dargestellt durch</span><span class="sxs-lookup"><span data-stu-id="84637-218">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
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

#### <a name="basis-set-object"></a><span data-ttu-id="84637-219">Basis Objekt festlegen</span><span class="sxs-lookup"><span data-stu-id="84637-219">Basis Set Object</span></span> ####

<span data-ttu-id="84637-220">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-220">This section is normative.</span></span>

<span data-ttu-id="84637-221">Jedes Problem Beschreibungs Objekt kann über eine `basis_set`-Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="84637-221">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="84637-222">Wenn der Wert der `basis_set`-Eigenschaft vorhanden ist, muss es sich um ein Objekt mit zwei Eigenschaften handeln, `type` und `name`.</span><span class="sxs-lookup"><span data-stu-id="84637-222">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="84637-223">Die Basisfunktionen, die durch den Wert der `basis_set`-Eigenschaft identifiziert werden, müssen ein echter Wert sein.</span><span class="sxs-lookup"><span data-stu-id="84637-223">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="84637-224">Die Annahme, dass alle Basisfunktionen in Wirklichkeit sind, kann in zukünftigen Versionen dieser Spezifikation gelockert werden.</span><span class="sxs-lookup"><span data-stu-id="84637-224">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="84637-225">Tabellen und Listen</span><span class="sxs-lookup"><span data-stu-id="84637-225">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="84637-226">Tabelle 1.</span><span class="sxs-lookup"><span data-stu-id="84637-226">Table 1.</span></span> <span data-ttu-id="84637-227">Zulässige physische Einheiten</span><span class="sxs-lookup"><span data-stu-id="84637-227">Allowed Physical Units</span></span> ###

<span data-ttu-id="84637-228">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-228">This section is normative.</span></span>

<span data-ttu-id="84637-229">Jede Zeichenfolge, die eine Einheit angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="84637-229">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="84637-230">Parser und Producer müssen die folgenden einfachen Mengen Objekte als gleichwertig behandeln:</span><span class="sxs-lookup"><span data-stu-id="84637-230">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="84637-231">Tabelle 2:</span><span class="sxs-lookup"><span data-stu-id="84637-231">Table 2.</span></span> <span data-ttu-id="84637-232">Zulässige Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="84637-232">Allowed Index Conventions</span></span> ###

<span data-ttu-id="84637-233">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-233">This section is normative.</span></span>

<span data-ttu-id="84637-234">Jede Zeichenfolge, die eine Index Konvention angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="84637-234">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="84637-235">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-235">This section is informative.</span></span>

<span data-ttu-id="84637-236">In zukünftigen Versionen dieser Spezifikation können zusätzliche Index Konventionen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="84637-236">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="84637-237">Interpretation von Index Konventionen</span><span class="sxs-lookup"><span data-stu-id="84637-237">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="84637-238">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-238">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="84637-239">Tabelle 3.</span><span class="sxs-lookup"><span data-stu-id="84637-239">Table 3.</span></span> <span data-ttu-id="84637-240">Zulässige Zustands Methoden</span><span class="sxs-lookup"><span data-stu-id="84637-240">Allowed State methods</span></span> ###

<span data-ttu-id="84637-241">Dieser Abschnitt ist normativ.</span><span class="sxs-lookup"><span data-stu-id="84637-241">This section is normative.</span></span>

<span data-ttu-id="84637-242">Jede Zeichenfolge, die eine Zustands Methode angibt, muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="84637-242">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="84637-243">Dieser Abschnitt ist informativ.</span><span class="sxs-lookup"><span data-stu-id="84637-243">This section is informative.</span></span>

<span data-ttu-id="84637-244">Weitere Zustands Methoden können in zukünftigen Versionen dieser Spezifikation eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="84637-244">Additional state methods may be introduced in future versions of this specification.</span></span>
