---
title: Grundlegendes zu Quantencomputing
description: Hier erfahren Sie, was Quantencomputer sind und wie sie sich die Prinzipien der Quantenmechanik zunutze machen.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.understanding
ms.openlocfilehash: 65fa85a80021124444fd352f9492d03cbefcb859
ms.sourcegitcommit: a03d79ca3f0774161a9f86a15528d36e1291acce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83433009"
---
# <a name="understanding-quantum-computing"></a>Grundlegendes zu Quantencomputing

Beim Quantencomputing werden die Prinzipien der Quantenmechanik genutzt, um Informationen zu verarbeiten. Daher muss beim Quantencomputing ein anderer Ansatz verfolgt werden als beim klassischen Computing.  Ein Beispiel für diesen Unterschied ist der Prozessor, der in Quantencomputern zum Einsatz kommt.  Bei klassischen Computern werden bekanntlich Silizium-basierte Chips verwendet. Quantencomputer nutzen dagegen Quantenmaterialien wie Atome, Ionen, Photonen oder Elektronen.  

Für das Verhalten des Quantenmaterials gelten die Gesetze der Quantenmechanik. Dabei werden Konzepte wie probabilistische Berechnung, Superposition und Verschränkung genutzt. Diese Konzepte bilden die Grundlage für Quantenalgorithmen, die sich die Leistungsfähigkeit des Quantencomputings zunutze machen, um komplexe Probleme zu lösen. In diesem Artikel werden einige der grundlegenden Konzepte der Quantenmechanik beschrieben, auf denen das Quantencomputing basiert.

## <a name="a-birds-eye-view-of-quantum-mechanics"></a>Allgemeiner Überblick über Quantenmechanik

Quantenmechanik wird auch als Quantentheorie bezeichnet und ist ein Teilbereich der Physik, der sich mit Teilchen auf atomarer und subatomarer Ebene beschäftigt. Auf der Quantenebene gelten jedoch viele der als selbstverständlich betrachteten Gesetze der Mechanik nicht. Superposition, Quantenmessung und Verschränkung sind drei Phänomene, die für das Quantencomputing von zentraler Bedeutung sind.  

### <a name="superposition-vs-binary-computing"></a>Gegenüberstellung von Superposition und binärem Computing

Stellen Sie sich vor, Sie machen Gymnastikübungen in Ihrem Wohnzimmer. Dabei drehen Sie sich erst ganz nach links und anschließend ganz nach rechts. Wenn Sie allerdings versuchen, sich gleichzeitig nach links und nach rechts zu drehen, werden Sie feststellen, dass das nicht geht (zumindest nicht, ohne sich aufzuspalten).  Natürlich können Sie sich nicht gleichzeitig in beiden Zuständen befinden und sich zugleich nach links und nach rechts drehen.

Als Quantenteilchen wären Sie dagegen mit einer bestimmten Wahrscheinlichkeit nach *links* UND mit einer bestimmten Wahrscheinlichkeit nach *rechts* gedreht. Möglich wird dies durch ein Phänomen namens **Superposition** (auch **Kohärenz** genannt).

Ein Quantenteilchen (etwa ein Elektron) hat seine eigenen Eigenschaften für „nach links oder nach rechts gedreht“. Ein Beispiel wäre **Spin** (nach oben oder unten), was in Anlehnung an das klassische binäre Computing aber auch einfach als 1 oder 0 bezeichnet werden kann. Wenn sich ein Quantenteilchen in einem Superpositionszustand befindet, handelt es sich dabei um eine lineare Kombination aus einer unendlichen Anzahl von Zuständen zwischen 1 und 0. Bis zur tatsächlichen Betrachtung des Zustands wissen Sie jedoch nicht, welcher das sein wird. Das bringt uns zum nächsten Phänomen: der **Quantenmessung**.

### <a name="quantum-measurement"></a>Quantenmessung

Nehmen wir nun an, ein Freund schaut bei Ihnen vorbei und möchte Sie bei Ihren Gymnastikübungen fotografieren. Dabei entsteht höchstwahrscheinlich ein unscharfes Bild, das Sie mitten in der Drehbewegung zwischen ganz links und ganz rechts zeigt.

Wenn Sie allerdings ein Quantenteilchen wären, würde etwas Interessantes passieren: Sie wären auf der Aufnahme nie in einer Zwischenposition zu sehen, sondern immer entweder ganz nach links oder ganz nach rechts gedreht, und zwar unabhängig davon, in welcher Position Sie sich zum Zeitpunkt der Aufnahme befunden haben.

Das liegt daran, dass die Betrachtung oder Messung eines Quantenteilchens den **Kollaps** des Superpositionszustands (auch **Dekohärenz** genannt) zur Folge hat, woraufhin das Teilchen einen klassischen binären Zustand (1 oder 0) einnimmt.

