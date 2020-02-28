---
title: Broombridge-Schema Spezifikation (ver 0,1)
description: Erläutert die Spezifikationen für das broombridge-Quantum-Schema v 0,1 für die Microsoft Quantum Chemistry Library.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
ms.openlocfilehash: 618892b6cb01855d17522b06e47f72f68595ab38
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906422"
---
# <a name="broombridge-specification-v01"></a>Broombridge-Spezifikation v 0,1 #

Die Schlüsselwörter "muss", "darf nicht", "erforderlich", "soll", "soll nicht", "sollte", "sollte nicht", "empfohlen", "Mai" und "optional" in diesem Dokument interpretiert werden, wie in [RFC 2119](https://tools.ietf.org/html/rfc2119)beschrieben.

Jede Rand Leiste mit den Überschriften "Note", "Information" oder "Warning" ist informativ.

## <a name="introduction"></a>Einführung ##

Dieser Abschnitt ist informativ.

Broombridge-Dokumente sollen Instanzen von Simulations Problemen in der Quantum-Chemie für die Verarbeitung mithilfe der Quantum-Simulation und der Programmier Toolkette kommunizieren.

## <a name="serialization"></a>Serialisierung ##

Dieser Abschnitt ist normativ.

Ein broombridge-Dokument muss als [YAML 1,2-Dokument](http://yaml.org/spec/) serialisiert werden, das ein JSON-Objekt darstellt, wie in [RFC 4627](https://tools.ietf.org/html/rfc4627) Abschnitt 2,2 beschrieben.
Das an YAML serialisierte Objekt muss über eine Eigenschaft `"$schema"` verfügen, deren Wert `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`ist und gemäß den Spezifikationen des JSON-Schema Entwurfs-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)] gültig sein muss.

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
Die `version`-Eigenschaft muss den Wert `"0.1"`haben.

### <a name="example"></a>Beispiel ###

Dieser Abschnitt ist informativ.

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a>Abschnitt ganzzahlige Sätze ##

Dieser Abschnitt ist normativ.

Das broombridge-Objekt muss über eine Eigenschaft `integral_sets` verfügen, deren Wert ein JSON-Array ist.
Jedes Element im Wert der `integral_sets`-Eigenschaft muss ein JSON-Objekt sein, das einen Satz von inteden beschreibt, wie im restlichen Teil dieses Abschnitts beschrieben.
Im restlichen Teil dieses Abschnitts verweist der Begriff "Integral Set Object" auf ein Element im Wert der `integral_sets`-Eigenschaft des broombridge-Objekts.

Jedes ganzzahlige Set-Objekt muss über eine Eigenschaft `metadata` verfügen, deren Wert ein JSON-Objekt ist.
Der Wert von `metadata` kann das leere JSON-Objekt (`{}`) sein oder zusätzliche Eigenschaften enthalten, die durch den implemenor definiert werden.

### <a name="hamiltonian-section"></a>Hamiltona-Abschnitt ###

#### <a name="overview"></a>Übersicht ####

Dieser Abschnitt ist informativ.

Die `hamiltonian`-Eigenschaft jedes ganzzahligen Mengen Objekts beschreibt den hamiltonan für ein bestimmtes Quantum-Chemie Problem, indem er seine ein-und zwei Text Begriffe als sparsesreellen von reellen Zahlen auflistet.
Die von jedem integralen Satz Objekt beschriebenen hamiltonan-Operatoren haben das Formular

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

