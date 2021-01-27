---
title: Microsoft- Q# Styleguide
description: Erlernen Sie die Benennungs-, Eingabe-, Dokumentations-und Formatierungs Konventionen für Q# Programme und Bibliotheken.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: contributor-guide
uid: microsoft.quantum.contributing.style
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2edd6baf7375415e395d15bac422168216bcff9a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852760"
---
# <a name="no-locq-style-guide"></a>Q# Styleguide #
## <a name="general-conventions"></a>Allgemeine Konventionen ##

Die in diesem Handbuch empfohlenen Konventionen sollen Ihnen helfen, Programme und Bibliotheken Q# leichter zu lesen und zu verstehen.

## <a name="guidance"></a>Anleitungen

Wir empfehlen Folgendes:

- Ignorieren Sie niemals eine Konvention, wenn Sie dies nicht absichtlich tun, um für Ihre Benutzer besser lesbaren und verständlichen Code bereitzustellen.

## <a name="naming-conventions"></a>Namenskonventionen ##

Beim anbieten des quantumentwicklungskit werden Funktions-und Vorgangs Namen unterstützt, mit denen Quantum-Entwickler Programme schreiben können, die leicht lesbar sind und die überraschen.
Ein wichtiger Aspekt dabei ist, dass wir bei der Auswahl von Namen für Funktionen, Vorgänge und Typen das *Vokabular* einrichten, mit dem Programmierer Quantum-Konzepte Ausdrücken. mit unseren Optionen können wir Sie bei der klaren Kommunikation unterstützen oder behindern.
Dies liegt in der Verantwortung für uns, sicherzustellen, dass die Namen, die wir einführen, eher Klarheit bieten als Verschleierung.
In diesem Abschnitt erfahren Sie, wie wir diese Verpflichtung in Bezug auf eine explizite Anleitung erfüllen, die uns bei der optimalen Durchführung der Q# Entwicklungs Community unterstützt.

### <a name="operations-and-functions"></a>Vorgänge und Funktionen ###

Eines der ersten Dinge, die ein Name einrichten sollte, ist, ob ein bestimmtes Symbol eine Funktion oder einen Vorgang darstellt.
Der Unterschied zwischen Funktionen und Vorgängen ist wichtig, um zu verstehen, wie sich ein Codeblock verhält.
Um den Unterschied zwischen Funktionen und Vorgängen an Benutzer zu übermitteln, basieren wir auf der Q# Verwendung von Nebeneffekten darauf, dass die Quantum-Vorgänge modelliert werden.
Dies *bedeutet* , dass ein Vorgang etwas bewirkt.

Im Gegensatz dazu beschreiben Funktionen die mathematischen Beziehungen zwischen den Daten.
Der Ausdruck `Sin(PI() / 2.0)` *ist* `1.0` , und impliziert nichts über den Zustand eines Programms oder seiner Qubits.

Durch die Zusammenfassung werden Vorgänge ausgeführt, während Functions Dinge sind.
Dieser Unterschied schlägt vor, dass wir Vorgänge als Verben und Funktionen als Nomen benennen.

> [!NOTE]
> Wenn ein benutzerdefinierter Typ deklariert wird, wird eine neue Funktion, die Instanzen dieses Typs erstellt, gleichzeitig implizit definiert.
> Aus dieser Sicht sollten benutzerdefinierte Typen als Nomen benannt werden, damit der Typ selbst und die Konstruktorfunktion konsistente Namen aufweisen.

Stellen Sie in angemessener Weise sicher, dass Vorgangs Namen mit Verben beginnen, die die Auswirkungen des Vorgangs eindeutig angeben.
Beispiel:

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

Ein Fall, der besondere Erwähnung verdient, ist, wenn ein Vorgang einen anderen Vorgang als Eingabe annimmt und ihn aufruft.
In solchen Fällen ist die vom Eingabevorgang ausgeführte Aktion nicht klar, wenn der äußere Vorgang definiert ist, sodass das Rechte Verb nicht sofort gelöscht wird.
Wir empfehlen das Verb `Apply` , wie in `ApplyIf` , `ApplyToEach` und `ApplyToFirst` .
Andere Verben können auch in diesem Fall nützlich sein, wie in `IterateThroughCartesianPower` .

| Verb | Erwarteter Effekt |
| ---- | ------ |
| Anwenden | Ein als Eingabe bereitgestellter Vorgang wird aufgerufen. |
| Assert | Eine Hypothese über das Ergebnis einer möglichen Quantum-Messung wird von einem Simulator geprüft. |
| Schätzung | Ein klassischer Wert wird zurückgegeben, der eine Schätzung darstellt, die aus einer oder mehreren Messungen gezeichnet wird. |
| Measure | Eine Quantum-Messung wird ausgeführt, und das Ergebnis wird an den Benutzer zurückgegeben. |
| Vorbereiten | Ein bestimmtes Register von Qubits wird in einem bestimmten Zustand initialisiert. |
| Beispiel | Ein klassischer Wert wird nach dem Zufallsprinzip aus einer Verteilung zurückgegeben. |