Dieser binäre Zustand ist hilfreich, da Einsen und Nullen beim Computing auf vielfältige Weise genutzt werden können. Nachdem ein Quantenteilchen gemessen und seine Superpositionseigenschaften verloren hat, bleibt es dauerhaft in diesem Zustand (genau wie Ihr Bild) und ist immer 1 oder 0. Es gibt beim Quantencomputing allerdings auch die Möglichkeit, ein Teilchen wieder in einen Superpositionszustand zu versetzen, um es erneut für Quantenberechnungen verwenden zu können. Dazu aber später mehr.

### <a name="entanglement"></a>Verschränkung

Das vielleicht interessanteste Phänomen der Quantenmechanik ist die Möglichkeit der **Verschränkung** mehrerer Quantenteilchen. Verschränkte Teilchen bilden ein einzelnes System, sodass der Quantenzustand eines einzelnen Teilchens nicht unabhängig vom Quantenzustand der anderen Teilchen beschrieben werden kann. Das bedeutet, dass jeder Vorgang oder Prozess für ein einzelnes Teilchen auch mit den anderen Teilchen zusammenhängt.

Zusätzlich zu der gegenseitigen Abhängigkeit können Teilchen diese Verbindung auch dann aufrechterhalten, wenn sie unglaublich weit voneinander entfernt sind. Das können sogar mehrere Lichtjahre sein. Die Auswirkungen der Quantenmessung gelten auch für verschränkte Teilchen. Wenn also eines der Teilchen gemessen wird und seine Superpositionseigenschaften verliert, verliert auch das andere Teilchen seine Superpositionseigenschaften. Aufgrund der Korrelation zwischen den verschränkten Qubits liefert die Messung des Zustands eines Qubits Informationen zum Zustand des anderen Qubits, was beim Quantencomputing äußerst hilfreich ist.

### <a name="qubits-and-probability"></a>Qubits und Wahrscheinlichkeit

Bei klassischen Computern werden Informationen in Bits gespeichert und verarbeitet. Bits können entweder den Zustand 1 oder den Zustand 0 haben, aber niemals beide. Das Äquivalent beim Quantencomputing ist das **Qubit**. Dieses stellt den Zustand eines Quantenteilchens dar. Dank Superposition können Qubits entweder 1 oder 0 oder alles dazwischen sein. Abhängig von der Konfiguration des Qubits kollabiert es mit einer gewissen *Wahrscheinlichkeit* zu 1 oder zu 0. Die Wahrscheinlichkeit, dass das Qubit nach dem Kollaps den einen oder den anderen Zustand aufweist, wird durch die **Quanteninterferenz** bestimmt. 

Erinnern Sie sich noch an Ihren Freund, der Sie fotografiert hat? Angenommen, dessen Kamera verfügt über spezielle *Interferenzfilter*. Wenn er bei seinen Aufnahmen den *70/30*-Filter verwendet, sind Sie auf 70 Prozent der Bilder nach links und auf 30 Prozent der Bilder nach rechts gedreht. Der Filter hat den regulären Zustand der Kamera beeinflusst, um die Wahrscheinlichkeit des Verhaltens zu beeinflussen.

Die Quanteninterferenz wirkt sich auf ähnliche Weise auf den Zustand eines Qubits aus, um die Wahrscheinlichkeit eines bestimmten Ergebnisses bei der Messung zu beeinflussen. Genau dieser probabilistische Zustand macht Quantencomputing so leistungsstark.

Ein Beispiel: Angenommen, Sie verfügen über zwei Bits in einem klassischen Computer. Jedes Bit kann entweder 1 oder 0 speichern. Somit ergeben sich vier mögliche Werte (**00**, **01**, **10** und **11**), von denen aber immer nur einer gespeichert werden kann. Mit zwei Qubits in Superposition kann jedes Qubit dagegen 1 oder 0 oder *beides* sein, wodurch sich die gleichen vier Werte gleichzeitig darstellen lassen. Mit drei Qubits lassen sich acht Werte darstellen, mit vier Qubits 16 Werte und so weiter.

## <a name="summary"></a>Zusammenfassung

Diese Konzepte kratzen zwar lediglich an der Oberfläche der Quantenmechanik, sind im Zusammenhang mit Quantencomputing aber immens wichtig.

- **Superposition:** Die Fähigkeit von Quantenteilchen, eine Kombination aller möglichen Zustände zu sein.
- **Quantenmessung:** Die Betrachtung eines Quantenteilchens in Superposition, was zu einem der möglichen Zustände führt.
- **Verschränkung:** Die Fähigkeit von Quantenteilchen, ihre Messergebnisse miteinander zu korrelieren.
- **Qubit:** Die Grundeinheit von Informationen beim Quantencomputing. Ein Qubit stellt ein Quantenteilchen in Superposition aller möglichen Zustände dar.
- **Interferenz:** Intrinsisches Verhalten eines Qubits aufgrund von Superposition, um die Wahrscheinlichkeit eines Ergebnisses beim Kollaps zu beeinflussen.

## <a name="next-steps"></a>Nächste Schritte

> [!div class="nextstepaction"]
> [Quantencomputer und -simulatoren](xref:microsoft.quantum.overview.simulators)
