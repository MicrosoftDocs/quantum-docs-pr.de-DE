---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: Purifedmixedstatewithdata-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: fc7bf8e6157af079ae4233ef45e67ce8ddfb8fe3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854277"
---
# <a name="purifiedmixedstatewithdata-function"></a>Purifedmixedstatewithdata-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen Vorgang zurück, der eine Bereinigung eines gegebenen gemischten Zustands vorbereitet, der durch ein Register entkoppelt ist, das eine angegebene Auflistung von Daten darstellt.
Ein "gereinigter gemischter Zustand mit Daten" bezieht sich auf den Zustand "", "", "", "", "⟩" | "⟩" | "garbagei ⟩", wobei jede XI-Datei eine Bitzeichenfolge ist

Weitere Erläuterungen finden Sie unter https://arxiv.org/pdf/1805.03662.pdf?page=15 .

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Beschreibung

Verwendet die Quantum-Rom-Technik, um eine gegebene Dichte Matrix darzustellen, und gibt diese Darstellung als Zustands Vorbereitungs Vorgang zurück.

Insbesondere, wenn eine Liste mit $N $ Koeffizienten $ \ alpha_j $,_Diese Funktion gibt einen Vorgang zurück, der die Quantum-Rom-Technik zum Vorbereiten einer Näherung von $ $ verwendet. \begin{align} \tilde \rho = \sum_{j = 0} ^ {N-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _J} \bra{\vec{x}_j} \end{align} $ $ des gemischten Zustands $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ Frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _J} \bra{\vec{x} _J}, \end{align} $ $, wobei jeder $p _J $ eine Näherung zum gegebenen Koeffizienten $ \ alpha_j $ darstellt, sodass $ $ \begin{align} \left | p_j-\bruch{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ für jede $j $.

Wenn ein Indexregister und ein Register von Garbage Qubits, anfänglich im Status $ \ket {0} \ket{00\cdots 0}, übergeben werden, bereitet der zurückgegebene Vorgang beide Register bei der Bereinigung von $ \tilde \rho $ vor. $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _J} \ket{\text{Garbage} _J}, \end{align} $ $, damit das Zurücksetzen und Aufheben der Zuordnung des Garbage Registers die gewünschte Vorbereitung für innerhalb des Ziel Fehlers $ \epsilon $ aufsetzt.

## <a name="input"></a>Eingabe

### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Der Ziel Fehler $ \epsilon $.


### <a name="coefficients--doublebool"></a>Koeffizienten: ([Double](xref:microsoft.quantum.lang-ref.double),[bool](xref:microsoft.quantum.lang-ref.bool)[]) []

Ein Array von $N $ Koeffizienten, das die Wahrscheinlichkeit der Basiszustände zusammen mit der bitstring $ \vec{x} _J $ angibt, die mit jedem Koeffizienten verknüpft ist.
Negative Zahlen $-\ alpha_j $ werden als positiv $ | \ alpha_j | $ behandelt.



## <a name="output--mixedstatepreparation"></a>Ausgabe: [mixedstatepreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Ein Vorgang, bei dem $ \tilde \rho $ als Bereinigung auf einen gemeinsamen Index und ein Garbage Register vorbereitet wird.

## <a name="remarks"></a>Bemerkungen

Die Koeffizienten, die für diesen Vorgang bereitgestellt werden, werden nach der Norm 1 normalisiert, sodass die Koeffizienten immer als eine gültige kategorische Wahrscheinlichkeitsverteilung bezeichnet werden.

## <a name="references"></a>References

- Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. purifedmixedstate](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)