Jede ganzzahlige Menge muss eine Eigenschaft `hamiltonian` haben, deren Wert ein JSON-Objekt ist.
Der Wert der `hamiltonian`-Eigenschaft wird als "hamiltonan" bezeichnet und muss die Eigenschaften `one_electron_integrals` und `two_electron_integrals` aufweisen, wie im restlichen Teil dieses Abschnitts beschrieben.
Ein hamiltonan-Objekt kann auch über eine `particle_hole_representation`-Eigenschaft verfügen.
Falls vorhanden, muss der Wert von `particle_hole_representation` dem im restlichen Teil dieses Abschnitts beschriebenen Format entsprechen.

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
Wenn der Wert von `index_convention` `mulliken`ist, muss ein Parser, der ein broombridge-Dokument lädt, für jedes Element der Menge von `two_electron_integrals` Arrays mit geringer Dichte einen hamiltonbegriff instanziieren, der mit dem zwei-Elektronen-Operator $h _ {i übereinstimmt. j, k, l} a ^ \ dagger_i a ^ \ dagger_j a_k a_l $, wobei $i $, $j $, $k $ und $l $ ganzzahlige Werte im inklusiven Bereich zwischen 1 und der Anzahl der von der `n_electrons`-Eigenschaft des integralen festgelegten Objekts angegebenen Elektronen sein müssen, und WHERE $h _ {i, j , k, l} $ ist das Element `[i, j, k, l, h(i, j, k, l)]` der Menge an Arrays mit geringer Dichte.

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

##### <a name="particlehole-representation-object"></a>Partikel – Loch-Darstellungs Objekt #####

Dieser Abschnitt ist normativ.

Das Objekt "Partikel – Hole-Darstellung" gibt an, dass die gespeicherten inteder in Bezug auf die Darstellung von Partikel Löchern definiert werden, wobei die Erstellungs-und Vernichtungs Operatoren die Entfernung vom verwendeten Verweis Zustand (z. b. einer Hartree) beschreiben. Fock-Zustand.
Das-Objekt ist optional.
Wenn das-Objekt nicht angegeben wird, wird die hamiltonan als nicht in der Darstellung eines Partikel Lochs angegeben interpretiert.
Falls vorhanden, muss der Wert `particle_hole_representation` ein Array mit geringer Array Menge sein, dessen Indizes vier ganze Zahlen und deren Werte eine Zahl und eine Zeichenfolge sind.
Der Zeichen folgen Teil des Werts der einzelnen Elemente darf nur die Zeichen `'+'` und `'-'` enthalten, der angibt, ob es sich bei einem angegebenen Faktor im Begriff um einen Erstellungs-oder Vernichtungs Operator in der Partikel – Loch-Darstellung handelt.  Beispielsweise `"-+++"` coresteiche auf eine Lücke, die an Site $i $ erstellt wird, und an den Standorten erstellte Partikel $j, k $ und $l $.

> [!NOTE]
> Da der Wert des `particle_hole_representation` ein Array Objekt mit geringer Dichte ist, müssen die Eigenschaften `unit` und `format` angegeben werden.
> Zulässige Einheiten sind in Tabelle 1 aufgeführt.
> Die `format`-Eigenschaft ist erforderlich und gibt an, ob die hamiltona-Koeffizienten als Array mit fester oder geringer Dichte angegeben werden.
> In der aktuellen Version werden nur sparsearrays unterstützt, wobei interpretiert wird, dass alle nicht angegebenen Elemente $0 $ sind. zukünftige Versionen können jedoch Unterstützung für zusätzliche Werte der `format`-Eigenschaft hinzufügen.

### <a name="initial-state-section"></a>Abschnitt "Anfangszustand" ###

Das initial_state_suggestion-Objekt gibt die anfänglichen Quantum-Zustände an, die für die angegebene hamiltonan von Interesse sind. Bei diesem Objekt muss es sich um ein Array von JSON-`state` Objekten handeln.

#### <a name="state-object"></a>State-Objekt ####

Jeder Status stellt eine übergeordnete Position der belegten Orbitals dar. Jedes Zustands Objekt muss über eine `label`-Eigenschaft verfügen, die eine Zeichenfolge enthält. Jedes Zustands Objekt muss über eine `superposition`-Eigenschaft verfügen, die ein Array von Basis Zuständen und deren nicht normalisierte Verstärkung enthält.

Der anfängliche Status lautet z. b. $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{e} = \bruchteil {0,1 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0.2 | ^ 2}} \ket{0} $ $ werden dargestellt am
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

#### <a name="basis-set-object"></a>Basis Objekt festlegen ####

Dieser Abschnitt ist normativ.

Jedes ganzzahlige Set-Objekt kann über eine `basis_set`-Eigenschaft verfügen.
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