Bei Functions empfiehlt es sich, die Verwendung von Verben anstelle von gängigen Substantiven zu vermeiden (siehe Anleitungen zu den richtigen Nomen unten) oder Adjektive:

- `ConstantArray`
- `Head`
- `LookupFunction`

Vor allem empfiehlt es sich in fast allen Fällen, frühere Partizipationen zu verwenden, wenn dies angebracht ist, um anzugeben, dass ein Funktionsname an anderer Stelle in einem Quantum-Programm mit einer Aktion oder einem Nebeneffekt verbunden ist.
Verwendet beispielsweise  `ControlledOnInt` die Form teilnehmen des Verbs "Control", um anzugeben, dass die Funktion als Adjektiv fungiert, um das Argument zu ändern.
Dieser Name hat den zusätzlichen Vorteil, dass die Semantik des integrierten `Controlled` funktors übereinstimmt, wie weiter unten erläutert.
Ebenso können- _Agent-Nomen_ verwendet werden, um Funktions-und UDT-Namen aus Vorgangs Namen zu erstellen, wie im Fall des namens `Encoder` für einen UDT, der stark zugeordnet ist `Encode` .

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Verwenden Sie Verben für Vorgangs Namen.
- Verwenden Sie Nomen oder Adjektive für Funktionsnamen.
- Verwenden Sie Nomen für benutzerdefinierte Typen und Attribute.
- Verwenden Sie für alle Aufruf baren Namen eine `CamelCase` starke Bevorzugung von `pascalCase` , `snake_case` oder `ANGRY_CASE` . Stellen Sie insbesondere sicher, dass Aufruf Bare Namen mit Großbuchstaben beginnen.
- Verwenden Sie für alle lokalen Variablen `pascalCase` die starke bevorzugte Einstellung für `CamelCase` , `snake_case` oder `ANGRY_CASE` . Stellen Sie insbesondere sicher, dass lokale Variablen mit Kleinbuchstaben beginnen.
- Vermeiden Sie die Verwendung von unterstrichen `_` in Funktions-und Vorgangs Namen. wenn zusätzliche Ebenen der Hierarchie erforderlich sind, verwenden Sie Namespaces und Namespace Aliase.

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp;  | Name | Beschreibung |
|---|------|-------------|
| ☑ | `operation ReflectAboutStart` | Löschen Sie die Verwendung eines Verbs ("reflektieren"), um die Auswirkung des Vorgangs anzuzeigen. |
| ☒ | <s>`operation XRotation`</s> | Die Verwendung von Substantiv Phrase schlägt eine Funktion anstelle von Operation vor. |
| ☒ | <s>`operation search_oracle`</s> | Die Verwendung von verstößt gegen die `snake_case` Q# Notation. |
| ☒ | <s>`operation Search_Oracle`</s> | Die Verwendung von unterstrichen, die intern für den Vorgangs Namen verwendet werden, verstößt Q# |
| ☑ | `function StatePreparationOracle` | Die Verwendung des Substantiv Ausdrucks deutet darauf hin, dass die Funktion einen Vorgang zurückgibt. |
| ☑ | `function EqualityFact` | Löschen Sie die Verwendung von Substantiv ("Fakt"), um anzugeben, dass es sich hierbei um eine Funktion handelt, während das Adjektiv ist. |
| ☒ | <s>`function GetRotationAngles`</s> | Die Verwendung von Verb ("Get") deutet darauf hin, dass es sich hierbei um einen Vorgang handelt. |
| ☑ | `newtype GeneratorTerm` | Die Verwendung des Substantiv Ausdrucks verweist eindeutig auf das Ergebnis des Aufrufs des UDT-Konstruktors. |
| ☒ | <s>`@Attribute() newtype RunOnce()`</s> | Die Verwendung des Verb Ausdrucks deutet darauf hin, dass der UDT-Konstruktor ein Vorgang ist. |
| ☑ | `@Attribute() newtype Deprecated(Reason : String)` | Die Verwendung des nominalen Ausdrucks kommuniziert mit der Verwendung des-Attributs. |

***

### <a name="entry-points"></a>Einstiegspunkte

