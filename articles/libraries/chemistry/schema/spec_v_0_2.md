---
title: Broombridge-Schema Spezifikation (ver 0,2)
description: Erläutert die Spezifikationen für das broombridge-Quantum-Schema v 0,2 für die Microsoft Quantum Chemistry Library.
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
ms.openlocfilehash: df7e651b7d32e672c6e83346ff603132bd55c1a2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907272"
---
# <a name="broombridge-specification-v02"></a>Broombridge-Spezifikation v 0,2 #

Die Schlüsselwörter "muss", "darf nicht", "erforderlich", "soll", "soll nicht", "sollte", "sollte nicht", "empfohlen", "Mai" und "optional" in diesem Dokument interpretiert werden, wie in [RFC 2119](https://tools.ietf.org/html/rfc2119)beschrieben.

Jede Rand Leiste mit den Überschriften "Note", "Information" oder "Warning" ist informativ.

## <a name="introduction"></a>Einführung ##

Dieser Abschnitt ist informativ.

Broombridge-Dokumente sollen Instanzen von Simulations Problemen in der Quantum-Chemie für die Verarbeitung mithilfe der Quantum-Simulation und der Programmier Toolkette kommunizieren.

## <a name="serialization"></a>Serialisierung ##

Dieser Abschnitt ist normativ.

Ein broombridge-Dokument muss als [YAML 1,2-Dokument](http://yaml.org/spec/) serialisiert werden, das ein JSON-Objekt darstellt, wie in [RFC 4627](https://tools.ietf.org/html/rfc4627) Abschnitt 2,2 beschrieben.
Das an YAML serialisierte Objekt muss über eine Eigenschaft `"$schema"` verfügen, deren Wert `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`ist und gemäß den Spezifikationen des JSON-Schema Entwurfs-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)] gültig sein muss.

Im restlichen Teil dieser Spezifikation verweist "das broombridge-Objekt" auf das JSON-Objekt, das aus einem broombridge-YAML-Dokument deserialisiert wurde.

Sofern nicht anders angegeben, dürfen Objekte keine zusätzlichen Eigenschaften aufweisen, die über die explizit in diesem Dokument angegebenen verfügen.

## <a name="additional-definitions"></a>Zusätzliche Definitionen ##

Dieser Abschnitt ist normativ.

### <a name="quantity-objects"></a>Mengen Objekte ###

Dieser Abschnitt ist normativ.

Bei einem _Mengen Objekt_ handelt es sich um ein JSON-Objekt, und es muss über eine Eigenschaft `units` verfügen, deren Wert einem der in Tabelle 1 aufgeführten zulässigen Werte entspricht.

Bei einem Mengen Objekt handelt es sich um ein _einfaches Mengen Objekt_ , wenn zusätzlich zu seiner `units`-Eigenschaft eine einzelne Eigenschaft `value`.
Der Wert der `value`-Eigenschaft muss eine Zahl sein.

Ein Mengen Objekt ist ein gebundenes _Mengen_ Objekt, wenn es über die Eigenschaften `lower` und `upper` zusätzlich zu seiner `units` Eigenschaft verfügt.
Die Werte der Eigenschaften `lower` und `upper` müssen zahlen sein.
Ein Objekt mit begrenzter Menge kann eine Eigenschaft `value` haben, deren Wert eine Zahl ist.

Bei einem Mengen Objekt handelt es sich um ein _Array Objekt_ mit geringer Dichte, wenn es die-Eigenschaft `format` und eine-Eigenschaft `values` zusätzlich zu seiner `units`-Eigenschaft aufweist.
Der Wert von `format` muss die Zeichenfolge `sparse`sein.
Der Wert der `values`-Eigenschaft muss ein Array sein.
Jedes Element von `values` muss ein Array sein, das die Indizes und den Wert der Menge an Arrays mit geringer Dichte darstellt.

Die Indizes für jedes Element eines Arrays mit geringer Dichte Menge müssen innerhalb des gesamten Objekts mit geringer Dichte Menge eindeutig sein.
Wenn ein Index mit dem Wert `0`vorhanden ist, muss ein Parser das Mengen Objekt mit geringer Dichte mit einem Array mit geringer Menge an Mengen Objekten behandeln, in dem dieser Index überhaupt nicht vorhanden ist.


Ein Mengen Objekt muss entweder

- ein einfaches Mengen Objekt,
- ein Objekt mit begrenzter Menge oder
- ein Mengen Objekt mit geringer Dichte.


