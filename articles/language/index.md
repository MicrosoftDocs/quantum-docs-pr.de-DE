---
title: Programmiersprache Q# | Microsoft-Dokumentation
description: Programmiersprache Q#
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: 560926f6f3e05c32a935f01ca5107a614e743ee2
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442484"
---
# <a name="the-q-programming-language"></a>Programmiersprache Q#

## <a name="introduction"></a>Einführung

Eine gängige Vorgehensweise beim Quantencomputing ist die Behandlung des Quantencomputers als Coprozessor, ähnlich wie bei GPUs, FPGAs und anderen ergänzenden Prozessoren.
Von der Hauptsteuerlogik wird klassischer Code auf einem klassischen „Hostcomputer“ ausgeführt.
Falls dies gewünscht bzw. erforderlich ist, kann über das Hostprogramm eine Unterroutine aufgerufen werden, die auf dem ergänzenden Prozessor ausgeführt wird.
Nach Abschluss der Unterroutine erhält das Hostprogramm Zugriff auf die entsprechenden Ergebnisse.

Q# (Q-Sharp) ist eine domänenspezifische Programmiersprache, die zum Ausdrücken von Quantenalgorithmen verwendet wird.
Sie wird zum Schreiben von Unterroutinen genutzt, die auf einem ergänzenden Quantenprozessor ausgeführt werden. Für die Steuerung werden hierbei ein klassisches Hostprogramm und ein Computer eingesetzt.
Bis zur allgemeinen Verfügbarkeit von Quantenprozessoren werden Q#-Unterroutinen auf einem Simulator ausgeführt.

Von Q# werden einige primitive Typen bereitgestellt, und es gibt zwei Möglichkeiten (Arrays und Tupel) zum Erstellen von neuen strukturierten Typen.
Es wird ein einfaches Prozedurmodell zum Schreiben von Programmen mit Schleifen und If/Then-Anweisungen unterstützt.
Die Konstrukte der obersten Ebene in Q# sind benutzerdefinierte Typen, Vorgänge und Funktionen.

In den folgenden Abschnitten finden Sie hilfreiche Informationen:
- [Typmodell](xref:microsoft.quantum.language.type-model)
- [Ausdrücke](xref:microsoft.quantum.language.expressions)
- [Anweisungen](xref:microsoft.quantum.language.statements)
- [Dateistruktur](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a>Konventionen

Derzeit arbeiten wir auf das Ziel hin, dass in allen Fällen eine einheitliche allgemeine Interpunktion verwendet wird.
Dahinter steht die Erwartung, dass Q# so einfacher zu erlernen und zu lesen ist. Der Grund ist, dass die Interpunktion dann immer die gleiche Bedeutung hat und ein Konzept immer auf die gleiche Weise dargestellt wird.

Dies gilt insbesondere in folgenden Fällen:

- Das Semikolon (`;`) wird als Abschluss einer ein- oder mehrzeiligen Anweisung verwendet.
  Es wird nicht für andere Zwecke genutzt.
- Das Komma (`,`) wird verwendet, um Elemente einer Sequenz zu trennen. Es wird für Tupelliterale, Arrayliterale, Argumentlisten, Tupeldefinitionen und Typlisten genutzt. **Aufgrund einer Änderung gegenüber früheren Versionen wird `;` nicht mehr als Arrayliteral-Trennzeichen unterstützt.**
- Der Doppelpunkt (`:`) wird verwendet, um eine Typanmerkung einzufügen. Er wird hauptsächlich in aufrufbaren Signaturen verwendet.
  Da mit dem Doppelpunkt immer eine Typsignatur eingefügt wird, wird für den in 0.3 eingeführten ternären bedingten Operator ein vertikaler Balken (`|`) verwendet, um die Wahr- und Falsch-Werte zu trennen. Aus diesem Grund wird in Q# als Trennzeichen `cond ? tval | fval` anstelle des Doppelpunkts wie in C genutzt.
  