Beim Definieren eines Einstiegs Punkts in ein Q# Programm erkennt der Q# Compiler das- [ `@EntryPoint()` Attribut](xref:Microsoft.Quantum.Core.EntryPoint) , sodass die Einstiegspunkte einen bestimmten Namen aufweisen (z. b. `main` , `Main` oder `__main__` ).
Aus Sicht eines Q# Entwicklers sind Einstiegspunkte also normale Vorgänge, die mit kommentiert werden `@EntryPoint()` .
Außerdem sind Q# Einstiegspunkte möglicherweise Einstiegspunkte für eine gesamte Anwendung (z Q# . b. in eigenständigen ausführbaren Programmen) oder eine Schnittstelle zwischen einem Q# Programm und dem Host Programm für eine Anwendung (d.h. bei Verwendung Q# von mit Python oder .net), sodass der Name "Main" irreführend sein kann, wenn er auf einen Q# Einstiegspunkt angewendet wird.

Wir empfehlen die Verwendung von Benennungs Einstiegspunkten, um die Verwendung des `@EntryPoint()` Attributs anhand der allgemeinen Ratschläge für Benennungs Vorgänge widerzuspiegeln, die oben aufgeführt sind.


# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Benennen Sie keine Einstiegspunkt Vorgänge als "Main".
- Name der Einstiegspunkt Vorgänge als normale Vorgänge.

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp;  | Name | Beschreibung |
|---|------|-------------|
| ☑ | `@EntryPoint() operation RunSimulation` | Kommuniziert den Zweck des Einstiegs Punkts über den Vorgangs Namen eindeutig. |
| ☒ | <s>`@EntryPoint() operation Main`</s> | Die Verwendung von `Main` kommuniziert nicht eindeutig mit dem Zweck des Einstiegs Punkts und ist mit dem- `@EntryPoint()` Attribut redundant. |

**_

### <a name="shorthand-and-abbreviations"></a>Kurzformen und Abkürzungen ###

Ungeachtet der obigen Ratschläge gibt es eine Vielzahl von kurz Informationen, die die allgemeine und weit verbreitete Verwendung von Quantum Computing sehen.
Es wird empfohlen, vorhandene und allgemeine kurzwerte zu verwenden, und wo Sie vorhanden sind, insbesondere bei Vorgängen, die für den Betrieb eines Ziel Computers intrinsisch sind.
Wir wählen beispielsweise den Namen `X` anstelle von `ApplyX` und `Rz` anstelle von aus `RotateAboutZ` .
Wenn Sie diese Kurznamen verwenden, sollten Vorgangs Namen Großbuchstaben sein (z. b. `MAJ` ).

Im Fall von häufig verwendeten Akronymen und Initialisierungen, wie z. b. "QFT" für "Quantum Fourier Transform", ist Vorsicht geboten.
Es empfiehlt sich, allgemeine .net-Konventionen für die Verwendung von Akronymen und initialismen in vollständigen Namen zu befolgen, die Folgendes vorschreiben:

- Akronyme mit zwei Buchstaben und Initialisierungen werden in Großbuchstaben benannt (z. b. `BE` für "Big-in").
- Alle längeren Akronyme und Initialisierer werden in benannt `CamelCase` (z. b. `Qft` für "Quantum Fourier Transform").

Folglich kann ein Vorgang, der den QFT implementiert, entweder `QFT` als Kurzform oder als ausgeschrieben bezeichnet werden `ApplyQft` .

Bei besonders häufig verwendeten Vorgängen und Funktionen ist es möglicherweise wünschenswert, einen Kurznamen als _Alias_ für eine längere Form bereitzustellen:

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Beachten Sie ggf. häufig akzeptierte und häufig verwendete Kurznamen.
- Verwenden Sie Großbuchstaben für Kurzformen.
- Verwenden Sie für kurze (aus zwei Buchstaben bestehende) Akronyme und Initialisierungen Großbuchstaben.
- Verwenden Sie `CamelCase` für längere (drei oder mehr Buchstaben) Akronyme und Initialisierer.

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp;   | Name | Beschreibung |
|---|------|-------------|
| ☑ | `X` | Wohl verständliche Kurzformen für "Apply a $X $ Transformation" |
| ☑ | `CNOT` | Wohl verständliche Kurzformen für "kontrolliert-not" |
| ☒ | <s>`Cnot`</s> | Kurzformen dürfen nicht in sein `CamelCase` . |
| ☑ | `ApplyQft` | Der allgemeine initialismus "QFT" wird als Teil eines langen Namens angezeigt. |
| ☑ | `QFT` | Allgemeine Initialisierung "QFT" wird als Teil einer Kurzform angezeigt. |



_*_


### <a name="proper-nouns-in-names"></a>Richtige Nomen in Namen ###