### <a name="examples"></a>Beispiele ###

Dieser Abschnitt ist informativ.

Eine einfache Menge, die $1.9844146837\,\mathrm{ha} $ darstellt:

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

Eine begrenzte Menge, die eine einheitliche Verteilung im Intervall von $ [-7,-6]\,\mathrm{ha} $ darstellt:

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

Im folgenden finden Sie eine Array Menge mit geringer Dichte, bei der ein-Element `[1, 2]` gleich `hello` und ein-Element `[3, 4]` gleich `world`sind:

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a>Abschnitt "Format" ##

Dieser Abschnitt ist normativ.

Das broombridge-Objekt muss über eine Eigenschaft `format` verfügen, deren Wert ein JSON-Objekt mit einer Eigenschaft namens `version`ist.
Die `version`-Eigenschaft muss den Wert `"0.2"`haben.

### <a name="example"></a>Beispiel ###

Dieser Abschnitt ist informativ.

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a>Problem Beschreibungs Abschnitt ##

Dieser Abschnitt ist normativ.

Das broombridge-Objekt muss über eine Eigenschaft `problem_description` verfügen, deren Wert ein JSON-Array ist.
Jedes Element im Wert der `problem_description`-Eigenschaft muss ein JSON-Objekt sein, das einen Satz von inteden beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.
Im restlichen Teil dieses Abschnitts verweist der Begriff "problembeschreibungs-Objekt" auf ein Element im Wert der `problem_description`-Eigenschaft des broombridge-Objekts.

Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `metadata` verfügen, deren Wert ein JSON-Objekt ist.
Der Wert von `metadata` kann das leere JSON-Objekt (`{}`) sein oder zusätzliche Eigenschaften enthalten, die durch den implemenor definiert werden.

### <a name="hamiltonian-section"></a>Hamiltona-Abschnitt ###

#### <a name="overview"></a>Übersicht ####

Dieser Abschnitt ist informativ.

Die `hamiltonian`-Eigenschaft jedes problembeschreibungs Objekts beschreibt den hamiltonan für ein bestimmtes Quantum-Chemie Problem, indem er seine ein-und zwei Text Begriffe als sparsesreellen von reellen Zahlen auflistet.
Die von den einzelnen problembeschreibungs-Objekten beschriebenen hamiltonan-Operatoren haben das Formular.

$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparamerow, \downpfeil\\}} h\_\{IJ\} a ^\{\dagger\}\_{i, \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparser, \downpfeil\\}} H\_{IJKL} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l, \rho} a\_{j, \sigma}, $ $

Hier $h _ {IJKL} = (IJ | KL) $ in der Mulliken-Konvention.

Aus Gründen der Übersichtlichkeit lautet der Begriff mit einem-Elektronen

$ $ H_ {IJ} = \int {\mathrm d} x \psi ^ *\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \bruchteil {z\_a} {| x-x\_a |}  \right) \psi\_j (x), $ $

und der zwei-Elektronen-Begriff ist

$ $ h\_\{IJKL\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).
$$

