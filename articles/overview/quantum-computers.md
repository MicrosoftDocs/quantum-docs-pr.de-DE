---
title: Was können Quantencomputer?
description: Erfahren Sie mehr über die Macht von Quantencomputern, von neuartigen Quantenalgorithmen bis zu von Quanten inspirierten Algorithmen, die auf klassischen Computern ausgeführt werden.
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: article
uid: microsoft.quantum.overview.computers
ms.openlocfilehash: 9d8ba90a504f298f9465ebf564c43625a4d43168
ms.sourcegitcommit: edcf15044d7bdf4f8b21fb8f6af4bde475eb13a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2019
ms.locfileid: "73529950"
---
# <a name="what-can-a-quantum-computer-do"></a>Was kann ein Quantencomputer?

Was können wir mit einem Quantencomputer tun, das sich mit einem klassischen Computer nicht erledigen lässt?

Die Lösung einiger der schwierigsten Probleme der Welt, zu der aktuelle Computer Milliarden Jahre Rechenzeit benötigen, könnte von einem Quantencomputer in Tagen, Stunden oder sogar Minuten erledigt werden.

Quantencomputer werden es Forschern ermöglichen, neue Katalysatoren und Materialien zu entwickeln, Medikamente zu verbessern, den Fortschritt in der künstlichen Intelligenz zu beschleunigen und grundlegende Fragen zum Ursprung des Universums zu beantworten.

## <a name="quantum-simulation"></a>Quantensimulation

Die Nutzung von Quantenprogrammen zum Modellieren der eigentlichen Quantensysteme hat das Potenzial, zu umfassenden Erkenntnissen zu führen, die Innovationen in vielen Branchen nach sich ziehen können. Photosynthese, Supraleiter und komplexe Moleküle sind Beispiele für Quantensysteme, die mithilfe von Quantenprogrammen simuliert werden können.

Das Simulieren von mikroskopisch kleinen Systemen, die sich nach den Gesetzen der Quantenmechanik verhalten, bringt hohen Berechnungsaufwand mit sich. Wir müssen alle möglichen Zustände berücksichtigen, die sich überlagern können, und die Anzahl der Zustände wächst exponentiell mit der Größe des Systems. Auf einem Quantencomputer brauchen wir gar nicht alle Zustände des Systems zu modellieren. Stattdessen betten wir den Quantenzustand des Systems, das wir modellieren möchten, in die Qubits des Computers selbst ein, und führen die Simulation mit einer bestimmten Menge an Quantengattern aus. Anders ausgedrückt: Wir verwenden einen Quantencomputer, um ein Quantensystem zu simulieren.

Chemische Moleküle sind Quantensysteme und können daher auf diese Weise analysiert werden. Eine solche spezifische chemische Verbindung ist das Enzym _Nitrogenase_, das möglicherweise das Potenzial besitzt, Energieverbrauch und Treibhausgasemissionen aktueller Dünger zu reduzieren – vorausgesetzt, wir verstehen seine Eigenschaften besser.

## <a name="cryptography"></a>Kryptografie

Der vielleicht bekannteste Anwendungsbereich von Quantencomputern ist die Kryptografie. Peter Shor hat 1994 gezeigt, dass mit einem skalierbaren Quantencomputer alle gängigen Verschlüsselungsverfahren geknackt werden können.  Die klassische Kryptografie basiert auf der „Widerspenstigkeit“ von Vorgängen mit hohen Zahlen, z. B. der Faktorisierung großer Zahlen in zwei Primzahlen.

Quantencomputer machen diese Vorgänge theoretisch lenkbar (per Shor-Algorithmus). Zwar ist die Implementierung dieses Algorithmus beim aktuellen Maßstab von Quantenhardware physisch nicht möglich, er hat aber die Entwicklung quantenresistenter Algorithmen in Gang gebracht, um Datensicherheit zukunftssicher zu gestalten, einschließlich neuartiger Quantenalgorithmen für die Verschlüsselung und die Verteilung von Kryptografieschlüsseln.

Bei Microsoft verfügen wir über das weltweit führende Team im Bereich Post-Quantenkryptografie und -sicherheit, das an der Entwicklung von quantenresistenten Algorithmen arbeitet.

## <a name="optimization"></a>Optimierung

Bei der Optimierung geht es darum, eine umfangreiche Suche in einem hochdimensionalen Bereich zur Erzielung einer Lösung durchzuführen, mit der eine bestimmte Kostenfunktion minimiert wird.   Auf einem Quantencomputer können wir Optimierungsalgorithmen beschleunigen, um Lösungen zu finden, die auf andere Weise nicht möglich wären. Beispiele für Anwendungsbereiche sind Transport/Logistik, Gesundheitswesen, Diagnostik und Materialwissenschaft. Dies kann erhebliche Auswirkungen auf die Effizienz der Branche haben.

Die Optimierung per Quantencomputing ermöglicht uns Innovationen im Bereich Transport/Logistik, die mit den heutigen klassischen Systemen nicht möglich sind.

Per Optimierung des Datenverkehrsflusses können Staus reduziert werden.  Weitere Bereiche neben der Routenplanung sind die Gatezuweisung für den Luftverkehr, die Paketzustellung, die Auftragsplanung und mehr. Wenn in der Materialwirtschaft weitere Durchbrüche erzielt werden, entstehen neue Energieformen, Akkus mit höherer Kapazität und leichtere, besser haltbare Materialien.

## <a name="machine-learning"></a>Machine Learning

Ein großer Teil der numerischen Berechnungen auf klassischen Computern besteht im Lösen linearer Gleichungssysteme. Dies gilt insbesondere für maschinelles Lernen, bei dem der größte Teil des Rechenaufwands in die Berechnung der Umkehrung riesiger Matrizen fließt.

Glücklicherweise gibt es einen Quantenalgorithmus, der es uns ermöglicht, das System exponentiell schneller als mit einem klassischen Computer zu lösen. Dies ebnet den Weg für die hohe Beschleunigung bei jedem Problem, für das die Lösung linearer Gleichungssysteme erforderlich ist.

Lösungen von Problemen in diesen Bereichen sind hilfreich für die Energiekrise, den Klimawandel, die Nahrungsmittelknappheit und persönliche und präzise medizinische Diagnosen.

## <a name="quantum-inspired-computing"></a>Von Quanten inspiriertes Computing

Von Quanten inspirierte Algorithmen werden mit klassischer Software implementiert, verwenden aber Quantenprinzipien, um höhere Geschwindigkeit und Genauigkeit zu erreichen.

Von Quanten inspirierte Algorithmen werden in der medizinischen Forschung angewendet. Beispielsweise, um die Genauigkeit von MRI-Scans (Magnetic Resonance Imaging, Magnetresonanztomografie) zu erhöhen. Das von Quanten inspirierte Computing wird verwendet, um die Konfiguration der MRI-Computer zur Erkennung bestimmter Krankheiten zu optimieren.

## <a name="next-steps"></a>Nächste Schritte

* [Warum sollte ich Quantencomputing erlernen?](xref:microsoft.quantum.overview.why)
* [Einstieg in das Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)
