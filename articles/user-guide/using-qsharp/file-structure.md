---
title: Q# Dateistruktur
description: Beschreibt die Struktur und die Syntax einer Q# Datei.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
no-loc:
- Q#
- $$v
ms.openlocfilehash: 98b3a2e35186989b8191cc566a5d5310bc26eafc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833313"
---
# <a name="no-locq-file-structure"></a>Q# Dateistruktur

Eine Q# Datei besteht aus einer Sequenz von *Namespace Deklarationen*.
Jede Namespace Deklaration enthält Deklarationen für benutzerdefinierte Typen, Vorgänge und Funktionen und kann jede beliebige Anzahl von Deklarationen und in beliebiger Reihenfolge enthalten.
Weitere Informationen zu Deklarationen in einem Namespace finden Sie unter [benutzerdefinierte Typen](xref:microsoft.quantum.guide.types#user-defined-types), [Vorgänge](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)und [Funktionen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).

Der einzige Text, der außerhalb einer Namespace Deklaration angezeigt werden kann, sind Kommentare.
Insbesondere Dokumentations Kommentare für einen Namespace vor der Deklaration. Weitere Informationen finden Sie in den [Dokumentations Kommentaren](#documentation-comments) in diesem Artikel. 

## <a name="namespace-declarations"></a>Namespacedeklarationen

Eine Q# Datei verfügt in der Regel nur über eine Namespace Deklaration, kann jedoch keine (und leer sein oder nur Kommentare enthalten) oder mehrere Namespaces enthalten.
Namespace Deklarationen können nicht eingefügt werden.

Sie können denselben Namespace in mehreren Dateien deklarieren, die Q# zusammen kompiliert werden, solange keine Typen-, Vorgangs-oder Funktions Deklarationen mit demselben Namen vorhanden sind.
Es ist insbesondere ungültig, denselben Typ im gleichen Namespace in mehreren Dateien zu definieren, auch wenn die Deklarationen identisch sind.

Eine Namespace Deklaration besteht aus dem Schlüsselwort `namespace` , gefolgt vom Namen des Namespace und den Deklarationen im Namespace, die in geschweifte Klammern eingeschlossen sind `{ }` .
Namespace Namen folgen dem .net-Muster einer Sequenz von mindestens einem zulässigen Symbol, das durch Zeiträume getrennt ist `.` .
Beispielsweise `MyQuantumStuff` sind und `Microsoft.Quantum.Intrinsic` gültige Namespace Namen.
Gemäß der Konvention werden die Symbole in einem Namespace Namen groß geschrieben, dies ist jedoch nicht erforderlich.

Verweise auf Typen oder Aufruf Bare Elemente, die weiter unten in einer Datei deklariert sind, werden ordnungsgemäß aufgelöst. Es ist nicht erforderlich, dass der Typ, der Vorgang oder die Funktionsdeklaration einem Verweis darauf vorangestellt wird.

## <a name="open-directives"></a>Open-Direktiven

Verwenden Sie in einem Namespace Block die- `open` Direktive, um alle Typen und callables zu importieren, die in einem bestimmten Namespace deklariert sind, und verweisen Sie anhand ihres nicht qualifizierten Namens darauf.
Eine solche `open` Direktive besteht aus dem `open` Schlüsselwort, gefolgt vom zu öffnenden Namespace und einem abschließenden Semikolon.

> [!NOTE] 
> Alle- `open` Direktiven müssen vor allen- `function` ,-oder- `operation` `newtype` Deklarationen im-Namespace Block angezeigt werden.

Optional können Sie einen Kurznamen für den geöffneten Namespace definieren. Wenn ein Kurzname definiert ist, müssen Sie alle Elemente aus diesem Namespace mit dem definierten Kurznamen qualifizieren. Wenn z. b. die folgende Namespace Deklaration und Open-Direktiven angegeben sind,

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

Wenn ein deklarierter Vorgang einen Vorgang `Op` aus verwendet `Microsoft.Quantum.Intrinsic` , wird er durch einfaches Verwenden von aufgerufen `Op` .
Um jedoch eine bestimmte Funktion `Fn` von aufzurufen `Microsoft.Quantum.Math` , müssen Sie Sie mithilfe von aufzurufen `Math.Fn` .

Die- `open` Direktive gilt für den gesamten Namespace Block in einer Datei.
Wenn Sie also einen zusätzlichen Namespace in derselben Q# Datei wie `NS` zuvor definieren, haben alle im zweiten Namespace definierten Vorgänge/Funktionen/Typen keinen Zugriff auf etwas von `Microsoft.Quantum.Intrinsic` oder, `Microsoft.Quantum.Math` es sei denn, Sie haben die Open-Direktiven darin wiederholt. 

Um auf einen Typ oder Aufruf baren Wert zu verweisen, der in einem anderen Namespace definiert ist, der *nicht* im aktuellen Namespace geöffnet ist, müssen Sie ihn mit seinem voll qualifizierten Namen referenzieren.
Angenommen, Sie verfügen über einen Vorgang mit `Op` dem Namen aus dem- `X.Y` Namespace:

* Sie müssen mit dem voll qualifizierten Namen referenzieren `X.Y.Op` , es sei denn, der `X.Y` Namespace wurde zuvor im aktuellen Block geöffnet. 
* Auch wenn der `X` Namespace geöffnet ist, ist es nicht möglich, auf den Vorgang als zu verweisen `Y.Op` .
* Wenn Sie den Kurznamen `Z` für `X.Y` in diesem Namespace und dieser Datei definiert haben, müssen Sie auf `Op` als verweisen `Z.Op` . 

Es ist in der Regel besser, einen Namespace mit einer- `open` Direktive einzubeziehen.
Die Verwendung eines voll qualifizierten Namens ist erforderlich, wenn zwei Namespaces Konstrukte mit dem gleichen Namen definieren und die aktuelle Quelle Konstrukte aus beidem verwendet.

Q# befolgt die gleichen Regeln für die Benennung wie andere .NET-Sprachen.
Q#Unterstützt jedoch keine relativen Verweise auf Namespaces.
Wenn der Namespace beispielsweise `a.b` geöffnet ist, wird ein Verweis auf einen Vorgang mit dem Namen `c.d` *nicht* in einen Vorgang mit dem vollständigen Namen aufgelöst `a.b.c.d` .

## <a name="formatting"></a>Formatierung

Die meisten Q# Anweisungen und Direktiven enden mit einem abschließenden Semikolon, `;` .
-Anweisungen und-Deklarationen, wie z. b. `for` und `operation` , die mit einem Anweisungsblock enden (siehe folgender Abschnitt), erfordern kein abschließendes Semikolon.
Jede Anweisungs Beschreibung gibt an, ob das abschließende Semikolon erforderlich ist.

Anweisungen, wie Ausdrücke, Deklarationen und Direktiven, können über mehrere Zeilen hinweg aufgeteilt werden.
Vermeiden Sie es, mehrere Anweisungen in einer einzelnen Zeile zu platzieren.

## <a name="statement-blocks"></a>Anweisungsblöcke

Q# -Anweisungen werden in Anweisungsblöcke gruppiert, die in geschweiften Klammern eingeschlossen sind `{ }` . Ein Anweisungsblock beginnt mit einem öffnenden `{` und endet mit einem schließenden `}` .

Ein Anweisungsblock, der lexikalisch in einem anderen-Block eingeschlossen ist, wird als Teil Block des enthaltenden Blocks angesehen; enthaltende-und-Unterblöcke werden auch als äußere und innere Blöcke bezeichnet.

## <a name="comments"></a>Kommentare

Kommentare beginnen mit zwei Schrägstrichen, `//` und werden bis zum Ende der Zeile fortgesetzt.
Ein Kommentar kann an beliebiger Stelle in einer Q# Quelldatei angezeigt werden.

## <a name="documentation-comments"></a>Dokumentationskommentare

Kommentare, die mit drei Schrägstrichen beginnen, `///` werden vom Compiler speziell behandelt, wenn Sie unmittelbar vor einem Namespace, einem Vorgang, einer Spezialisierung, einer Funktion oder einer Typdefinition erscheinen.
In diesem Fall behandelt der Compiler Sie als Dokumentation für den definierten Aufruf baren oder benutzerdefinierten Typ, der mit anderen .NET-Sprachen identisch ist.

Innerhalb von `///` Kommentaren wird Text, der als Teil der API-Dokumentation angezeigt wird, als [markdown](https://daringfireball.net/projects/markdown/syntax)formatiert, wobei verschiedene Teile der Dokumentation durch speziell benannte Header angezeigt werden.
Verwenden Sie in markdown die `@"<ref target>"` Erweiterung für Querverweise auf Vorgänge, Funktionen und benutzerdefinierte Typen in Q# . Ersetzen Sie dies `<ref target>` durch den voll qualifizierten Namen des Code Objekts, auf das verwiesen wird.
Unterschiedliche Dokumentations-Engines unterstützen möglicherweise zusätzliche markdownerweiterungen.

Zum Beispiel:

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

Die folgenden Namen sind als Dokumentations Kommentar Header gültig.

- **Zusammenfassung**: eine kurze Zusammenfassung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs. Der erste Absatz der Zusammenfassung wird für Hover-Informationen verwendet. Es sollte nur Text sein.
- **Beschreibung**: eine Beschreibung des Verhaltens einer Funktion oder eines Vorgangs oder der Zweck eines Typs. Zusammenfassung und Beschreibung bilden die generierte Dokumentations Datei für die Funktion, den Vorgang oder den Typ.
  Die Beschreibung unterstützt die in-line-Symbole und-Gleichungen, die in-line-
- **Input**: eine Beschreibung des eingabetupels für einen Vorgang oder eine Funktion.
  Kann zusätzliche markdown-Unterabschnitte enthalten, die jedes Element des eingabetupels angeben.
- **Output**: eine Beschreibung des Tupels, das von einem Vorgang oder einer Funktion zurückgegeben wird.
- **Typparameter**: ein leerer Abschnitt, der einen zusätzlichen unter Abschnitt für jeden generischen Typparameter enthält.
- **Beispiel**: ein kurzes Beispiel für den Vorgang, die Funktion oder den Typ, der verwendet wird.
- **Hinweise**: verschiedene Prosa, die einen Aspekt des Vorgangs, der Funktion oder des Typs beschreibt.
- **Siehe auch**: eine Liste der voll qualifizierten Namen, die verwandte Funktionen, Vorgänge oder benutzerdefinierte Typen angeben.
- **Verweise**: eine Liste von verweisen und citationen für das dokumentierte Element.

## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions) in Q# .