Wie in der Beschreibung der`basis_set`- [Eigenschaft](#basis-set-object) der einzelnen Elemente der `integral_sets`-Eigenschaft erwähnt, wird explizit angenommen, dass die verwendeten Basisfunktionen einen echten Wert haben.
Dies ermöglicht es uns, die folgenden Symmetries zwischen den Begriffen zu verwenden, um die Darstellung der hamiltonan zu komprimieren.

$ $ H_ {IJKL} = H_ {IJLK} = H_ {jikl} = H_ {jilk} = H_ {klij} = H_ {klji} = H_ {lkij} = H_ {lkji}.
$$


#### <a name="contents"></a>Contents ####

Dieser Abschnitt ist normativ.

Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `hamiltonian` verfügen, deren Wert ein JSON-Objekt ist.
Der Wert der `hamiltonian`-Eigenschaft wird als "hamiltonan" bezeichnet und muss die Eigenschaften `one_electron_integrals` und `two_electron_integrals` aufweisen, wie im restlichen Teil dieses Abschnitts beschrieben.

Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `coulomb_repulsion` verfügen, deren Wert ein einfaches Mengen Objekt ist.
Jedes Problem Beschreibungs Objekt muss über eine Eigenschaft `energy_offet` verfügen, deren Wert ein einfaches Mengen Objekt ist.
> Nebenbei Die Werte von `coulomb_repulsion` und `energy_offet` addiert die Identitäts Laufzeit der hamiltonan.

##### <a name="one-electron-integrals-object"></a>Integrale Objekt mit einem-Elektronen #####

Dieser Abschnitt ist normativ.

Die `one_electron_integrals`-Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte sein, deren Indizes zwei Ganzzahlen und deren Werte Ziffern sind.
Jeder Begriff muss über Indizes `[i, j]`, wo `i >= j`.

> Nebenbei Dies spiegelt die Symmetrie wider, die $h _ {IJ} = H_ {JI} $ liegt. Dies ist eine Folge der Tatsache, dass der hamiltonan hermitian ist.


###### <a name="example"></a>Beispiel ######

Dieser Abschnitt ist informativ.

Die folgende Menge an Arrays mit geringer Dichte repräsentiert den Wert hamiltonan $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1, \downarrow}) + 0,17 (a ^\{\dagger\}\_{2, \uparamerow} a\_{1, \uparamerow} + a ^\{\dagger\}\_{1, \uparamerow} a\_{2, \uparamerow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{ha}.
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
> Broombridge verwendet die 1-basierte Indizierung.


##### <a name="two-electron-integrals-object"></a>2-Elektronen-inteals-Objekt #####

Dieser Abschnitt ist normativ.

Die `two_electron_integrals`-Eigenschaft des hamiltonan-Objekts muss eine Array Menge mit geringer Dichte mit einer zusätzlichen Eigenschaft namens `index_convention`sein.
Jedes Element des Werts `two_electron_integrals` muss vier Indizes aufweisen.

Jede `two_electron_integrals` Eigenschaft muss über eine `index_convention`-Eigenschaft verfügen.
Der Wert der `index_convention`-Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 1 aufgeführt sind.
Wenn der Wert von `index_convention` `mulliken`ist, muss ein Parser, der ein broombridge-Dokument lädt, für jedes Element der Menge von `two_electron_integrals` Arrays mit geringer Dichte einen hamiltonbegriff instanziieren, der mit dem zwei-Elektronen-Operator $h _ {i übereinstimmt. j, k, l} a ^ \ dagger_i a ^ \ dagger_j a_k a_l $, wobei $i $, $j $, $k $ und $l $ ganzzahlige Werte von mindestens 1 sein müssen und wobei $h _ {i, j, k, l} $ das Element `[i, j, k, l, h(i, j, k, l)]` der Menge an geringer Dichte ist.

###### <a name="symmetries"></a>Symmetries ######

Dieser Abschnitt ist normativ.

Wenn die `index_convention`-Eigenschaft eines `two_electron_integrals` Objekts gleich `mulliken`ist und ein Element mit Indizes `[i, j, k, l]` vorhanden ist, dürfen die folgenden Indizes nur vorhanden sein, wenn Sie `[i, j, k, l]`sind:

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> Da die `index_convention`-Eigenschaft ein Objekt mit geringer Menge ist, können für unterschiedliche Elemente keine Indizes wiederholt werden.
> Insbesondere, wenn ein Element mit Indizes `[i, j, k, l]` vorhanden ist, kann kein anderes Element über diese Indizes verfügen.


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a>Beispiel #######

Dieser Abschnitt ist informativ.

Das folgende Objekt gibt den hamiltonan an.

$ $ H = \bruch12 \sum\_{\sigma, \rho\in\\{\ubirow, \downpfeil\\}} \biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2 , \rho} a\_{3, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{2, \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3 , \sigma} a ^ {\dagger}\_{2, \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{1, \rho} a\_{6, \sigma}\Biggr)\\, \textrm{ha}.
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

### <a name="initial-state-section"></a>Abschnitt "Anfangszustand" ###

Dieser Abschnitt ist normativ.

Das `initial_state_suggestion` Objekt, dessen Wert ein JSON-Array ist, gibt die anfänglichen Quantum-Zustände an, die für die angegebene hamiltonan von Interesse sind. Jedes Element im Wert der `initial_state_suggestion`-Eigenschaft muss ein JSON-Objekt sein, das einen Quantenzustand beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.
Im restlichen Teil dieses Abschnitts verweist der Begriff "State Object" auf ein Element im Wert der `initial_state_suggestion`-Eigenschaft des broombridge-Objekts.

#### <a name="state-object"></a>State-Objekt ####

Dieser Abschnitt ist normativ.

Jedes Zustands Objekt muss über eine `label`-Eigenschaft verfügen, die eine Zeichenfolge enthält. Jedes Zustands Objekt muss über eine `method`-Eigenschaft verfügen. Der Wert der `method`-Eigenschaft muss einer der zulässigen Werte sein, die in Tabelle 3 aufgeführt sind.
Jedes Zustands Objekt verfügt möglicherweise über eine Eigenschaft `energy`, deren Wert ein einfaches Mengen Objekt sein muss.

Wenn der Wert der `method`-Eigenschaft `sparse_multi_configurational`ist, muss das State-Objekt über eine `superposition`-Eigenschaft verfügen, die ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.

Der anfängliche Status lautet z. b. $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{e} = \bruchteil {0,1 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0.2 | ^ 2}} \ket{0}, $ $, wobei "$ \ket{e} $" den Wert "Energy $0,987 \textrm{ha} $" hat, wird durch dargestellt.
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

Wenn der Wert der `method`-Eigenschaft `unitary_coupled_cluster`ist, muss das State-Objekt über eine `cluster_operator`-Eigenschaft verfügen, deren Wert ein JSON-Objekt ist.
Das JSON-Objekt muss über eine `reference_state`-Eigenschaft verfügen, deren Wert ein Basiszustand ist.
Das JSON-Objekt verfügt möglicherweise über eine `one_body_amplitudes`-Eigenschaft, deren Wert ein Array von Einzel Text Cluster-Operatoren und deren Verstärkung ist.
Das JSON-Objekt verfügt möglicherweise über eine `two_body_amplitudes`-Eigenschaft, deren Wert ein Array aus zwei Text-Cluster Operatoren und deren Verstärkung ist.
, das ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.

Beispielsweise der Status $ $ \ket{\text{Reference}} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0}, $ $

