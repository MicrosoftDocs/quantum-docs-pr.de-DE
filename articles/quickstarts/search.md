---
title: 'Ausführen des Grover-Suchalgorithmus in Q#: Quantum Development Kit'
description: Erstellen eines Q#-Projekts, das den Grover-Algorithmus veranschaulicht, einen der kanonischen Quantenalgorithmen.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 0e64fcd56929fa33397c45bf1b2e99bf687eca6f
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906949"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>Schnellstart: Implementierung des Grover-Suchalgorithmus in Q#

In dieser Schnellstartanleitung erfahren Sie, wie Sie eine Grover-Suchabfrage erstellen und ausführen, um die Suche in unstrukturierten Daten zu beschleunigen.  Bei der Grover-Suche handelt es sich um einen der beliebtesten Quantencomputingalgorithmen. Diese relativ kleine Q#-Implementierung vermittelt Ihnen einen Eindruck davon, welche Vorteile die Programmierung von Quantenlösungen mit einer allgemeinen Q#-Quantenprogrammiersprache zum Ausdrücken von Quantenalgorithmen bietet.  Die Simulationsausgabe am Ende der Anleitung zeigt, dass die Suche nach einer bestimmten Zeichenfolge in einer Liste unsortierter Einträge nur einen Bruchteil der Zeit dauert, die für die Durchsuchung der gesamten Liste auf einem klassischen Computer benötigt würde.

Der Grover-Algorithmus durchsucht eine Liste unstrukturierter Daten nach bestimmten Elementen. Er kann beispielsweise diese Frage beantworten: Ist diese Karte, die aus einem Kartenstapel gezogen wurde, ein Herz As? Die Bezeichnung des spezifischen Elements wird als _markierte Eingabe_ bezeichnet.

Bei Verwendung des Grover-Suchalgorithmus besteht Sicherheit, dass ein Quantencomputer diese Suche in weniger Schritten ausführt als die Anzahl der Elemente in der durchsuchten Liste – das kann kein klassischer Algorithmus. Die höhere Geschwindigkeit ist im Fall des Kartenstapels vernachlässigbar. In Listen, die Millionen oder Milliarden Elemente enthalten, wird sie aber wichtig.

Sie können den Grover-Suchalgorithmus mit wenigen Codezeilen erstellen.

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit][install].

## <a name="what-does-grovers-search-algorithm-do"></a>Was macht der Grover-Suchalgorithmus?

Der Grover-Algorithmus fragt, ob ein Element in einer Liste dasjenige ist, nach dem wir suchen. Dazu erstellt er eine Quantenüberlagerung der Indizes der Liste mit jedem Koeffizienten (jeder Wahrscheinlichkeitsamplitude), wodurch die Wahrscheinlichkeit dargestellt wird, dass ein bestimmter Index der gesuchte ist.

Im Kern des Algorithmus befinden sich zwei Schritte, die den Koeffizienten des gesuchten Index inkrementell verstärken, bis die Wahrscheinlichkeitsamplitude des betreffenden Koeffizienten sich eins annähert.

Die Anzahl der inkrementellen Verstärkungen ist kleiner als die Anzahl der Elemente in der Liste. Das ist der Grund, warum der Grover-Suchalgorithmus die Suche in weniger Schritten als jeder klassische Algorithmus durchführen kann.

![Funktionsdiagramm des Grover-Suchalgorithmus](~/media/grover.png)

## <a name="write-the-code"></a>Schreiben des Codes

1. [Erstellen Sie ein neues Q#-Projekt](xref:microsoft.quantum.howto.createproject) mit dem Namen `Grover` unter Verwendung des Quantum Development Kit in der Entwicklungsumgebung Ihrer Wahl.

1. Fügen Sie den folgenden Code der `Operations.qs`-Datei in Ihrem neuen Projekt hinzu:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-40":::

1. Um die Liste zu definieren, die wir durchsuchen, erstellen Sie eine neue Datei `Reflections.qs`, und fügen Sie den folgenden Code ein:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    Die `ReflectAboutMarked`-Operation definiert die markierte Eingabe, nach der Sie suchen: die Zeichenfolge aus abwechselnden Nullen und Einsen. In diesem Beispiel wird die markierte Eingabe hartcodiert. Sie kann erweitert werden, um nach verschiedenen Eingaben zu suchen, oder generalisiert, um nach beliebigen Eingaben zu suchen.

1. Führen Sie als Nächstes Ihr neues Q#-Programm aus, um das von `ReflectAboutMarked` markierte Element zu finden.

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python mit Visual Studio Code oder Befehlszeile](#tab/tabid-python)

    Um Ihr neues Q#-Programm aus Python auszuführen, speichern Sie den folgenden Code als `host.py`:

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# mit Visual Studio Code oder Befehlszeile](#tab/tabid-csharp)

    Um Ihr neues Q#-Programm aus C# auszuführen, ändern Sie `Driver.cs`, so dass es den folgenden C#-Code beinhaltet:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# mit Visual Studio 2019](#tab/tabid-vs2019)

    Ändern Sie zum Ausführen Ihres neuen Q#-Programms aus C# in Visual Studio `Driver.cs`, sodass der folgende C#-Code enthalten ist:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Drücken Sie dann F5. Das Programm wird gestartet, und ein neues Fenster mit den folgenden Ergebnissen wird angezeigt: 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    Die `ReflectAboutMarked`-Operation wird nur viermal aufgerufen, Ihr Q#-Programm war aber imstande, die Eingabe "01010" unter $2^{5} = 32$ möglichen Eingaben zu finden!

## <a name="next-steps"></a>Nächste Schritte

Wenn Ihnen dieser Schnellstart gefallen hat, sehen Sie sich einige der unten aufgeführten Ressourcen an, um mehr darüber zu erfahren, wie Sie Q# verwenden können, um eigene Quantenanwendungen zu schreiben:

- [Zurück zum Leitfaden mit den ersten Schritte mit dem QDK](xref:microsoft.quantum.welcome)
- Ausprobieren eines [Beispiels](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) für einen allgemeineren Grover-Suchalgorithmus
- [Weitere Informationen zur Grover-Suche mit den Quanten-Katas](xref:microsoft.quantum.overview.katas)
- Informieren Sie sich ausführlicher über die [Amplitudenverstärkung](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), die Quantencomputingtechnik hinter dem Suchalgorithmus von Grover.
- [Quantencomputingkonzepte](xref:microsoft.quantum.concepts.intro)
- [Quantum Development Kit-Beispiele](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
