---
title: Q#API-Entwurfs Prinzipien
description: Q#API-Entwurfs Prinzipien
author: cgranade
ms.author: chgranad
ms.date: 3/9/2020
ms.topic: article
uid: microsoft.quantum.contributing.api-design
no-loc:
- Q#
- $$v
ms.openlocfilehash: 580fcaea575ff544ed2c5f31eba7e963bea4534b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866892"
---
# <a name="no-locq-api-design-principles"></a>Q#API-Entwurfs Prinzipien

## <a name="introduction"></a>Einführung

Als Sprache und als Plattform ermöglicht Benutzern das Q# schreiben, ausführen, verstehen und untersuchen von Quantum-Anwendungen.
Um den Benutzern beim Entwerfen Q# von Bibliotheken zu helfen, befolgen wir eine Reihe von API-Entwurfs Prinzipien, um unsere Entwürfe zu unterstützen und uns dabei zu unterstützen, für die Quantum-Entwicklungs Community verwendbare Bibliotheken zu erstellen.
In diesem Artikel werden diese Grundsätze aufgeführt, und es werden Beispiele zum Anwenden der APIs beim Entwerfen von Q# APIs erläutert.

> [!TIP]
> Dies ist ein Recht detailliertes Dokument, das Sie bei der Entwicklung von Bibliotheken und ausführlichen Bibliotheks Beiträgen unterstützen soll.
> Sie finden es wahrscheinlich am nützlichsten, wenn Sie Ihre eigenen Bibliotheken in schreiben Q# , oder wenn Sie [ Q# ](https://github.com/microsoft/QuantumLibraries)größere Features zum bibliothektrepository beitragen.
>
> Wenn Sie jedoch erfahren möchten, wie Sie im Allgemeinen an das Quantum Development Kit mitwirken, empfehlen wir Ihnen, mit dem [Beitrags Handbuch](xref:microsoft.quantum.contributing)zu beginnen.
> Wenn Sie allgemeinere Informationen über das Formatieren Ihres Codes suchen, sind Q# Sie möglicherweise daran interessiert, sich das [Styleguide](xref:microsoft.quantum.contributing.style)anzusehen.

## <a name="general-principles"></a>Allgemeine Prinzipien

**Schlüsselprinzip:** Verfügbar machen von APIs, die den Schwerpunkt auf Quantum-Anwendungen legen.

- ✅**Wählen Sie** Vorgangs-und Funktionsnamen aus, die die allgemeine Struktur von Algorithmen und Anwendungen widerspiegeln.
- ⛔️ **keine** APIs verfügbar machen, die sich hauptsächlich auf Low-Level-Implementierungsdetails konzentrieren.

**Schlüsselprinzip:** Starten Sie jeden API-Entwurf mit Beispiel Anwendungsfällen, um sicherzustellen, dass die APIs intuitiv verwendet werden können.

- ✅Stellen **Sie** sicher, dass jede Komponente einer öffentlichen API über einen entsprechenden Anwendungsfall verfügt, anstatt zu versuchen, alle möglichen Verwendungsmöglichkeiten von Anfang an zu entwerfen.
    Anders ausgedrückt: führen Sie keine öffentlichen APIs ein, wenn Sie nützlich sind, aber stellen Sie sicher, dass jeder Teil einer API ein *konkretes* Beispiel hat, in dem es nützlich ist.

  *Beispiele:*
  - @"microsoft.quantum.canon.applytoeachca"kann verwendet werden `ApplyToEachCA(H, _)` , um die Registrierung in einem einheitlichen Status der übergeordneten Position vorzubereiten, eine gängige Aufgabe in vielen Quantenalgorithmen. Der gleiche Vorgang kann auch für viele andere Aufgaben in Vorbereitungs-, Numerics-und Oracle-basierten Algorithmen verwendet werden.

- ✅**Verwenden Sie** die neuen API-Entwürfe für Brainstorming und Workshop, um zu überprüfen, ob Sie intuitiv sind und vorgeschlagene Anwendungsfälle erfüllen.

  *Beispiele:*
  - \#Überprüfen Sie den aktuellen Q-Code, um zu sehen, wie neue API-Entwürfe vorhandene Implementierungen vereinfachen und verdeutlichen könnten
  - Überprüfen Sie die vorgeschlagenen API-Entwürfe mit Vertretern primärer Zielgruppen.