In der Physik ist es üblich, die Dinge nach der ersten Person zu benennen, um Sie zu veröffentlichen. die meisten nicht-Physikern sind nicht mit den Namen aller Benutzer und dem gesamten Verlauf vertraut.
Wenn Sie sich zu stark auf Benennungs Konventionen der Physik verlassen, kann dies zu einer beträchtlichen Barriere für die Eingabe führen, da Benutzer aus anderen Hintergründen eine große Anzahl scheinbar undurchsichtiger Namen erlernen müssen, um allgemeine Vorgänge und Konzepte zu verwenden.
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
Daher wird empfohlen, dass, soweit sinnvoll, gängige Nomen, die ein Konzept beschreiben, für die richtigen Nomen, die den Veröffentlichungs Verlauf eines Konzepts beschreiben, eine starke Bevorzugung annehmen.
Ein bestimmtes Beispiel ist, dass der einzeln gesteuerte Swap-Vorgang und der doppelt kontrollierte not-Vorgang in Academic Literatur oft als "Fredkin"-und "deffoli"-Vorgänge bezeichnet werden, die jedoch in Q# erster Linie als und identifiziert werden `CSWAP` `CCNOT` .
In beiden Fällen enthalten die API-Dokumentations Kommentare Synonyme, die auf den richtigen Substantiven basieren, sowie alle entsprechenden citierungen.

Diese Einstellung ist besonders wichtig, da eine bestimmte Verwendung von richtigen Nomen immer erforderlich ist – Q# folgt der von vielen klassischen Sprachen festgelegten Tradition und bezieht sich auf Typen als `Bool` Verweis auf die boolesche Logik, die wiederum in Bezug auf George Boole benannt wird.
Einige Quantum-Konzepte werden ähnlich benannt, einschließlich des in `Pauli` die Sprache integrierten Typs Q# .
Wenn Sie die Verwendung von richtigen Nomen minimieren, bei denen eine solche Verwendung nicht wesentlich ist, verringern wir die Auswirkungen, bei denen die richtigen Nomen nicht vernünftig vermieden werden können.

# <a name="guidance"></a>[Leitfaden](#tab/guidance) 

Wir empfehlen Folgendes:

- Vermeiden Sie die Verwendung von richtigen Substantiven in Namen.

# <a name="examples"></a>[Beispiele](#tab/examples)

_*_

### <a name="type-conversions"></a>Typkonvertierungen ###

Da Q# eine stark und statisch typisierte Sprache ist, kann ein Wert eines Typs nur als Wert eines anderen Typs mithilfe eines expliziten Aufrufes einer Typkonvertierungs Funktion verwendet werden.
Dies steht im Gegensatz zu Sprachen, die es ermöglichen, Typen implizit (z. b. typherauf Stufung) oder durch Umwandlung zu ändern.
Typkonvertierungs Funktionen spielen daher eine wichtige Rolle bei der Q# Bibliotheksentwicklung und bilden eine der gängigsten Entscheidungen zum benennen.
Es ist jedoch zu beachten, dass Typkonvertierungen immer _deterministisch_ sind. Sie können als Funktionen geschrieben werden und fallen daher unter den obigen Empfehlungen.
Insbesondere wird empfohlen, dass Typkonvertierungs Funktionen nie als Verben (z. b. `ConvertToX` ) oder adverbfilter-präpositional-Ausdrücke () benannt werden `ToX` . Sie sollten jedoch als Adjektiv-Ausdrücke mit präpositional bezeichnet werden, die die Quell-und Zieltypen angeben ( `XAsY` ).
Beim Auflisten von Array Typen in Namen der Typkonvertierungs Funktion wird die Kurzform empfohlen `Arr` .
Abgesehen von Ausnahmefällen wird empfohlen, dass alle Typkonvertierungs Funktionen mit benannt werden, `As` damit Sie schnell identifiziert werden können.

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Wenn eine Funktion einen Wert vom Typ `X` in einen Wert vom Typ konvertiert `Y` , verwenden Sie entweder den Namen `AsY` oder `XAsY` .

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp;   | Name | Beschreibung |
|---|------|-------------|
| ☒ | <s>`ToDouble`</s> | Die Vorposition "to" führt zu einem Verb Ausdruck, der einen Vorgang und keine Funktion angibt. |
| ☒ | <s>`AsDouble`</s> | Der Eingabetyp ist aus dem Funktionsnamen nicht eindeutig. |
| ☒ | <s>`PauliArrFromBoolArr`</s> | Die Eingabe-und Ausgabetypen werden in der falschen Reihenfolge angezeigt. |
| ☑ | `ResultArrAsBoolArr` | Die Eingabe-und Ausgabetypen sind eindeutig. |

_*_

