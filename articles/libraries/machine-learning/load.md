---
title: Klassische Daten werden geladen
description: Erfahren Sie, wie Sie ein eigenes Dataset laden, um ein Klassifizierungs Modell mit dem Microsoft Quantum Development Kit (QDK) zu trainieren.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
ms.openlocfilehash: efa4a65a489446cbef48507d0b02a932da74c71c
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327661"
---
# <a name="load-and-classify-your-own-datasets"></a><span data-ttu-id="defc9-103">Laden und klassifizieren ihrer eigenen Datasets</span><span class="sxs-lookup"><span data-stu-id="defc9-103">Load and classify your own datasets</span></span>

<span data-ttu-id="defc9-104">In diesem kurzen Tutorial erfahren Sie, wie Sie Ihr eigenes Dataset laden, um ein Klassifizierungs Modell mit dem Quantum Development Kit (QDK) zu trainieren.</span><span class="sxs-lookup"><span data-stu-id="defc9-104">In this short tutorial, we are going to learn how to load your own dataset to train a classifier model with the Quantum Development Kit (QDK).</span></span>

<span data-ttu-id="defc9-105">Wir empfehlen Ihnen dringend die Verwendung eines standardisierten Serialisierungsformats, wie z. b. [JSON-Dateien](https://en.wikipedia.org/wiki/JSON) , um Ihre Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="defc9-105">We highly recommend the use of a standardized serialization format such as [JSON files](https://en.wikipedia.org/wiki/JSON) to store your data.</span></span>
<span data-ttu-id="defc9-106">Solche Formate bieten eine hohe Kompatibilität mit verschiedenen Frameworks wie Python und dem .NET-Ökosystem.</span><span class="sxs-lookup"><span data-stu-id="defc9-106">Such formats offer high compatibility with different frameworks like Python and the .NET ecosystem.</span></span>
<span data-ttu-id="defc9-107">Insbesondere wird empfohlen, die Vorlage zum Laden der Daten zu verwenden, damit Sie den Code direkt aus den Beispielen kopieren können.</span><span class="sxs-lookup"><span data-stu-id="defc9-107">In particular, we recommend using our template for loading the data, so that you can copy-paste the code directly from the samples.</span></span>

## <a name="template-for-loading-your-datasets"></a><span data-ttu-id="defc9-108">Vorlage zum Laden von Datasets</span><span class="sxs-lookup"><span data-stu-id="defc9-108">Template for loading your datasets</span></span>

<span data-ttu-id="defc9-109">Angenommen, wir haben ein Trainings Dataset $ (x, y) $ der Größe $N = $2, wobei jede Instanz $x _I $ von $x $ drei Features hat: $x _ {I1} $, $x _ {I2} $ und $x _ {I3} $.</span><span class="sxs-lookup"><span data-stu-id="defc9-109">Suppose we have a training dataset $(x, y)$ of size $N=2$ where each instance $x_i$ of $x$ has three features: $x_{i1}$, $x_{i2}$ and $x_{i3}$.</span></span>
<span data-ttu-id="defc9-110">Das Validierungs DataSet hat die gleiche Struktur.</span><span class="sxs-lookup"><span data-stu-id="defc9-110">The validation dataset has the same structure.</span></span>
<span data-ttu-id="defc9-111">Diese Datensätze können durch eine Datei dargestellt werden `data.json` , die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="defc9-111">These datsets can be represented by a `data.json` file similar to the following:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a><span data-ttu-id="defc9-112">Beispiel für die Verwendung der Vorlage</span><span class="sxs-lookup"><span data-stu-id="defc9-112">Example using the template</span></span>

<span data-ttu-id="defc9-113">Angenommen, wir verfügen über ein kleines DataSet mit den Höhen und Gewichtungen von unterschiedlichen Katzen und Hunden.</span><span class="sxs-lookup"><span data-stu-id="defc9-113">Suppose we have a small dataset with the heights and weights of different cats and dogs.</span></span> <span data-ttu-id="defc9-114">Dieses DataSet ist sehr klein, um ein Modell zu trainieren, reicht aber aus, um den Prozess des Ladens eines Datasets anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="defc9-114">This dataset is very small to train a model but will be enough to show the process of loading a dataset.</span></span>

| <span data-ttu-id="defc9-115">Höhe (m)</span><span class="sxs-lookup"><span data-stu-id="defc9-115">Height (m)</span></span> | <span data-ttu-id="defc9-116">Gewichtung (kg)</span><span class="sxs-lookup"><span data-stu-id="defc9-116">Weight (kg)</span></span> | <span data-ttu-id="defc9-117">Tier</span><span class="sxs-lookup"><span data-stu-id="defc9-117">Animal</span></span> |
|-----------|------------|--------|
| <span data-ttu-id="defc9-118">0,54</span><span class="sxs-lookup"><span data-stu-id="defc9-118">0.54</span></span>      | <span data-ttu-id="defc9-119">30</span><span class="sxs-lookup"><span data-stu-id="defc9-119">30</span></span>         | <span data-ttu-id="defc9-120">Hund</span><span class="sxs-lookup"><span data-stu-id="defc9-120">Dog</span></span>    |
| <span data-ttu-id="defc9-121">0,30</span><span class="sxs-lookup"><span data-stu-id="defc9-121">0.30</span></span>      | <span data-ttu-id="defc9-122">8</span><span class="sxs-lookup"><span data-stu-id="defc9-122">8</span></span>          | <span data-ttu-id="defc9-123">Cat</span><span class="sxs-lookup"><span data-stu-id="defc9-123">Cat</span></span>    |
| <span data-ttu-id="defc9-124">0,91</span><span class="sxs-lookup"><span data-stu-id="defc9-124">0.91</span></span>      | <span data-ttu-id="defc9-125">44</span><span class="sxs-lookup"><span data-stu-id="defc9-125">44</span></span>         | <span data-ttu-id="defc9-126">Hund</span><span class="sxs-lookup"><span data-stu-id="defc9-126">Dog</span></span>    |
| <span data-ttu-id="defc9-127">0,86</span><span class="sxs-lookup"><span data-stu-id="defc9-127">0.86</span></span>      | <span data-ttu-id="defc9-128">31</span><span class="sxs-lookup"><span data-stu-id="defc9-128">31</span></span>          | <span data-ttu-id="defc9-129">Hund</span><span class="sxs-lookup"><span data-stu-id="defc9-129">Dog</span></span>    |
| <span data-ttu-id="defc9-130">0,32</span><span class="sxs-lookup"><span data-stu-id="defc9-130">0.32</span></span>      | <span data-ttu-id="defc9-131">5</span><span class="sxs-lookup"><span data-stu-id="defc9-131">5</span></span>         | <span data-ttu-id="defc9-132">Cat</span><span class="sxs-lookup"><span data-stu-id="defc9-132">Cat</span></span>    |
| <span data-ttu-id="defc9-133">0,25</span><span class="sxs-lookup"><span data-stu-id="defc9-133">0.25</span></span>      | <span data-ttu-id="defc9-134">4</span><span class="sxs-lookup"><span data-stu-id="defc9-134">4</span></span>          | <span data-ttu-id="defc9-135">Cat</span><span class="sxs-lookup"><span data-stu-id="defc9-135">Cat</span></span>    |

<span data-ttu-id="defc9-136">Der Prozess lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="defc9-136">The process is:</span></span>

- <span data-ttu-id="defc9-137">Zuerst müssen wir das Dataset in Schulungen und Validierung aufteilen.</span><span class="sxs-lookup"><span data-stu-id="defc9-137">First we need to separate the dataset into training and validation.</span></span> <span data-ttu-id="defc9-138">In diesem Fall können wir einfach die ersten drei Beispiele für das Training und die restlichen Beispiele für die Überprüfung verwenden.</span><span class="sxs-lookup"><span data-stu-id="defc9-138">In this case we can just take the first three samples for training and the rest of samples for validation.</span></span> <span data-ttu-id="defc9-139">Im Allgemeinen empfiehlt es sich, das Trainings-und Validierungs Dataset nach dem Zufallsprinzip zu testen, um unerwünschte Bias in den Trainingsdaten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="defc9-139">In general it is a good practice to sample randomly the training and validation dataset to avoid unwanted biases in the training data.</span></span>
- <span data-ttu-id="defc9-140">Zweitens muss jeder Klasse eine numerische Bezeichnung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="defc9-140">Secondly, we need to assign a numeric label to each class.</span></span> <span data-ttu-id="defc9-141">Beachten Sie, dass die QML-Bibliothek momentan nur binäre Klassifizierungs Probleme zulässt.</span><span class="sxs-lookup"><span data-stu-id="defc9-141">Note that, for the moment, the QML library only admits binary classification problems.</span></span> <span data-ttu-id="defc9-142">Daher weisen wir die Bezeichnung 0 der `Dog` -Klasse und die Zahl 1 der-Klasse zu `Cat` .</span><span class="sxs-lookup"><span data-stu-id="defc9-142">So we will assign the label 0 to the class `Dog` and the number 1 to the class `Cat`.</span></span>
- <span data-ttu-id="defc9-143">Zum Schluss füllen wir die Vorlage mithilfe der Daten aus dem DataSet aus.</span><span class="sxs-lookup"><span data-stu-id="defc9-143">Finally, we fill the template using the data from our dataset.</span></span> <span data-ttu-id="defc9-144">Beachten Sie, dass Sie für große Datasets ein kleines Skript erstellen sollten, um die Vorlage automatisch aus dem jeweiligen Dataset zu generieren.</span><span class="sxs-lookup"><span data-stu-id="defc9-144">Note that for big datasets you should build a small script to automatically generate the template from your specific dataset.</span></span> <span data-ttu-id="defc9-145">Dieses Skript hängt vom ursprünglichen Format des Datasets ab.</span><span class="sxs-lookup"><span data-stu-id="defc9-145">This script will depend on the original format of your dataset.</span></span>

<span data-ttu-id="defc9-146">Für unser DataSet `data.json` lautet die Datei:</span><span class="sxs-lookup"><span data-stu-id="defc9-146">For our dataset the `data.json` file is:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a><span data-ttu-id="defc9-147">Laden der Daten</span><span class="sxs-lookup"><span data-stu-id="defc9-147">Loading the data</span></span>

<span data-ttu-id="defc9-148">Nachdem Sie Ihre Daten als JSON-Datei serialisiert haben, können Sie Sie in mithilfe von JSON-Bibliotheken laden, die mit Ihrer bevorzugten Host Sprache bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="defc9-148">Once you have your data serialized as a JSON file, you can load it in using JSON libraries provided with your host language of choice.</span></span>

### <a name="python"></a>[<span data-ttu-id="defc9-149">Python</span><span class="sxs-lookup"><span data-stu-id="defc9-149">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="defc9-150">Python stellt das [integrierte `json` Paket](https://docs.python.org/3.7/library/json.html) zum Arbeiten mit JSON-serialisierten Daten bereit:</span><span class="sxs-lookup"><span data-stu-id="defc9-150">Python provides the [built-in `json` package](https://docs.python.org/3.7/library/json.html) for working with JSON-serialized data:</span></span>

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[<span data-ttu-id="defc9-151">C#</span><span class="sxs-lookup"><span data-stu-id="defc9-151">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="defc9-152">Die .net Core-Plattform stellt das [ `System.Text.Json` Paket](https://www.nuget.org/packages/System.Text.Json) zum Arbeiten mit JSON-serialisierten Daten bereit:</span><span class="sxs-lookup"><span data-stu-id="defc9-152">The .NET Core platform provides the [`System.Text.Json` package](https://www.nuget.org/packages/System.Text.Json) for working with JSON-serialized data:</span></span>

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a><span data-ttu-id="defc9-153">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="defc9-153">Next steps</span></span>

<span data-ttu-id="defc9-154">Nun können Sie Ihre eigenen Experimente mit ihren eigenen Datasets ausführen.</span><span class="sxs-lookup"><span data-stu-id="defc9-154">Now you are ready to start running your own experiments with your own datasets.</span></span> <span data-ttu-id="defc9-155">Probieren Sie verschiedene Klassifizierungen und Datasets aus, und tragen Sie zur Community bei, die ihre Ergebnisse gemeinsam nutzen!</span><span class="sxs-lookup"><span data-stu-id="defc9-155">Try different classifiers and dataset and contribute to the community sharing your results!</span></span>