**Schlüsselprinzip:** Entwerfen Sie APIs zum unterstützen und fördern lesbaren Codes.

- ✅Stellen **Sie** sicher, dass der Code von Domänen Experten und nicht-Experten gleichermaßen lesbar ist.
- ✅**Legen Sie** den Fokus auf die Auswirkungen der einzelnen Vorgänge und Funktionen innerhalb des Algorithmus auf hoher Ebene, und verwenden Sie die Dokumentation, um die Implementierungsdetails nach Bedarf zu vertiefen.
- ✅**Befolgen Sie** ggf. das gängige [Q- \# Stil Handbuch](xref:microsoft.quantum.contributing.style) .

**Schlüsselprinzip:** Entwerfen Sie APIs so, dass Sie stabil sind und eine Vorwärtskompatibilität gewährleisten.

- ✅**Stellen Sie** alte APIs ordnungsgemäß als veraltet ein, wenn wichtige Änderungen erforderlich sind.

- ✅Stellen **Sie** "Shim"-Vorgänge und-Funktionen bereit, mit denen vorhandener Benutzercode während der Veraltung ordnungsgemäß ausgeführt werden kann.

  *Beispiele:*
  - Wenn Sie einen Vorgang mit dem Namen zu umbenennen `EstimateExpectation` `EstimateAverage` , führen Sie einen neuen Vorgang mit dem Namen ein, `EstimateExpectation` der den ursprünglichen Vorgang unter seinem neuen Namen aufruft, damit vorhandener Code weiterhin ordnungsgemäß funktionieren kann.

- ✅Verwenden **Sie** das- @"microsoft.quantum.core.deprecated" Attribut, um dem Benutzer veraltete Anwendungen mitzuteilen.

- ✅Wenn Sie einen Vorgang oder eine Funktion umbenennen, geben **Sie** den neuen Namen als Zeichen folgen Eingabe an `@Deprecated` .

- ⛔️ **nicht** vorhandene Funktionen oder Vorgänge ohne einen veralteten Zeitraum von mindestens sechs Monaten für Vorschau Releases oder mindestens zwei Jahre für unterstützte Releases entfernen.

## <a name="functions-and-operations"></a>Funktionen und Vorgänge

**Schlüssel** Prinzipal: Stellen Sie sicher, dass jede Funktion und jeder Vorgang innerhalb der API genau definiert ist.

- ⛔️ **keine** Funktionen und Vorgänge verfügbar machen, die mehrere nicht zusammenhängende Tasks ausführen.

**Schlüsselprinzip:** entwerfen Sie Funktionen und Vorgänge so, dass Sie so wiederverwendbar wie möglich sind, und um zukünftige Anforderungen zu antizipieren.

- ✅Arbeiten **Sie** mit den Entwurfsfunktionen und-Vorgängen zusammen mit anderen Funktionen und Vorgängen zusammen, sowohl in derselben API als auch in bereits vorhandenen Bibliotheken.

  *Beispiele:*
  - Der @"microsoft.quantum.canon.delay" Vorgang nimmt nur minimale Annahmen über seine Eingaben an und kann daher verwendet werden, um Anwendungen von entweder in der Q# Standardbibliothek oder gemäß der Definition durch die Benutzer zu verzögern.
    <!-- TODO: define bad example. -->

- ✅**Machen Sie** rein deterministische Klassische Logik als Funktionen anstelle von Vorgängen verfügbar.

  *Beispiele:*
  - Eine Unterroutine, bei der die Gleit Komma Eingabe als Quadrate festgelegt wird, kann deterministisch geschrieben werden, sodass Sie dem Benutzer als `Squared : Double -> Double` nicht als Vorgang angezeigt werden soll `Square : Double => Double` . Dadurch kann die Unterroutine an mehr Stellen aufgerufen werden (z. b. innerhalb anderer Funktionen) und nützliche Optimierungs Informationen für den Compiler bereitstellen, die sich auf die Leistung und Optimierungen auswirken können.
  - `ForEach<'TInput, 'TOutput>('TInput => 'TOutput, 'TInput[]) => 'TOutput[]`und `Mapped<'TInput, 'TOutput>('TInput -> 'TOutput, 'TInput[]) -> 'TOutput[]` unterscheiden sich in Bezug auf den Determinismus. beide sind in unterschiedlichen Situationen nützlich.
  - API-Routinen, die die Anwendung von Quantum-Vorgängen transformieren, können oft auf deterministische Weise ausgeführt werden und können daher als Funktionen wie z. b. zur Verfügung gestellt werden `CControlled<'T>(op : 'T => Unit) => ((Bool, 'T) => Unit)` .

- ✅Generalisieren **Sie** den Eingabetyp für jede Funktion und jeden Vorgang bei Bedarf mit Typparametern.

  *Beispiele:*
  - `ApplyToEach`weist den-Typ `<'T>(('T => Unit), 'T[]) => Unit` anstelle des spezifischen Typs der am häufigsten verbreiteten Anwendung auf `((Qubit => Unit), Qubit[]) => Unit` .

> [!TIP]
> Es ist wichtig, zukünftige Anforderungen zu antizipieren, aber es ist auch wichtig, konkrete Probleme für Ihre Benutzer zu lösen.
> Wenn Sie dieses Schlüsselprinzip anwenden, müssen Sie immer sorgfältige Überlegungen und einen Lastenausgleich durcharbeiten, um zu vermeiden, dass die APIs "nur in

**Schlüssel** Prinzipal: Wählen Sie Eingabe-und Ausgabetypen für Funktionen und Vorgänge aus, die vorhersagbar sind und die den Zweck einer Aufruf baren Funktion übermitteln.

- ✅Verwenden **Sie** Tupeltypen, um Eingaben und Ausgaben logisch zu gruppieren, die nur bei einer gemeinsamen Verwendung von Bedeutung sind. In diesen Fällen sollten Sie einen benutzerdefinierten Typ verwenden.

  *Beispiele:*
  - Eine Funktion, die das lokale Mindestwerte einer anderen Funktion ausgibt, muss möglicherweise die Grenzen eines Such Intervalls als Eingabe annehmen, sodass `LocalMinima(fn : (Double -> Double), (left : Double, right : Double)) : Double` möglicherweise eine geeignete Signatur ist.
  - Ein Vorgang, mit dem eine Ableitung eines Machine Learning-Klassifizierers mithilfe der Parameter Verschiebungs Technik geschätzt wird, muss möglicherweise sowohl den verschobenen als auch den nicht gestuften Parameter Vektoren als Eingaben verwenden. `(unshifted : Double[], shifted : Double[])`In diesem Fall ist möglicherweise eine Eingabe vergleichbar mit.

- ✅Ordnen **Sie** Elemente in Eingabe-und ausgabetupeln konsistent über verschiedene Funktionen und Vorgänge zu.

  *Beispiele:*
  - Wenn zwei-oder-Funktionen oder-Vorgänge in Erwägung gezogen werden, die jeweils einen Drehwinkel und ein Ziel-Qubit als Eingaben übernehmen, müssen Sie sicherstellen, dass Sie in jedem eingabetupel gleich Das heißt, `ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl` Sie bevorzugen und `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` in `ApplyRotation(target : Qubit, angle : Double) : Unit is Adj + Ctl` und `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` .

**Schlüssel** Prinzipal: Entwerfen Sie Funktionen und Vorgänge, um gut mit Q- \# sprach Features wie z. b. Teilanwendungen zu arbeiten.

- ✅Ordnen **Sie** Elemente in Eingabe Tupeln so an, dass die am häufigsten angewendeten Eingaben zuerst auftreten (d.h., dass die partielle Anwendung ähnlich verhält).

  *Beispiele:*
  - Ein Vorgang `ApplyRotation` , der eine Gleit Komma Zahl und ein Qubit als Eingaben annimmt, kann häufig teilweise mit der Gleit Komma Eingabe für die Verwendung mit Vorgängen verwendet werden, die eine Eingabe des Typs erwarten `Qubit => Unit` . Folglich eine Signatur von`operation ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl`
      funktioniert mit partieller Anwendung am weitesten gehend.
  - In der Regel bedeutet diese Anleitung, dass alle klassischen Daten vor allen Qubits in den eingabetupeln platziert werden, aber ein gutes Urteil verwendet und überprüft wird, wie Ihre API in der Praxis aufgerufen wird

## <a name="user-defined-types"></a>Benutzerdefinierte Typen

**Schlüsselprinzip:** verwenden Sie benutzerdefinierte Typen, um APIs ausdrucksvoller und benutzerfreundlicher zu gestalten.

- ✅Führen **Sie** neue benutzerdefinierte Typen ein, um hilfreiche Kurzform für lange und/oder komplizierte Typen bereitzustellen.

  *Beispiele:*
  - In Fällen, in denen ein Vorgangstyp mit drei Qubit-Array Eingaben häufig als Eingabe verwendet oder als Ausgabe zurückgegeben wird, stellt ein UDT wie z. b.`newtype TimeDependentBlockEncoding = ((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl)`
      kann hilfreich sein, um eine hilfreiche Kurzweile bereitzustellen.

- ✅Führen **Sie** neue benutzerdefinierte Typen ein, um anzugeben, dass ein angegebener Basistyp nur in einem speziellen Sinn verwendet werden sollte.

  *Beispiele:*
  - Ein Vorgang, der speziell als ein Vorgang interpretiert werden sollte, der klassische Daten in ein Quantum-Register codiert, eignet sich möglicherweise für die Bezeichnung mit einem benutzerdefinierten Typ `newtype InputEncoder = (Apply : (Qubit[] => Unit))` .

- ✅Führen **Sie** neue benutzerdefinierte Typen mit benannten Elementen ein, die zukünftige Erweiterbarkeit ermöglichen (z. b. eine Ergebnis Struktur, die in der Zukunft möglicherweise weitere benannte Elemente enthält).

  *Beispiele:*
  - Wenn ein Vorgang `TrainModel` eine große Anzahl von Konfigurationsoptionen verfügbar macht, ermöglicht das verfügbar machen dieser Optionen als neuer `TrainingOptions` UDT und Bereitstellen einer neuen Funktion das `DefaultTrainingOptions : Unit -> TrainingOptions` überschreiben spezifischer benannter Elemente in trainingoptions-UDT-Werten, wobei Bibliotheks Entwickler weiterhin neue UDT-Elemente hinzufügen können.

- ✅Deklarieren **Sie** benannte Elemente für neue benutzerdefinierte Typen entsprechend, dass die Benutzer die richtige tupelentkonstruktion kennen müssen.

  *Beispiele:*
  - Wenn eine komplexe Zahl in der Polar Zerlegung repräsentiert, bevorzugen `newtype ComplexPolar = (Magnitude: Double, Argument: Double)` Sie `newtype ComplexPolar = (Double, Double)` .

**Schlüssel** Prinzipal: Verwenden Sie benutzerdefinierte Typen, um die Cognitive Load zu verringern, und für die keine weiteren Konzepte und Nomenklatur benötigt werden.

- ⛔️ führen **keine** benutzerdefinierten Typen ein, die erfordern, dass der Benutzer häufig den Unwrap-Operator ( `!` ) verwendet oder häufig mehrere Ebenen der entpackt werden müssen. Mögliche Entschärfungs Strategien sind:

  - Wenn Sie einen benutzerdefinierten Typ mit einem einzelnen Element verfügbar machen, sollten Sie einen Namen für dieses Element definieren. Nehmen Sie zum Beispiel `newtype Encoder = (Apply : (Qubit[] => Unit is Adj + Ctl))` an `newtype Encoder = (Qubit[] => Unit is Adj + Ctl)` .

  - Sicherstellen, dass andere Funktionen und Vorgänge "umschließende" UDT-Instanzen direkt akzeptieren können.

- ⛔️ führen **keine** neuen benutzerdefinierten Typen ein, die integrierte Typen duplizieren, ohne zusätzliche Ausdruckskraft zu bieten.

  *Beispiele:*
  - Ein UDT `newtype QubitRegister = Qubit[]` stellt keine weitere Ausdruckskraft dar `Qubit[]` und ist daher schwieriger zu verwenden, ohne dass ein Unterscheidung möglich ist.
  - Ein UDT `newtype LittleEndian = Qubit[]` dokumentiert die Art und Weise, wie das zugrunde liegende Register verwendet und interpretiert werden soll, und bietet somit zusätzliche Ausdruckskraft für den Basistyp.

- ⛔️ **keine** Accessorfunktionen einführen, wenn dies nicht unbedingt erforderlich ist.   benannte Elemente werden in diesem Fall stark bevorzugt.

  *Beispiele:*
  - Wenn Sie einen UDT einführen `newtype Complex = (Double, Double)` , empfiehlt es sich, die Definition in zu ändern, `newtype Complex = (Real : Double, Imag : Double)` um Funktionen `GetReal : Complex -> Double` und einzuführen `GetImag : Complex -> Double` .

## <a name="namespaces-and-organization"></a>Namespaces und Organisation

**Schlüssel** Prinzipal: Wählen Sie Namespace Namen aus, die vorhersagbar sind und den Zweck von Funktionen, Vorgängen und benutzerdefinierten Typen in jedem Namespace eindeutig übermitteln.

- ✅Nennen **Sie** Namespaces als `Publisher.Product.DomainArea` .

  *Beispiele:*
  - Funktionen, Vorgänge und UDTs, die von Microsoft als Teil der Funktion für die Quantum-Simulation des quantumentwicklungskit veröffentlicht werden, werden im- `Microsoft.Quantum.Simulation` Namespace platziert.
  - `Microsoft.Quantum.Math`stellt einen Namespace dar, der von Microsoft als Teil des quantumentwicklungskit in Bezug auf den Domänen Bereich Mathematik veröffentlicht wurde.

- ✅Platzieren **Sie** Vorgänge, Funktionen und benutzerdefinierte Typen, die für bestimmte Funktionen verwendet werden, in einen Namespace, der diese Funktionalität beschreibt, auch wenn diese Funktionalität in verschiedenen Problem Domänen verwendet wird.

  *Beispiele:*
  - Die von Microsoft als Teil des quantumentwicklungskit veröffentlichten APIs zur Zustands Vorbereitung werden in platziert `Microsoft.Quantum.Preparation` .
  - Die von Microsoft als Teil des quantumentwicklungskit veröffentlichten Quantum-Simulations-APIs werden in platziert `Microsoft.Quantum.Simulation` .

- ✅Platzieren **Sie** Vorgänge, Funktionen und benutzerdefinierte Typen, die nur in bestimmten Domänen verwendet werden, in Namespaces, die Ihre Domäne des Hilfsprogramms angeben. Verwenden Sie bei Bedarf Subnamespaces, um fokussierte Aufgaben in jedem domänenspezifischen Namespace anzugeben.

  *Beispiele:*
  - Die von Microsoft veröffentlichte Quantum Machine Learning-Bibliothek wird größtenteils in den- @"microsoft.quantum.machinelearning" Namespace eingefügt, aber Beispiel Datasets werden vom- @"microsoft.quantum.machinelearning.datasets" Namespace bereitgestellt.
  - Die von Microsoft als Teil des quantumentwicklungskit veröffentlichten Quantum-Chemie-APIs sollten in platziert werden `Microsoft.Quantum.Chemistry` . Die Funktionalität, die für die Implementierung der Jordanien-Wigner-Zerlegung spezifisch ist, kann in platziert werden `Microsoft.Quantum.Chemistry.JordanWigner` , sodass die primäre Schnittstelle für den Domänen Bereich der Quantum-Chemie nicht mit Implementierungen beschäftigt ist.

**Schlüsselprinzip:** Verwenden Sie Namespaces und Zugriffsmodifizierer, um die API-Oberfläche zu verwenden, die Benutzern zur Verfügung gestellt wird, und um interne Details im Zusammenhang mit Implementierung und Tests ihrer APIs auszublenden

- ✅Wenn sinnvoll, **sollten** Sie alle Funktionen und Vorgänge, die erforderlich sind, um eine API zu implementieren, im gleichen Namespace wie die implementierte API platzieren. Sie sind jedoch mit den Schlüsselwörtern "private" oder "Internal" gekennzeichnet, um anzugeben, dass Sie nicht Teil der öffentlichen API-Oberfläche für eine Bibliothek sind. Verwenden Sie einen Namen, der mit einem Unterstrich ( `_` ) beginnt, um private und interne Vorgänge und Funktionen visuell von öffentlichen callables zu unterscheiden.

  *Beispiele:*
  - Der Vorgangs Name `_Features` gibt eine Funktion an, die für einen bestimmten Namespace und eine Assembly privat ist, und muss entweder mit dem- `internal` Schlüsselwort verknüpft werden.

- ✅In dem seltenen Fall, dass ein umfangreicher Satz privater Funktionen oder Vorgänge erforderlich ist, um die API für einen bestimmten Namespace zu **implementieren, platzieren** Sie diese in einem neuen Namespace, der dem Namespace entspricht, der implementiert wird und in dem Sie endet `.Private` .

- ✅Platzieren Sie alle Komponententests in Namespaces, die mit dem zu testenden Namespace überein **Stimmen** und mit enden `.Tests` .

## <a name="naming-conventions-and-vocabulary"></a>Benennungs Konventionen und Vokabulare

**Schlüsselprinzip:** Wählen Sie Namen und Terminologie aus, die für eine Vielzahl von Zielgruppen klar, zugänglich und lesbar sind, einschließlich der Quantum-Einsteiger und-Experten.

- ⛔️ **weder** diskriminierte noch exklusive Bezeichnernamen oder Terminologie in API-Dokumentations Kommentaren verwenden.

- ✅Verwenden **Sie** API-Dokumentations Kommentare zum Bereitstellen von relevantem Kontext, Beispielen und verweisen, insbesondere für schwierigere Konzepte.

- ⛔️ **keine** Namen von Bezeichnern verwenden, die unnötig esoterisch sind oder für die ein signifikantes Wissen der Quantum-Algorithmen erforderlich ist.

  *Beispiele:*
  - "Amplitude-Verstärkungs Iterationen" zu "Grover-Iterationen" bevorzugen.

- ✅**Wählen Sie** Vorgänge und Funktionsnamen aus, die die beabsichtigte Auswirkung einer Aufruf baren und nicht deren Implementierung eindeutig vermitteln. Beachten Sie, dass die Implementierung in [API-Dokumentations Kommentaren](xref:microsoft.quantum.guide.filestructure#documentation-comments)und dokumentiert werden kann.

  *Beispiele:*
  - "Schätzung überlappen" mit "Hadamard Test" bevorzugen, da letztere kommuniziert, wie die erste implementiert ist.

- ✅Verwenden **Sie** Wörter auf konsistente Weise für alle Q- \# APIs:

  - **Verbund**

    - **Assert**: Überprüfen Sie, ob eine Annahme über den Status eines Ziel Computers und seiner Qubits (möglicherweise durch Verwendung nicht physischer Ressourcen) gilt. Vorgänge mit diesem Verb sollten immer sicher entfernt werden, ohne dass sich dies auf die Funktionalität von Bibliotheken und ausführbaren Programmen auswirkt. Beachten Sie, dass im Gegensatz zu Fakten Assertionen im Allgemeinen vom externen Zustand abhängig sind, wie z. b. der Status eines Qubit-Registers, der Ausführungsumgebung oder so weiter. Da die Abhängigkeit von externem Status eine Art von Nebeneffekt ist, müssen Assertionen als Vorgänge und nicht als Funktionen verfügbar gemacht werden.

    - **Schätzung**: bei Verwendung eines oder mehrerer möglicherweise wiederholter Messungen wird eine klassische Menge von Messergebnissen geschätzt.

      *Beispiele:*
      - @"microsoft.quantum.characterization.estimatefrequency"
      - @"microsoft.quantum.characterization.estimateoverlapbetweenstates"

    - **Prepare**: wenden Sie einen Quantum-Vorgang oder eine Sequenz von Vorgängen auf ein oder mehrere Qubits an, die in einem bestimmten Anfangszustand (in der Regel $ \ket{00\cdots 0} $) gestartet werden, sodass der Status dieser Qubits in den gewünschten Endzustand weiterentwickelt wird. Im allgemeinen **kann** das agieren in anderen Zuständen als dem angegebenen Startstatus zu einer nicht definierten einheitlichen Transformation führen, **sollte** aber trotzdem einen Vorgang und seinen Adjoint "Abbrechen" und einen No-op-Vorgang anwenden.

      *Beispiele:*
      - @"microsoft.quantum.preparation.preparearbitrarystate"
      - @"microsoft.quantum.preparation.prepareuniformsuperposition"

    - **Measure**: wenden Sie einen Quantum-Vorgang oder eine Sequenz von Vorgängen auf ein oder mehrere Qubits an, und lesen Sie die klassischen Daten zurück.

      *Beispiele:*
      - @"microsoft.quantum.intrinsic.measure"
      - @"microsoft.quantum.arithmetic.measurefxp"
      - @"microsoft.quantum.arithmetic.measureinteger"

    - **Apply**: wenden Sie einen Quantum-Vorgang oder eine Sequenz von Vorgängen auf ein oder mehrere Qubits an, sodass sich der Status dieser Qubits in kohärenter Weise ändert. Dieses Verb ist das allgemeinste Verb in der Q \# -Nomenklatur und **sollte nicht verwendet werden** , wenn ein spezifischere Verb eher direkt relevant ist.

  - **Nomen**:

    - **Fakt**: eine boolesche Bedingung, die nur von Ihren Eingaben abhängt, nicht vom Status eines Ziel Computers, der Umgebung oder des Zustands der Qubits des Computers. Im Gegensatz zu einer-Assertion ist ein Fakt nur für die *Werte* , die für diese Tatsache bereitgestellt werden, empfindlich. Beispiel:

      *Beispiele:*
      - @"microsoft.quantum.diagnostics.equalityfacti": stellt einen Gleichheits Fakt über zwei ganzzahlige Eingaben dar. entweder sind die als Eingabe bereitgestellten Ganzzahlen gleich zueinander, oder Sie sind nicht unabhängig von einem anderen Programmzustand.

    - **Optionen:** Ein UDT, der mehrere benannte Elemente enthält, die als "optionale Argumente" für eine Funktion oder einen Vorgang fungieren können. Beispiel:

      *Beispiele:*
      - Der @"microsoft.quantum.machinelearning.trainingoptions" UDT umfasst benannte Elemente für Lernrate, Mini Batch-Größe und andere konfigurierbare Parameter für ml-Schulungen.

  - **Adjektive**:

    - ⛔️ **New**: dieses Adjektiv **sollte nicht** verwendet werden, um Verwirrung mit der Verwendung als Verb in vielen Programmiersprachen zu vermeiden (z. b. C++, c#, Java, typescript, PowerShell).

  - **Präpositionen:** In einigen Fällen können Präpositionen verwendet werden, um die Rollen von Substantiven und Verben in Funktions-und Vorgangs Namen genauer zu unterscheiden oder zu verdeutlichen. Es sollte jedoch sorgfältig und konsistent vorgegangen werden.

    - **Wie folgt:** Stellt dar, dass die Eingabe und Ausgabe einer Funktion die gleichen Informationen darstellen, dass die Ausgabe diese Informationen jedoch nicht in ihrer ursprünglichen Darstellung, sondern **als** *X* darstellt. Dies gilt insbesondere für Typkonvertierungs Funktionen.

      *Beispiele:*
      - `IntAsDouble(2)`Gibt an, dass sowohl die Eingabe ( `2` ) als auch die Ausgabe ( `2.0` ) die gleichen Informationen qualitativ darstellen, wobei jedoch unterschiedliche Q- \# Datentypen verwendet werden.

    - **Von:** Um die Konsistenz zu gewährleisten, **sollte** diese Vorposition nicht verwendet werden, um Typkonvertierungs Funktionen anzugeben, oder andere Fälle **, in denen dies zutrifft** .

    - ⛔️ **:** diese Vorposition **sollte nicht** verwendet werden, um Verwirrung mit der Verwendung als Verb in vielen Programmiersprachen zu vermeiden.