### <a name="private-or-internal-names"></a>Private oder interne Namen ###

In vielen Fällen ist ein Name ausschließlich für die interne Verwendung in einer Bibliothek oder einem Projekt vorgesehen und ist kein garantierter Teil der API, die von einer Bibliothek angeboten wird.
Es ist hilfreich, eindeutig anzugeben, dass dies der Fall ist, wenn Funktionen und Vorgänge benannt werden, damit versehentlich Abhängigkeiten von internem Code offensichtlich werden.
Wenn ein Vorgang oder eine Funktion nicht für die direkte Verwendung vorgesehen ist, sondern stattdessen von einer übereinstimmenden Aufruf baren Funktion verwendet werden soll, die von einer partiellen Anwendung verwendet wird, empfiehlt es sich, einen Namen zu verwenden, der mit dem `internal` Schlüsselwort für die Aufruf Bare-Aktivität beginnt

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Wenn eine Funktion, ein Vorgang oder ein benutzerdefinierter Typ nicht Teil der öffentlichen API für eine Q# Bibliothek oder ein Programm ist, stellen Sie sicher, dass Sie als intern gekennzeichnet ist, indem Sie das `internal` Schlüsselwort vor der- `function` ,-oder- `operation` `newtype` Deklaration platzieren.

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp;  | Name | Beschreibung |
|---|------|-------------|
| ☒ | <s>`operation _ApplyDecomposedOperation`</s> | Verwenden Sie keinen Unterstrich `_` , um anzugeben, dass dieser Vorgang nur für die interne Verwendung vorgesehen ist. |
| ☑ | `internal operation ApplyDecomposedOperation` | Das `internal` Schlüsselwort am Anfang weist eindeutig darauf hin, dass dieser Vorgang nur für die interne Verwendung vorgesehen ist. |

_*_
### <a name="variants"></a>Varianten ###

Obwohl diese Einschränkung in zukünftigen Versionen von möglicherweise nicht beibehalten wird Q# , ist es aktuell, dass häufig Gruppen verwandter Vorgänge oder Funktionen vorhanden sind, die durch die von Ihnen unterstützten Funktoren unterschieden werden, oder durch die konkreten Typen ihrer Argumente.
Diese Gruppen können unterschieden werden, indem der gleiche Stamm Name verwendet wird, gefolgt von einem oder zwei Buchstaben, die die Variante angeben.

| Suffix | Bedeutung |
|--------|---------|
| `A` | Für die Unterstützung erwartete Eingabe `Adjoint` |
| `C` | Für die Unterstützung erwartete Eingabe `Controlled` |
| `CA` | Es wurde eine Eingabe erwartet, die `Controlled` und `Adjoint` |
| `I` | Eingabe oder Eingaben weisen den Typ auf. `Int` |
| `D` | Eingabe oder Eingaben weisen den Typ auf. `Double` |
| `L` | Eingabe oder Eingaben weisen den Typ auf. `BigInt` |

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Wenn eine Funktion oder ein Vorgang nicht mit ähnlichen Funktionen oder Vorgängen durch die Typen und die Funktions Unterstützung Ihrer Eingaben verknüpft ist, verwenden Sie kein Suffix.
- Wenn eine Funktion oder ein Vorgang mit ähnlichen Funktionen oder Vorgängen verknüpft ist, die von den Typen und der funktorunterstützung Ihrer Eingaben verwendet werden, verwenden Sie Suffixe wie in der obigen Tabelle, um Varianten zu unterscheiden.

# <a name="examples"></a>[Beispiele](#tab/examples)

_*_

### <a name="arguments-and-variables"></a>Argumente und Variablen ###

Ein wichtiges Ziel des Q# Codes für eine Funktion oder einen Vorgang besteht darin, den Code einfach zu lesen und zu verstehen.
Ebenso sollten die Namen von Eingaben und Typargumenten kommunizieren, wie eine Funktion oder ein Argument nach der Bereitstellung verwendet wird.


# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Verwenden Sie für alle Variablen-und Eingabe Namen `pascalCase` die starke bevorzugte Einstellung für `CamelCase` , `snake_case` oder `ANGRY_CASE` .
- Eingabe Namen sollten beschreibend sein. vermeiden Sie, wenn möglich, einen oder zwei Buchstaben.
- Vorgänge und Funktionen, die genau ein Typargument akzeptieren, sollten das Typargument von angeben, `T` wenn seine Rolle offensichtlich ist.
- Wenn eine Funktion oder ein Vorgang mehrere Typargumente annimmt oder wenn die Rolle eines einzelnen Typarguments nicht offensichtlich ist, sollten Sie die Verwendung eines kurzen Großbuchstaben mit vorangestelltem Wort `T` (z. b. `TOutput` ) für jeden Typ in Erwägung gezogen.
- Geben Sie keine Typnamen in Argument-und Variablennamen ein. Diese Informationen können von Ihrer Entwicklungsumgebung bereitgestellt werden.
- Kennzeichnen Sie skalare Typen nach Ihren Literalnamen ( `flagQubit` ) und Array Typen durch einen Plural ( `measResults` ).
  Vor allem bei Arrays von Qubits sollten diese Typen in Erwägung gezogen werden, `Register` Wenn der Name auf eine Sequenz von Qubits verweist, die in irgendeiner Weise eng miteinander verknüpft sind.
