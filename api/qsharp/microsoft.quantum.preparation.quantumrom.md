---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: Quantenrom-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229884"
---
# <a name="quantumrom-function"></a>Quantenrom-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Quantum Rom ist veraltet. Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PurifiedMixedState>.

Verwendet die Quantum-Rom-Technik, um eine angegebene Dichte Matrix darzustellen.

Eine Liste mit $N $ Koeffizienten $ \ alpha_j $, dadurch wird ein einheitlicher $U $ zurückgegeben, der die Quantum-Rom-Technik verwendet, um eine Näherung von $ \tilde \rho\ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} $ der Reinigung der Dichte Matrix $ \rho = \ sum_ {j = 0} ^ {n-1} \bruchteil {| alpha_j |} zu erstellen. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $. In dieser Näherung ist der Fehler $ \epsilon $, dass $ | p_j-\bruch{| alpha_j |} {\ sum_k | \ alpha_k |} | \le \epsilon/N $ und $ \| \tilde \rho-\rho \| \le \epsilon $. Anders ausgedrückt: $ $ \begin{align} u\ket {0} ^ {\lceil\ Log_2 n\rceil} \ Ket {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{Garbage} _J}.
\end{align} $ $

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a>Eingabe

### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Der Ziel Fehler $ \epsilon $.


### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von $N $ Koeffizienten, das die Wahrscheinlichkeit von Basis Zuständen angibt.
Negative Zahlen $-\ alpha_j $ werden als positiv $ | \ alpha_j | $ behandelt.



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a>Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[, int,](xref:microsoft.quantum.lang-ref.int)[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit) ist ADJ + CTL)

## <a name="first-parameter"></a>Erster Parameter

Ein Tupel `(x,(y,z))` , bei dem `x = y + z` die Gesamtzahl der zugeordneten Qubits ist, `y` die Anzahl der Qubits für das `LittleEndian` Register und `z` die Anzahl der Garbage Qubits.

## <a name="second-parameter"></a>Zweiter Parameter

Die einnorm $ \ sum_j | \ alpha_j | $ des Koeffizienten-Arrays.

## <a name="third-parameter"></a>Dritter Parameter

Der einheitliche $U $.

## <a name="references"></a>Referenzen

- Encoding Electronic Spectra in Quantum-Verbindungen mit linearer T-Komplexität Ryan babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru paler, Austin Fowler, Hartmut netven https://arxiv.org/abs/1805.03662