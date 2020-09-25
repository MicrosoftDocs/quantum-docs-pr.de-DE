---
title: Lineare Algebra für Quantencomputing
description: Hier finden Sie Informationen zu den grundlegenden Konzepten der linearen Algebra, die zum Verständnis des Quantencomputings benötigt werden.
author: bradben
ms.author: v-benbra
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.algebra
no-loc:
- Q#
- $$v
ms.openlocfilehash: bff1da475f87278bc9e769805b3fe0fe8704d47a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835127"
---
# <a name="linear-algebra-for-quantum-computing"></a>Lineare Algebra für Quantencomputing

Lineare Algebra ist die Sprache des Quantencomputings. Sie müssen zwar nicht mit ihr vertraut sein, um Quantenprogramme implementieren oder schreiben zu können, sie wird jedoch im Allgemeinen verwendet, um Qubit-Zustände und Quantenoperationen zu beschreiben und die Reaktion eines Quantencomputers auf eine Reihe von Anweisungen vorherzusagen.

Die Vertrautheit mit den [grundlegenden Konzepten der Quantenphysik](xref:microsoft.quantum.overview.understanding) kann für das Verständnis des Quantencomputings ebenso hilfreich sein, wie gewisse Grundkenntnisse im Bereich der linearen Algebra zum besseren Verständnis der Funktionsweise von Quantenalgorithmen beitragen. Sie sollten zumindest mit **Vektoren** und **Matrizenmultiplikation** vertraut sein. In den folgenden Tutorials werden noch einmal die Grundlagen behandelt, falls Sie Ihre Kenntnisse im Zusammenhang mit diesen Algebrakonzepten auffrischen möchten:

- [Jupyter Notebook-Tutorial zu linearer Algebra](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/LinearAlgebra)
- [Jupyter Notebook-Tutorial zu komplexer Arithmetik](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ComplexArithmetic)
- [Lineare Algebra für Quantencomputing](https://cds.cern.ch/record/1522001/files/978-1-4614-6336-8_BookBackMatter.pdf)
- [Grundlagen der linearen Algebra](https://www.math.ubc.ca/~carrell/NB.pdf)
- [Einführung in Quantencomputing](https://www.codeproject.com/Articles/5155638/Quantum-Computation-Primer-Part-1#exploring-quantum-superposition)

## <a name="vectors-and-matrices-in-quantum-computing"></a>Vektoren und Matrizen beim Quantencomputing

Im Thema [Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding) haben Sie gelernt, dass sich ein Qubit im Zustand 1 oder 0 oder in Superposition (also in beiden Zuständen) befinden kann. In der linearen Algebra wird der Zustand eines Qubits als Vektor beschrieben und durch eine einspaltige **Matrix** $\begin{bmatrix} a \\\\  b \end{bmatrix}$ dargestellt. Er wird auch als **Quantenzustandsvektor** (oder einfach nur Zustandsvektor) bezeichnet und muss folgende Anforderung erfüllen: $|a|^2 + |b|^2 = 1$.  

Die Elemente der Matrix stellen die Wahrscheinlichkeit dafür dar, dass das Qubit nach dem Kollaps einen bestimmten Zustand aufweist. Dabei ist $|a|^2$ die Wahrscheinlichkeit, dass es nach dem Kollaps 0 ist, und $|b|^2$ die Wahrscheinlichkeit, dass es nach dem Kollaps 1 ist. Die folgenden Matrizen stellen jeweils gültige Zustandsvektoren dar:

$$\begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \begin{bmatrix} 0 \\\\  1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{-1}{\sqrt{2}} \end{bmatrix} \text{ und }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{i}{\sqrt{2}} \end{bmatrix}.$$

In [Quantencomputer und -simulatoren](xref:microsoft.quantum.overview.simulators) haben Sie außerdem gelernt, dass Quantenoperationen verwendet werden, um den Zustand eines Qubits zu ändern.  Quantenoperationen können ebenfalls durch eine Matrix dargestellt werden. Wenn eine Quantenoperation auf ein Qubit angewendet wird, werden die beiden zur Darstellung verwendeten Matrizen multipliziert, und die resultierende Antwort stellt den neuen Zustand des Qubits nach der Operation dar.  

Hier sehen Sie die Darstellung zweier gängiger Quantenoperationen mit Matrizenmultiplikation:


Die [`X`-Operation](xref:microsoft.quantum.intrinsic.x) wird durch die Pauli-Matrix $X$ dargestellt:

$$X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}$$
    
Sie wird verwendet, um den Zustand eines Qubits von 0 in 1 zu ändern (oder umgekehrt). Beispiel:

$$\begin{bmatrix}0 &1\\\\ 1 &0\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \begin{bmatrix} 0 \\\\  1 \end{bmatrix}$$

Die [H-Operation](xref:microsoft.quantum.intrinsic.h) wird durch die Hadamard-Transformation $H$ dargestellt:

$$H = \dfrac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}$$

 Sie versetzt ein Qubit in einen Superpositionszustand mit ausgeglichener Wahrscheinlichkeit des Ergebnisses beim Kollaps, wie hier zu sehen:

$$\frac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix}=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=\left(\frac{1}{\sqrt{2}}\right)^2=\frac{1}{2}$$