$ $ \ket{\text{UCCSD}} = e ^ {T-t ^ \dagger}\ket{\text{Reference}}, $ $

$ $ T = 0,1 a ^ {\dagger}\_{3, \uparrow}a\_{2, \downarrow} + 0,2 a ^ {\dagger}\_{2, \uparrow}a\_{2, \downarrow}-0,3 a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \downarrow}a\_{3, \uparrow}a\_{2, \downarrow} $ $ wird dargestellt durch
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

#### <a name="basis-set-object"></a>Basis Objekt festlegen ####

Dieser Abschnitt ist normativ.

Jedes Problem Beschreibungs Objekt kann über eine `basis_set`-Eigenschaft verfügen.
Wenn der Wert der `basis_set`-Eigenschaft vorhanden ist, muss es sich um ein Objekt mit zwei Eigenschaften handeln, `type` und `name`.

Die Basisfunktionen, die durch den Wert der `basis_set`-Eigenschaft identifiziert werden, müssen ein echter Wert sein.

> [!NOTE]
> Die Annahme, dass alle Basisfunktionen in Wirklichkeit sind, kann in zukünftigen Versionen dieser Spezifikation gelockert werden.

## <a name="tables-and-lists"></a>Tabellen und Listen ##

### <a name="table-1-allowed-physical-units"></a>Tabelle 1. Zulässige physische Einheiten ###

Dieser Abschnitt ist normativ.

Jede Zeichenfolge, die eine Einheit angibt, muss eine der folgenden sein:

- `hartree`
- `ev`

Parser und Producer müssen die folgenden einfachen Mengen Objekte als gleichwertig behandeln:

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a>Tabelle 2: Zulässige Index Konventionen ###

Dieser Abschnitt ist normativ.

Jede Zeichenfolge, die eine Index Konvention angibt, muss eine der folgenden sein:

- `mulliken`

Dieser Abschnitt ist informativ.

In zukünftigen Versionen dieser Spezifikation können zusätzliche Index Konventionen eingeführt werden.

#### <a name="interpretation-of-index-conventions"></a>Interpretation von Index Konventionen ####

Dieser Abschnitt ist informativ.

### <a name="table-3-allowed-state-methods"></a>Tabelle 3. Zulässige Zustands Methoden ###

Dieser Abschnitt ist normativ.

Jede Zeichenfolge, die eine Zustands Methode angibt, muss eine der folgenden sein:

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

Dieser Abschnitt ist informativ.

Weitere Zustands Methoden können in zukünftigen Versionen dieser Spezifikation eingeführt werden.
