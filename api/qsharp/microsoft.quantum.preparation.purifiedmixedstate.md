---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: Purifedmixedstate-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 594a1d9fa674e457ab88072ade4198283b677af6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854307"
---
# <a name="purifiedmixedstate-function"></a>Purifedmixedstate-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen Vorgang zurück, der eine Reinigung eines gegebenen gemischten Zustands vorbereitet.
Ein "gereinigter gemischter Zustand" bezieht sich auf Zustände in der Form | ψ ⟩ =. i. PI | i ⟩ | garbagei ⟩ angegeben durch einen Vektor von Koeffizienten {Pi}. Zustände dieses Formulars können auf gemischte Zustände reduziert werden p ≔ Pi | i ⟩ ⟨ i | durch die Ablauf Verfolgung über das "Garbage Register" (d. h. ein gemischter Zustand, der in der Berechnungsbasis diagonal ist).

Weitere Erläuterungen finden Sie unter https://arxiv.org/pdf/1805.03662.pdf?page=15 .

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Beschreibung

Verwendet die Quantum-Rom-Technik, um eine gegebene Dichte Matrix darzustellen, und gibt diese Darstellung als Zustands Vorbereitungs Vorgang zurück.

Insbesondere, wenn eine Liste mit $N $ Koeffizienten $ \ alpha_j $, diese Funktion gibt einen Vorgang zurück, der die Quantum Rom-Technik verwendet, um eine Näherung von $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \ zu vorbereiten. End{align} $ $ des gemischten Zustands $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ Frac {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{align} $ $, wobei jeder $p _J $ eine Näherung zum gegebenen Koeffizienten $ \ alpha_j $ darstellt, sodass $ $ \begin{align} \left | p_j-\bruch{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ für jede $j $.

Wenn ein Indexregister und ein Register von Garbage Qubits, anfänglich im Status $ \ket {0} \ket{00\cdots 0}, übergeben werden, bereitet der zurückgegebene Vorgang beide Register bei der Bereinigung von $ \tilde \rho $ vor. $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{Garbage} _J}, \end{align} $ $, damit das Zurücksetzen und Aufheben der Zuordnung des Garbage Registers die gewünschte Vorbereitung innerhalb des Ziel Fehlers $ \epsilon $ aufsetzt.

## <a name="input"></a>Eingabe

### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Der Ziel Fehler $ \epsilon $.


### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von $N $ Koeffizienten, das die Wahrscheinlichkeit von Basis Zuständen angibt.
Negative Zahlen $-\ alpha_j $ werden als positiv $ | \ alpha_j | $ behandelt.



## <a name="output--mixedstatepreparation"></a>Ausgabe: [mixedstatepreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Ein Vorgang, bei dem $ \tilde \rho $ als Bereinigung auf einen gemeinsamen Index und ein Garbage Register vorbereitet wird.

## <a name="example"></a>Beispiel

Der folgende Code Ausschnitt bereitet eine Reinigung des $3 $-Qubit-Zustands $ \rho = \ sum_ {j = 0} ^ {4} \bruchteil {| alpha_j |} vor. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $, wobei "$ \vec\alpha = (1.0, 2,0, 3,0, 4,0, 5,0) $" und der Ziel Fehler "$10 ^ $" lautet {-3} :

```qsharp
let coefficients = [1.0, 2.0, 3.0, 4.0, 5.0];
let targetError = 1e-3;
let purifiedState = PurifiedMixedState(targetError, coefficients);
using (indexRegister = Qubit[purifiedState::Requirements::NIndexQubits]) {
    using (garbageRegister = Qubit[purifiedState::Requirements::NGarbageQubits]) {
        purifiedState::Prepare(LittleEndian(indexRegister), new Qubit[0], garbageRegister);
    }
}
```

## <a name="remarks"></a>Bemerkungen

Die Koeffizienten, die für diesen Vorgang bereitgestellt werden, werden nach der Norm 1 normalisiert, sodass die Koeffizienten immer als eine gültige kategorische Wahrscheinlichkeitsverteilung bezeichnet werden.

## <a name="references"></a>References

- Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. purienedmixedstatewithdata](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)