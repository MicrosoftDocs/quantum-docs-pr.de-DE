---
title: Was ist Quantencomputing?
description: Erfahren Sie, was Quantencomputing ist und was ein Quantencomputer kann.
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.what
ms.openlocfilehash: 2f3b64b00a0a9552e52e34cb1e3652810b266eab
ms.sourcegitcommit: edcf15044d7bdf4f8b21fb8f6af4bde475eb13a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2019
ms.locfileid: "73529930"
---
# <a name="what-is-quantum-computing"></a>Was ist Quantencomputing?

Es gibt einige Probleme, die so schwierig und so unglaublich gewaltig sind, dass ihre Lösung selbst bei Zusammenarbeit aller Supercomputer der Welt länger als die Lebensdauer des Universums dauern würde.

Quantencomputer bieten das Versprechen, einige der größten Herausforderungen unseres Planeten zu lösen – im Bereich Umweltschutz, Landwirtschaft, Gesundheitswesen, Energie, Klima, Materialwissenschaft und bei Problemen, die wir bisher nicht einmal kennen. Der Einfluss von Quantencomputern wird weitreichend sein, so groß wie die Schaffung des Transistors im Jahr 1947, die den Weg zur digitalen Ökonomie von heute ebnete.

Quantencomputer nutzen die einzigartigen Verhaltensweisen der Quantenphysik, um ein neues und leistungsstarkes Modell des Computings bereitzustellen. Die Theorie der Quantenphysik postuliert, dass Materie auf Quantenebene sich in einer Überlagerung mehrerer klassischer Zustände befinden kann. Und diese vielen Zustände überlagern einander wie Wellen in einem Gezeitenbecken.  Nach einer Messung stellt sich einer der klassischen Zustände ein. 

Daraufhin wird bei einer Wiederholung der gleichen Messung das gleiche klassische Ergebnis erreicht.  Eine Quantenverschränkung tritt auf, wenn Partikel so miteinander interagieren, dass sich der Quantenzustand der einzelnen Partikel nur in Abhängigkeit von den anderen Partikeln beschreiben lässt, selbst wenn die Partikel physisch weit voneinander entfernt sind.  

Quantencomputer speichern Informationen in Quantenzuständen von Materie und profitieren von Quanteneigenschaften wie Superposition und Verschränkung, um Quantenberechnungen auf der Grundlage dieser Informationen durchzuführen, wobei sie Quanteninterferenzen nutzen und lernen, sie zu programmieren.

Quantencomputing mag sich einschüchternd anhören, aber mit den richtigen Ressourcen können Sie noch heute anfangen, Quantenanwendungen zu erstellen.

## <a name="the-qubit"></a>Das Qubit

Quantencomputing definiert Computingkonzepte, die das Quantenverhalten widerspiegeln.  Am Anfang des Quantencomputings steht das Konzept eines Qubit.  Beim Quantencomputing bildet ein Quantenbit – **Qubit** – eine Quanteninformationseinheit, wie ein klassisches Bit. Klassische Bits enthalten einen einzelnen binären Wert (0 oder 1). Der Zustand eines Qubits kann dagegen eine **Superposition** sein (also 0 und 1 gleichzeitig).  

Die Messung eines Qubits verändert dessen Zustand. Nach der Messung geht das Qubit von einer Superposition in einen der klassischen Zustände über.  

Mehrere Qubits können außerdem **verschränkt** sein. Bei der Messung eines verschränkten Qubits wird unsere Kenntnis des Zustands der anderen Qubits ebenfalls aktualisiert.

## <a name="quantum-algorithms"></a>Quantenalgorithmen

Quantenalgorithmen nutzen Quanteneigenschaften und -verhaltensweisen, um klassische Algorithmen zu beschleunigen oder völlig neue Möglichkeiten für die Modellierung physischer Systeme zu bieten.  Diese Algorithmen nutzen die Art der Informationscodierung durch Qubits sowie die Möglichkeit zur parallelen Verwendung mehrerer verschränkter Qubits in Superposition.  

Bei klassischen Computern werden Informationen in Bits mit zwei möglichen Werten (0 oder 1) codiert.  Ein Qubit codiert zwei Werte gleichzeitig (0 und 1).  Zwei klassische Bits codieren einen von vier möglichen Werten: 00, 01, 10 oder 11. Zwei Qubits codieren dagegen gleichzeitig eine beliebige Superposition der vier Zustände. Bei einer Messung erhalten wir allerdings immer nur einen dieser Werte. Vier Qubits codieren gleichzeitig eine beliebige Superposition von 16 Werten. Dies setzt sich exponentiell so fort.  100 Qubits können mehr Informationen codieren, als heutzutage in den größten Computersystemen zur Verfügung stehen.  

Wenn mehrere verschränkte Qubits zudem kohärent agieren, können sie mehrere Optionen gleichzeitig verarbeiten. Verschränkte Qubits können Informationen in einem Bruchteil der Zeit verarbeiten, die selbst die schnellsten nicht quantengestützten Systeme benötigen würden.

