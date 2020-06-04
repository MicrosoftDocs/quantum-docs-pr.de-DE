---
title: 'F #-Dateistruktur'
description: 'Beschreibt die Struktur und die Syntax einer Q #-Datei.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: b8c24dae6cc8d8f37ad4f1f74017c05cabe3a4b4
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327457"
---
# <a name="q-file-structure"></a>F #-Dateistruktur

Jeder Q #-Vorgang, jede Funktion und jeder benutzerdefinierte Typ wird in einem Namespace definiert.

Eine Q #-Datei besteht aus einer Sequenz von *Namespace Deklarationen*.
Jede Namespace Deklaration enthält Deklarationen für benutzerdefinierte Typen, Vorgänge und Funktionen.
Eine Namespace Deklaration kann beliebig viele Typen von Deklarationen und in beliebiger Reihenfolge enthalten.
Befolgen Sie diese Links, um weitere Informationen zum Deklarieren von [benutzerdefinierten Typen](xref:microsoft.quantum.guide.types#user-defined-types), [Vorgängen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)und [Funktionen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) innerhalb eines Namespace zu erhalten.

Der einzige Text, der außerhalb einer Namespace Deklaration angezeigt werden kann, sind Kommentare.
Insbesondere Dokumentations Kommentare (weitere Details finden Sie unten) für einen Namespace vor der Deklaration.

## <a name="namespace-declarations"></a>Namespacedeklarationen

Eine Q #-Datei hat normalerweise genau eine Namespace Deklaration, kann jedoch keine (und leer sein oder nur Kommentare enthalten) oder mehrere Namespaces enthalten.
Namespace Deklarationen dürfen nicht eingefügt werden.

Derselbe Namespace kann in mehreren Q #-Dateien deklariert werden, die zusammen kompiliert werden, solange keine Typen-, Vorgangs-oder Funktions Deklarationen mit demselben Namen vorhanden sind.
Es ist insbesondere ungültig, denselben Typ im gleichen Namespace in mehreren Dateien zu definieren, auch wenn die Deklarationen identisch sind.

Eine Namespace Deklaration besteht aus dem Schlüsselwort `namespace` , gefolgt vom Namen des Namespace, einer offenen geschweifter Klammer `{` , den im Namespace enthaltenen Deklarationen und einer schließenden geschweifter Klammer `}` .
Namespace Namen folgen dem .net-Muster einer Sequenz von mindestens einem zulässigen Symbol, das durch Zeiträume getrennt ist `.` .
Beispielsweise `MyQuantumStuff` sind und `Microsoft.Quantum.Intrinsic` gültige Namespace Namen.
Gemäß der Konvention werden die Symbole in einem Namespace Namen groß geschrieben, dies ist jedoch nicht erforderlich.

Verweise auf Typen oder Aufruf Bare Dateien, die in einer Datei weiter unten deklariert sind, werden ordnungsgemäß aufgelöst. Es ist nicht erforderlich, dass der Typ, der Vorgang oder die Funktionsdeklaration einem Verweis darauf vorangestellt wird.

## <a name="open-directives"></a>Open-Direktiven

Innerhalb eines Namespace Blocks kann die- `open` Direktive verwendet werden, um alle Typen und callables zu importieren, die in einem bestimmten Namespace deklariert sind, und auf diese mit dem nicht qualifizierten Namen zu verweisen.
Eine solche `open` Direktive besteht aus dem `open` Schlüsselwort, gefolgt vom zu öffnenden Namespace und einem abschließenden Semikolon.

> [!NOTE] 
> Alle- `open` Direktiven müssen vor allen- `function` ,-oder- `operation` `newtype` Deklarationen im-Namespace Block angezeigt werden.

Optional kann ein Kurzname für den geöffneten Namespace definiert werden, sodass alle Elemente aus diesem Namespace durch den definierten Kurznamen qualifiziert werden können (und müssen). Wenn z. b. die folgende Namespace Deklaration und Open-Direktiven angegeben sind,

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

Wenn ein von uns deklarierte Vorgang einen Vorgang `Op` aus verwendet `Microsoft.Quantum.Intrinsic` , wird er durch einfaches Verwenden von aufgerufen `Op` .
Wenn jedoch eine bestimmte Funktion `Fn` von aufgerufen `Microsoft.Quantum.Math` werden soll, muss Sie mit aufgerufen werden `Math.Fn` .

Die- `open` Direktive gilt für den gesamten Namespace Block in einer Datei.
Wenn wir also einen zusätzlichen Namespace in der gleichen Q #-Datei wie oben definieren würden `NS` , hätten alle im zweiten Namespace definierten Vorgänge/Funktionen/Typen keinen Zugriff auf etwas von `Microsoft.Quantum.Intrinsic` oder, `Microsoft.Quantum.Math` es sei denn, wir haben die Open-Direktiven darin wiederholt. 

Auf einen Typ oder Aufruf baren Wert, der in einem anderen Namespace definiert ist, der *nicht* im aktuellen Namespace geöffnet ist, muss mit seinem voll qualifizierten Namen darauf verwiesen werden.
Beispielsweise muss auf einen Vorgang `Op` mit dem Namen aus dem- `X.Y` Namespace durch seinen voll qualifizierten Namen verwiesen werden `X.Y.Op` , es sei denn, der `X.Y` Namespace wurde zuvor im aktuellen Block geöffnet. Wie bereits erwähnt, `X` ist es nicht möglich, auf den Vorgang als zu verweisen, auch wenn der Namespace geöffnet wurde `Y.Op` .
Wenn ein Kurzname `Z` für `X.Y` in diesem Namespace und in der Datei definiert wurde, `Op` muss als bezeichnet werden `Z.Op` . 

Es ist in der Regel besser, einen Namespace mit einer- `open` Direktive einzubeziehen.
Die Verwendung eines voll qualifizierten Namens ist erforderlich, wenn zwei Namespaces Konstrukte mit dem gleichen Namen definieren und die aktuelle Quelle Konstrukte aus beidem verwendet.

F # befolgt die gleichen Regeln für die Benennung wie andere .NET-Sprachen.
F # unterstützt jedoch keine relativen Verweise auf Namespaces.
Das heißt, wenn der Namespace `a.b` geöffnet wurde, wird ein Verweis auf einen Vorgang mit dem Namen `c.d` *nicht* in einen Vorgang mit dem vollständigen Namen aufgelöst `a.b.c.d` .

## <a name="formatting"></a>Formatierung

Die meisten Q #-Anweisungen und-Direktiven enden mit einem abschließenden Semikolon, `;` .
-Anweisungen und-Deklarationen, wie z. b. `for` und `operation` , die mit einem Anweisungsblock enden (siehe unten), erfordern kein abschließendes Semikolon
Jede Anweisungs Beschreibung gibt an, ob das abschließende Semikolon erforderlich ist.

Anweisungen, wie Ausdrücke, Deklarationen und Direktiven, werden möglicherweise über mehrere Zeilen hinweg aufgeteilt.
Das vorhanden sein mehrerer Anweisungen in einer einzelnen Zeile sollte vermieden werden.

## <a name="statement-blocks"></a>Anweisungsblöcke

Q #-Anweisungen werden in Anweisungsblöcke gruppiert.
Ein Anweisungsblock beginnt mit einem öffnenden `{` und endet mit einem schließenden `}` .

Ein Anweisungsblock, der lexikalisch in einem anderen-Block eingeschlossen ist, wird als Teil Block des enthaltenden Blocks angesehen; enthaltende-und-Unterblöcke werden auch als äußere und innere Blöcke bezeichnet.

## <a name="comments"></a>Kommentare

Kommentare beginnen mit zwei Schrägstrichen, `//` und werden bis zum Zeilenende fortgesetzt.
Ein Kommentar kann an beliebiger Stelle in einer f #-Quelldatei angezeigt werden.

## <a name="documentation-comments"></a>Dokumentationskommentare

Kommentare, die mit drei Schrägstrichen beginnen, `///` werden vom Compiler speziell behandelt, wenn Sie unmittelbar vor einem Namespace, einem Vorgang, einer Spezialisierung, einer Funktion oder einer Typdefinition erscheinen.
In diesem Fall wird der Inhalt als Dokumentation für den definierten Aufruf baren oder benutzerdefinierten Typ, wie für andere .NET-Sprachen, übernommen.

Innerhalb von `///` Kommentaren wird Text, der als Teil der API-Dokumentation angezeigt wird, als [markdown](https://daringfireball.net/projects/markdown/syntax)formatiert, wobei verschiedene Teile der Dokumentation durch speziell benannte Header angezeigt werden.
Als Erweiterung von markdown können Querverweise auf Vorgänge, Funktionen und benutzerdefinierte Typen in Q # mithilfe von eingeschlossen werden `@"<ref target>"` `<ref target>` . dabei wird durch den voll qualifizierten Namen des Code Objekts ersetzt, auf das verwiesen wird.
Optional kann eine Dokumentations-Engine auch zusätzliche markdownerweiterungen unterstützen.

Beispiel:

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

Die folgenden Namen werden als Dokumentations Kommentar Header erkannt.

- **Zusammenfassung**: eine kurze Zusammenfassung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs. Der erste Absatz der Zusammenfassung wird für Hover-Informationen verwendet. Es sollte nur Text sein.
- **Beschreibung**: eine Beschreibung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs. Die Zusammenfassung und Beschreibung werden verkettet, um die generierte Dokumentations Datei für die Funktion, den Vorgang oder den Typ zu bilden.
  Die Beschreibung enthält möglicherweise in-line-Symbole und-Gleichungen in der Zeile.
- **Input**: eine Beschreibung des eingabetupels für einen Vorgang oder eine Funktion.
  Kann zusätzliche markdown-Unterabschnitte enthalten, die jedes einzelne Element des eingabetupels angeben.
- **Output**: eine Beschreibung des Tupels, das von einem Vorgang oder einer Funktion zurückgegeben wird.
- **Typparameter**: ein leerer Abschnitt, der einen zusätzlichen unter Abschnitt für jeden generischen Typparameter enthält.
- **Beispiel**: ein kurzes Beispiel für den Vorgang, die Funktion oder den Typ, der verwendet wird.
- **Hinweise**: verschiedene Prosa, die einen Aspekt des Vorgangs, der Funktion oder des Typs beschreibt.
- **Siehe auch**: eine Liste der voll qualifizierten Namen, die verwandte Funktionen, Vorgänge oder benutzerdefinierte Typen angeben.
- **Verweise**: eine Liste von verweisen und citationen für das Element, das dokumentiert wird.

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu [Vorgängen und Funktionen](xref:microsoft.quantum.guide.operationsfunctions) in f #.