Eine Matrix, die eine Quantenoperation darstellt, muss **unitär** sein. Eine Matrix ist unitär, wenn die **Inverse** der Matrix der **konjugierten Transponierten** der Matrix entspricht.

## <a name="representing-two-qubit-states"></a>Darstellen von Zuständen mit zwei Qubits

In den obigen Beispielen wurde der Zustand eines einzelnen Qubits mithilfe einer einspaltigen Matrix $\begin{bmatrix} a \\\\  b \end{bmatrix}$ und die Anwendung einer Operation durch die Multiplikation der beiden Matrizen beschrieben. Von Quantencomputern wird jedoch nicht nur ein Qubit verwendet. Wie lässt sich also der kombinierte Zustand von zwei Qubits beschreiben? 

Da jedes Qubit wie bereits erwähnt ein Vektorraum ist, können sie nicht einfach multipliziert werden. Stattdessen wird ein **Tensorprodukt** verwendet. Hierbei handelt es sich um eine verwandte Operation, die auf der Grundlage einzelner Vektorräume einen neuen Vektorraum erstellt und durch das Symbol $\otimes$ dargestellt wird. So wird beispielsweise das Tensorprodukt der beiden Qubit-Zustände $\begin{bmatrix} a \\\\  b \end{bmatrix}$ und $\begin{bmatrix} c \\\\  d \end{bmatrix}$ wie folgt berechnet:

$$ \begin{bmatrix} a \\\\  b \end{bmatrix} \otimes \begin{bmatrix} c \\\\  d \end{bmatrix} =\begin{bmatrix} a \begin{bmatrix} c \\\\  d \end{bmatrix} \\\\ b \begin{bmatrix}c \\\\  d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix} $$

Das Ergebnis ist eine vierdimensionale Matrix, wobei jedes Element eine Wahrscheinlichkeit darstellt. $ac$ ist beispielsweise die Wahrscheinlichkeit, dass die beiden Qubits nach dem Kollaps 0 und 0 sind, $ad$ ist die Wahrscheinlichkeit für 0 und 1 und so weiter. 

Ein einzelner Qubit-Zustand $\begin{bmatrix} a \\\\  b \end{bmatrix}$ muss die Anforderung $|a|^2 + |b|^2 = 1$ erfüllen, um einen Quantenzustand darzustellen. Analog dazu muss ein Zustand mit zwei Qubits $\begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}$ die folgende Anforderung erfüllen: $|ac|^2 + |ad|^2 + |bc|^2+ |bd|^2 = 1$.

## <a name="summary"></a>Zusammenfassung

Lineare Algebra ist die Standardsprache zur Beschreibung von Quantencomputing und Quantenphysik. Die im Microsoft Quantum Development Kit enthaltenen [Bibliotheken](xref:microsoft.quantum.libraries) unterstützen Sie zwar beim Ausführen komplexer Quantenalgorithmen, ohne dass Sie sich im Detail mit der zugrunde liegenden Mathematik beschäftigen müssen. Trotzdem sollten Sie sich mit den Grundlagen vertraut machen, um sich schneller zurechtzufinden und über eine solide Basis zu verfügen, auf der Sie aufbauen können.

## <a name="next-steps"></a>Nächste Schritte

[Installieren des QDK](xref:microsoft.quantum.install)