Quantenalgorithmen werden bereits seit mehreren Jahrzehnten erforscht, um diese Quantenattribute nutzbar zu machen, und es wurden bereits zahlreiche innovative Techniken gefunden, um Aufgaben in einem Bruchteil der Zeit zu lösen, die bei Verwendung klassischer Methoden nötig wäre.  

Einer der berühmtesten Quantenalgorithmen ist der _Shor-Algorithmus_ zur Faktorisierung, der das klassisch sperrige Problem der Faktorisierung einer großen Zahl in zwei Primzahlen schnell genug macht, um eine Gefahr für die klassische Kryptografie zu bilden.

Auf der eher konstruktiven Seite werden durch Überlagerung, Quantenverschränkung und die Eigenschaft der **Nichtkopierbarkeit** von Qubits (womit die Unmöglichkeit des unentdeckten Kopierens von Qubits bezeichnet wird) Algorithmen für die Verteilung sicherer kryptografischer Schlüssel möglich.

Der _Grover-Algorithmus_ bietet eine Quantenalgorithmus-Technik, mit der sich beim Durchsuchen unstrukturierter Daten eine quadratische Beschleunigung erzielen lässt.

## <a name="quantum-hardware"></a>Quantenhardware

In klassischen Computern entsprechen Bits Spannungsniveaus in den Siliziumschaltkreisen. Die Hardware von Quantencomputern kann durch viele physikalische Umsetzungen von Qubits implementiert werden: Ionenfallen, Supraleitung, neutrale Atome, Elektronenspin, Lichtpolarisation, topologische Qubits. Quantenhardware ist eine aufstrebende Technologie. Qubits sind naturgemäß anfällig und verlieren bei der Interaktion mit ihrer Umgebung an Kohärenz. Daher muss ein ausgewogenes Verhältnis zwischen Systemgenauigkeit und Skalierbarkeit gefunden werden. Je größer der Maßstab (d.h. die Anzahl der Qubits), desto höher ist die Fehlerrate.

Microsoft entwickelt einen Quantencomputer auf der Grundlage topologischer Qubits. Wir glauben, dass ein topologisches Qubit weniger durch Änderungen in seiner Umgebung beeinflusst wird, was das Maß an externer Fehlerkorrektur verringert. Topologische Qubits zeichnen sich durch erhöhte Stabilität und Widerstandsfähigkeit gegenüber Umgebungsrauschen aus, was bedeutet, dass sie sich leichter skalieren lassen und länger zuverlässig bleiben.

## <a name="quantum-computing--a-full-hardware-and-software-stack"></a>Quantencomputing: ein vollständiger Hardware- und Softwarestapel

Das Quantenprogramm von Microsoft ist einzigartig, da wir uns auf die Skalierung jeder einzelnen Komponente des Systems konzentrieren, um echte Quantenvorteile zu liefern. Dieser ganzheitliche Ansatz umfasst Folgendes:

* Aufbau eines Quantencomputers mit zuverlässigen, skalierbaren und fehlertoleranten topologischen Qubits 
* Entwicklung einer einzigartigen kryogenischen Steuerungsebene mit geringer Verlustleistung und Wärmeabgabe 
* Entwicklung eines vollständigen Softwarestapels zur Programmierung des Quantencomputers und zur Steuerung des skalierbaren Systems.

Das Open-Source-QDK (Quantum Development Kit) wurde eingeführt, um Quantenprogrammierung und die Entwicklung von Algorithmen zugänglicher zu machen. Unsere übergeordnete Programmiersprache namens Q# ist auf die Bewältigung der Herausforderungen im Bereich der Quantenprogrammierung ausgelegt.  Q# ist als übergeordnete quantenorientierte Programmiersprache für die Entwicklung von Algorithmen und Anwendungen konzipiert. Der Q#-Compiler ist in einen Softwarestapel integriert, der es ermöglicht, einen Quantenalgorithmus bis zu den primitiven Operationen eines Quantencomputers hinab zu kompilieren.  Bis zu einem bestimmten Maßstab (Anzahl Qubits) können Quantencomputer auf einem klassischen Computer simuliert werden. Mithilfe von Simulation können Sie heute beginnen, Quantenprogramme zu schreiben, die morgen auf Quantenhardware ausgeführt werden können.  Darüber hinaus stehen Beispiele, Bibliotheken und Lernübungen für Q# zur Verfügung, um Ihnen den Einstieg in die Quantenprogrammierung zu erleichtern. 

## <a name="next-steps"></a>Nächste Schritte

* [Was können Quantencomputer?](xref:microsoft.quantum.overview.computers)
* [Einstieg in das Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)
* Weitere Informationen zu [Konzepten des Quantencomputings](xref:microsoft.quantum.concepts.intro)