- Variablen, die als Indizes in Arrays verwendet werden, sollten mit beginnen `idx` und als Singular (z. b.) verwendet werden `things[idxThing]` .
  Vermeiden Sie insbesondere die Verwendung von Variablennamen mit nur einem Buchstaben als Indizes. Verwenden Sie `idx` ggf. mindestens.
- Variablen, die zum Speichern der Längen von Arrays verwendet werden, sollten mit beginnen `n` und pluralisiert werden (z. b. `nThings` ).

# <a name="examples"></a>[Beispiele](#tab/examples)

_*_

### <a name="user-defined-type-named-items"></a>Benannte Elemente User-Defined Typs ###

Benannte Elemente in benutzerdefinierten Typen sollten als benannt werden `CamelCase` , auch als Eingabe für UDT-Konstruktoren.
Dadurch können benannte Elemente bei Verwendung der accessornotation (z. b. `callable::Apply` ) oder der Copy-and-Update-Notation () eindeutig von Verweisen auf lokale Variablen getrennt werden `set arr w/= Data <- newData` .

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Benannte Elemente in UDT-Konstruktoren sollten als benannt werden, d `CamelCase` . h., Sie sollten mit einem anfänglichen Großbuchstaben beginnen.
- Benannte Elemente, die in Vorgänge aufgelöst werden, sollten als Verb Phasen benannt werden.
- Benannte Elemente, die nicht in Vorgänge aufgelöst werden, sollten als nominale Ausdrücke benannt werden.
- Für UDTs, die Vorgänge einschließen, sollte ein einzelnes benanntes Element mit dem Namen `Apply` definiert werden.

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp;  | Codeausschnitt | Beschreibung |
|---|---------|-------------|
| ☑ | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | Der Name `Apply` ist ein `CamelCase` -formatierter Verb Ausdruck, der darauf hinweist, dass das benannte Element ein Vorgang ist. |
| ☒ | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | Benannte Elemente sollten mit einem ersten Großbuchstaben beginnen. |
| ☒ | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | Benannte Elemente, die in Functions aufgelöst werden, sollten als nominale Ausdrücke und nicht als Verb Ausdrücke benannt werden. |

_*_

## <a name="input-conventions"></a>Eingabe Konventionen ##

Wenn ein Entwickler einen Vorgang oder eine Funktion aufruft, müssen die verschiedenen Eingaben für diesen Vorgang bzw. diese Funktion in einer bestimmten Reihenfolge angegeben werden. dadurch erhöht sich die kognitive Auslastung eines Entwicklers, um eine Bibliothek verwenden zu können.
Vor allem ist die Aufgabe des hintergabeorderings häufig eine Ablenkungs Maßnahme von der Aufgabe, die eine Implementierung eines Quantum-Algorithmus zu programmieren.
Obwohl die Unterstützung für umfangreiche IDE dies sehr stark mindern kann, kann ein guter Entwurf und die Einhaltung allgemeiner Konventionen dazu beitragen, die durch eine API erzwungene kognitive Auslastung zu minimieren.

Wenn möglich, kann es hilfreich sein, die Anzahl der Eingaben zu verringern, die von einem Vorgang oder einer Funktion erwartet werden, damit die Rolle der einzelnen Eingaben sowohl für Entwickler, die diesen Vorgang oder diese Funktion aufrufen, als auch für Entwickler, die diesen Code später lesen, gleichzeitig offensichtlich ist.
Besonders wenn es nicht möglich oder sinnvoll ist, die Anzahl der Argumente für einen Vorgang oder eine Funktion zu reduzieren, ist es wichtig, dass eine konsistente Reihenfolge vorhanden ist, die die Überraschung des Benutzers beim Vorhersagen der Reihenfolge der Eingaben minimiert.

Wir empfehlen eine Eingabe Reihenfolge Konventionen, die größtenteils von der Betrachtung einer partiellen Anwendung als Generalisierung von f (x, y) ≡ f (x) (y) abgeleitet ist.
Folglich sollte das partielle anwenden der ersten Argumente zu einem Aufruf baren Ergebnis führen, das immer nützlich ist, wenn dies angemessen ist.
Nach diesem Prinzip sollten Sie die folgende Reihenfolge von Argumenten verwenden:

- Klassische, nicht Aufruf Bare Argumente, wie z. b. Winkel, Vektoren von Mächten usw.
- Aufruf Bare Argumente (Funktionen und Argumente).
  Wenn sowohl Funktionen als auch Vorgänge als Argumente verwendet werden, erwägen Sie das Platzieren von Vorgängen nach Funktionen.
- Auflistungen, auf die durch Aufruf Bare Argumente in ähnlicher Weise wie `Map` , `Iter` , und agiert werden `Enumerate` `Fold` .
- Als Steuerelemente verwendete Qubit-Argumente.
- Als Ziele verwendete Qubit-Argumente.

Stellen Sie sich einen Vorgang `ApplyPhaseEstimationIteration` zur Verwendung in der Phasen Schätzung vor, der einen Winkel und einen Oracle annimmt, den Winkel `Rz` von einem Array mit unterschiedlichen Skalierungsfaktoren an geändert übergibt und dann Anwendungen des Oracle steuert.
Wir würden die Eingaben `ApplyPhaseEstimationIteration` folgendermaßen sortieren:

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
Im besonderen Fall, dass eine Überraschung minimiert wird, imitieren einige Funktionen und Vorgänge das Verhalten der integrierten Funktoren `Adjoint` und `Controlled` .
Hat z. b. den- `ControlledOnInt<'T>` Typ `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` , z. b. `ControlledOnInt<Qubit[]>(5, _)` wie das- `Controlled` Funktor, aber für die Bedingung, dass das Steuerelement registriert den Status $ \ket {5} = \ket {101} $ darstellt.
Daher erwartet ein Entwickler, dass die Eingaben `ControlledOnInt` den aufrufenden, der zuletzt transformiert wird, und dass der resultierende Vorgang als Eingabe `(Qubit[], 'T)` ---der gleichen Reihenfolge wie die Ausgabe des `Controlled` funktors.

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Verwenden Sie Eingabe Sortierungen in Übereinstimmung mit der Verwendung der partiellen Anwendung.
- Verwenden Sie Eingabe Sortierungen, die mit integrierten Funktoren konsistent sind.
- Platzieren Sie alle klassischen Eingaben vor allen Quantum-Eingaben.

# <a name="examples"></a>[Beispiele](#tab/examples)

_*_

## <a name="documentation-conventions"></a>Konventionen in der Dokumentation ##

Die Q# Sprache ermöglicht das Anfügen von Dokumentationen an Vorgänge, Funktionen und benutzerdefinierte Typen durch die Verwendung von speziell formatierten Dokumentations Kommentaren.
Diese Dokumentations Kommentare sind durch drei Schrägstriche () gekennzeichnet und `///` sind kleine [markdown-Dokumente mit docfx-Geschmack](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) , mit denen der Zweck der einzelnen Vorgänge, Funktionen und benutzerdefinierten Typen beschrieben werden kann, welche Eingaben jeweils erwartet werden usw.
Der mit dem Quantum Development Kit bereitgestellte Compiler extrahiert diese Kommentare und verwendet diese, um die besitzen-Dokumentation in ähnlicher Weise wie bei zu unterstützen https://docs.microsoft.com/quantum .
Entsprechend verwendet der Sprachserver, der mit dem Quantum Development Kit bereitgestellt wird, diese Kommentare, um Benutzern Hilfe zu bieten, wenn Sie mit dem Mauszeiger auf Symbole in Ihrem Q# Code zeigen.
Durch die Verwendung von Dokumentations Kommentaren können Benutzer den Code sinnvoll machen, indem Sie einen nützlichen Verweis auf Details bereitstellen, die nicht ohne weiteres mit den anderen Konventionen in diesem Dokument ausgedrückt werden.

> [!div class="nextstepaction"]
> [Syntax Referenz für Dokumentations Kommentare](xref:microsoft.quantum.qsharp.comments#documentation-comments).

Um diese Funktionalität für Benutzer effektiv nutzen zu können, empfiehlt es sich, beim Schreiben von Dokumentations Kommentaren einige Punkte zu berücksichtigen.

# <a name="guidance"></a>[Leitfaden](#tab/guidance)

Wir empfehlen Folgendes:

- Jeder öffentlichen Funktion, jedem Vorgang und jedem benutzerdefinierten Typ sollte unmittelbar ein Dokumentations Kommentar vorangestellt werden.
- Jeder Dokumentations Kommentar sollte mindestens die folgenden Abschnitte enthalten:
    - Zusammenfassung
    - Eingabe
    - Ausgabe (falls zutreffend)
- Stellen Sie sicher, dass alle Zusammenfassungen zwei oder weniger Sätze sind. Wenn mehr Platz benötigt wird, geben Sie einen `# Description` direkt folgenden Abschnitt `# Summary` mit umfassenden Details an.
- Wenn Sie vernünftig Vorgehen, sollten Sie mathematische nicht in Zusammenfassungen einschließen, da nicht alle Clients eine TeX-Notation in Zusammenfassungen unterstützen. Beachten Sie, dass beim Schreiben von Prosa Dokumenten (z. b. tex oder markdown) die Verwendung längerer Zeilenlängen vorzuziehen ist.
- Stellen Sie alle relevanten mathematischen Ausdrücke im- `# Description` Abschnitt bereit.
- Wenn Sie Eingaben beschreiben, wiederholen Sie nicht die Typen der einzelnen Eingaben, da diese vom Compiler abgeleitet werden können, und das Risiko der Inkonsistenz.
- Geben Sie nach Bedarf Beispiele an, die jeweils in einem eigenen Abschnitt enthalten sind `# Example` .
- Beschreiben Sie kurz die einzelnen Beispiele, bevor Sie Code auflisten.
- Nennen Sie alle relevanten akademischen Veröffentlichungen (z. b. Beiträge, Verfahren, Blogbeiträge und alternative Implementierungen) in einem `# References` Abschnitt als Auflistungs Liste mit Links.
- Stellen Sie sicher, dass, sofern möglich, alle anfügelinks zu permanenten und unveränderlichen bezeichmern (Dois-oder versionierte arXiv-Nummern) gehören.
- Wenn ein Vorgang oder eine Funktion mit anderen Vorgängen oder Funktionen verknüpft ist, können Sie im Abschnitt andere Varianten als Aufzählungs Zeichen auflisten `# See Also` .
- Belassen Sie eine leere Kommentar Linie zwischen den Abschnitten der Ebene-1 ( `/// #` ), lassen Sie jedoch keine Leerzeile zwischen den Abschnitten der Ebene 2 ( `/// ##` ).

# <a name="examples"></a>[Beispiele](#tab/examples)

#### <a name=""></a>☑ ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

_*_

## <a name="formatting-conventions"></a>Formatierungs Konventionen ##

Zusätzlich zu den oben genannten Vorschlägen ist es hilfreich, den Code so lesbar wie möglich zu machen, um konsistente Formatierungs Regeln zu verwenden.
Diese Formatierungs Regeln sind eher willkürlich und stark bis zur persönlichen Ästhetik.
Trotzdem empfiehlt es sich, einen konsistenten Satz von Formatierungs Konventionen innerhalb einer Gruppe von Projektmitarbeitern zu verwalten, insbesondere für große Q# Projekte wie das Quantum Development Kit selbst.
Diese Regeln können automatisch mithilfe des in den Compiler integrierten Formatierungs Tools angewendet werden Q# .

# <a name="guidance"></a>[Leitfaden](#tab/guidance) 

Wir empfehlen Folgendes:

- Verwenden Sie vier Leerzeichen anstelle von Registerkarten für die Portabilität.
  Beispielsweise in vs Code:
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- Zeilenumbruch um 79 Zeichen, soweit angemessen.
- Verwenden Sie Leerzeichen um binäre Operatoren.
- Verwenden Sie Leerzeichen auf beiden Seiten von Doppelpunkten, die für Typanmerkungen verwendet werden.
- Verwenden Sie ein einzelnes Leerzeichen nach Kommas, das in Array-und tupelliteralen verwendet wird (z. b. in Eingaben für Funktionen und Vorgänge).
- Verwenden Sie keine Leerzeichen nach Funktions-, Vorgangs-oder UDT-Namen oder nach den `@` in-Attribut Deklarationen.
- Jede Attribut Deklaration sollte sich in einer eigenen Zeile befinden.

# <a name="examples"></a>[Beispiele](#tab/examples)

| &nbsp; | Codeausschnitt | Beschreibung |
|---|---------|-------------|
| ☒ | <s>`2+3`</s> | Verwenden Sie Leerzeichen um binäre Operatoren. |
| ☒ | <s>`target:Qubit`</s> | Verwenden Sie Leerzeichen um Doppelpunkte der Typanmerkung. |
| ☑ | `Example(a, b, c)` | Elemente im eingabetupel sind zur besseren Lesbarkeit ordnungsgemäß verteilt. |
| ☒ | <s>`Example (a, b, c)`</s> | Leerzeichen sollten nach Funktions-, Vorgangs-oder UDT-Namen unterdrückt werden. |

_**
