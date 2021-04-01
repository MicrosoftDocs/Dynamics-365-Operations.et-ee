---
title: Masinõppemudelite tulemused (eelversioon)
description: Selles teemas käsitletakse segaduse maatrikseid, klassifitseerimisprobleeme ja täpsust masinõppe (ML) mudelites. Eesmärk on parandada oma arusaamist ML-i prognoosimise tulemuste täpsusest.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: dcdc6d501f09b639eb0d7504e0f760a66bb3dbc7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208529"
---
# <a name="results-of-machine-learning-models-preview"></a><span data-ttu-id="046dd-104">Masinõppemudelite tulemused (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="046dd-104">Results of machine learning models (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="046dd-105">Selles teemas käsitletakse segaduse maatrikseid, klassifitseerimisprobleeme ja täpsust masinõppe (ML) mudelites.</span><span class="sxs-lookup"><span data-stu-id="046dd-105">This topic discusses confusion matrices, classification problems, and accuracy in machine learning (ML) models.</span></span> <span data-ttu-id="046dd-106">Eesmärk on parandada oma arusaamist ML-i prognoosimise tulemuste täpsusest.</span><span class="sxs-lookup"><span data-stu-id="046dd-106">The purpose is to enhance your understanding of accuracy in ML prediction results.</span></span> <span data-ttu-id="046dd-107">Sihtrühma kuuluvad insenerid, analüütikud ja juhid, kes soovivad luua oma teadmisi ja oskusi andmeteaduses.</span><span class="sxs-lookup"><span data-stu-id="046dd-107">The target audience includes engineers, analysts, and managers who want to build their knowledge and skills in data science.</span></span>

## <a name="confusion-matrix"></a><span data-ttu-id="046dd-108">Segaduse maatriks</span><span class="sxs-lookup"><span data-stu-id="046dd-108">Confusion matrix</span></span>
<span data-ttu-id="046dd-109">Pärast seda kui jälgitav ML-i probleem on ajalooliste andmete komplekti põhjal koolitatud, seda testitakse kasutades andmeid, mis on koolitusprotsessist eemale jäänud.</span><span class="sxs-lookup"><span data-stu-id="046dd-109">After a supervised ML problem is trained on a set of historical data, it's tested by using data that is withheld from the training process.</span></span> <span data-ttu-id="046dd-110">Sel viisil saate võrrelda koolitatud mudeli prognoose tegelike väärtustega.</span><span class="sxs-lookup"><span data-stu-id="046dd-110">In this way, you can compare the predictions from the trained model with the actual values.</span></span> <span data-ttu-id="046dd-111">Segaduse maatriks annab võimaluse hinnata, kui edukas klassifitseerimise probleem on ja kus see teeb vigu (st kus see läheb segadusse).</span><span class="sxs-lookup"><span data-stu-id="046dd-111">The confusion matrix provides a means of evaluating how successful a classification problem is and where it makes mistakes (that is, where it becomes "confused").</span></span>

<span data-ttu-id="046dd-112">Näiteks teie eesmärk on ennustada, kas lemmikloom on koer või kass, mis põhineb osadel füüsilistel ja käitumuslikel atribuutidel.</span><span class="sxs-lookup"><span data-stu-id="046dd-112">For example, your objective is to predict whether a pet is a dog or a cat, based on some physical and behavioral attributes.</span></span> <span data-ttu-id="046dd-113">Kui teil on testimise andmekomplektis 30 koera ja 20 kassi, võib segaduse maatriks sarnaneda järgmise illustratsiooniga.</span><span class="sxs-lookup"><span data-stu-id="046dd-113">If you have a test dataset that contains 30 dogs and 20 cats, the confusion matrix might resemble the following illustration.</span></span>

![Liikide prognoosimise näide](media/species-prediction-matrix.png)

<span data-ttu-id="046dd-115">Roheliste lahtrite numbrid tähistavad õigeid prognoose.</span><span class="sxs-lookup"><span data-stu-id="046dd-115">The numbers in the green cells represent correct predictions.</span></span> <span data-ttu-id="046dd-116">Nagu näete, mudel ennustas protsentuaalselt suurema osa kassidest õigesti.</span><span class="sxs-lookup"><span data-stu-id="046dd-116">As you can see, the model predicted a higher percentage of the actual cats correctly.</span></span> <span data-ttu-id="046dd-117">Mudeli üldist täpsust on lihtne arvutada.</span><span class="sxs-lookup"><span data-stu-id="046dd-117">The overall accuracy of the model is easy to calculate.</span></span> <span data-ttu-id="046dd-118">Sel juhul on see 42 ÷ 50 või 0,84.</span><span class="sxs-lookup"><span data-stu-id="046dd-118">In this case, it's 42 ÷ 50, or 0.84.</span></span>

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a><span data-ttu-id="046dd-119">Mitmeklassilised klassifikaatorid segaduse maatriksis</span><span class="sxs-lookup"><span data-stu-id="046dd-119">Multi-class classifiers in a confusion matrix</span></span>

<span data-ttu-id="046dd-120">Enamik arutelusid segaduse maatriksis on keskendunud binaarsetele klassifikaatoritele, nagu eelmises näites.</span><span class="sxs-lookup"><span data-stu-id="046dd-120">Most discussions about the confusion matrix are focused on binary classifiers, as in the preceding example.</span></span> <span data-ttu-id="046dd-121">See juhtum on erijuhtum, kus võib kaaluda muid mõõdikuid, näiteks tundlikkust ja tagasikutsumist.</span><span class="sxs-lookup"><span data-stu-id="046dd-121">This case is a special case where other metrics can be considered, such as sensitivity and recall.</span></span>

<span data-ttu-id="046dd-122">Järgmiseks vaatleme kolme olekuga finantsstsenaariumi klassifitseerimisprobleemi.</span><span class="sxs-lookup"><span data-stu-id="046dd-122">Next, we will consider a classification problem for a finance scenario that has three states.</span></span> <span data-ttu-id="046dd-123">Mudel ennustab, kas kliendiarve tasutakse õigel ajal, hilja või väga hilja.</span><span class="sxs-lookup"><span data-stu-id="046dd-123">The model predicts whether a customer invoice will be paid on time, late, or very late.</span></span> <span data-ttu-id="046dd-124">Näiteks 100 testarve seast 50 tasuti õigeaegselt, 35 tasuti hilja ja 15 tasuti väga hilja.</span><span class="sxs-lookup"><span data-stu-id="046dd-124">For example, out of 100 test invoices, 50 are paid on time, 35 are paid late, and 15 are paid very late.</span></span> <span data-ttu-id="046dd-125">Sel juhul võib mudel tekitada segaduse maatriksi, mis sarnaneb järgmise illustratsiooniga.</span><span class="sxs-lookup"><span data-stu-id="046dd-125">In this case, a model might produce a confusion matrix that resembles the following illustration.</span></span>

![Mudel 1](media/payment-prediction-matrix.png)<span data-ttu-id="046dd-127">]</span><span class="sxs-lookup"><span data-stu-id="046dd-127">]</span></span>

<span data-ttu-id="046dd-128">Segaduse maatriks annab oluliselt rohkem teavet kui lihtne täpsusmõõdik.</span><span class="sxs-lookup"><span data-stu-id="046dd-128">A confusion matrix provides significantly more information than a simple accuracy metric.</span></span> <span data-ttu-id="046dd-129">Samas see on seda suhteliselt lihtne mõista.</span><span class="sxs-lookup"><span data-stu-id="046dd-129">However, it's still relatively easy to understand.</span></span> <span data-ttu-id="046dd-130">Segaduse maatriks näitab, kas teil on tasakaalustatud andmekogum, kus väljundklassidel on sarnased arvud.</span><span class="sxs-lookup"><span data-stu-id="046dd-130">A confusion matrix tells you whether you have a balanced dataset where the output classes have similar counts.</span></span> <span data-ttu-id="046dd-131">Mitmeklassilise stsenaariumi puhul näitab see, kui kaugel võib ennustus olla, kui väljundklassid on järgklassid, nagu eelmises näites kliendimaksete kohta.</span><span class="sxs-lookup"><span data-stu-id="046dd-131">For the multi-class scenario, it tells you how far off a prediction might be when the output classes are ordinal, as in the preceding example about customer payments.</span></span>

## <a name="model-accuracy"></a><span data-ttu-id="046dd-132">Mudeli täpsus</span><span class="sxs-lookup"><span data-stu-id="046dd-132">Model accuracy</span></span> 
<span data-ttu-id="046dd-133">Erinevad täpsusmõõdikud on mudeli kvaliteedi kvantifitseerimise eeliseks.</span><span class="sxs-lookup"><span data-stu-id="046dd-133">Different accuracy metrics have the advantage of quantifying the model quality.</span></span> 

<span data-ttu-id="046dd-134">Kuna täpsus on kergesti mõistetav, on see hea lähtepunkt mudeli selgitamiseks teistele inimestele, eriti mudeli kasutajatele, kes ei ole andmeteadlased.</span><span class="sxs-lookup"><span data-stu-id="046dd-134">Because accuracy is an easy metric to understand, it's a good starting point for explaining a model to other people, especially to users of the model who aren't data scientists.</span></span> <span data-ttu-id="046dd-135">Mudeli täpsuse mõistmiseks ei ole vaja statistikat.</span><span class="sxs-lookup"><span data-stu-id="046dd-135">No understanding of statistics is required to understand the model's accuracy.</span></span> <span data-ttu-id="046dd-136">Kui segaduse maatriks on saadaval, annab see täiendava ülevaate mudeli jõudlusest.</span><span class="sxs-lookup"><span data-stu-id="046dd-136">When a confusion matrix is available, it provides further insight into the model's performance.</span></span>

<span data-ttu-id="046dd-137">Samas põhjalikuma arusaamise huvides tuleks siiski pöörata tähelepanu mitmetele täpsusega seotud probleemile.</span><span class="sxs-lookup"><span data-stu-id="046dd-137">However, for a more thorough understanding, several challenges that are associated with accuracy should be noted.</span></span> <span data-ttu-id="046dd-138">Mõõdik sõltub probleemi kontekstist.</span><span class="sxs-lookup"><span data-stu-id="046dd-138">The usefulness of the metric depends on the context of the problem.</span></span> <span data-ttu-id="046dd-139">Küsimus, mis sageli tekib seoses mudeli tulemuslikkusega, on: „Kui hea mudel on?”</span><span class="sxs-lookup"><span data-stu-id="046dd-139">A question that often arises in relation to model performance is, "How good is the model?"</span></span> <span data-ttu-id="046dd-140">Kuid vastata sellele küsimusele ei ole tingimata lihtne.</span><span class="sxs-lookup"><span data-stu-id="046dd-140">However, the answer to this question isn't necessarily straightforward.</span></span> <span data-ttu-id="046dd-141">Kaaluge järgmist segiajamise maatriksit (mudel 2).</span><span class="sxs-lookup"><span data-stu-id="046dd-141">Consider the following confusion matrix (model 2).</span></span>

![Makse ennustamise näide suurema näidisega](media/payment-prediction-matrix-2.png)

<span data-ttu-id="046dd-143">Kiire kalkulatsioon näitab, et selle mudeli täpsus on (70 + 10 + 3) ÷ 100 või 0,83.</span><span class="sxs-lookup"><span data-stu-id="046dd-143">A quick calculation shows that this model's accuracy is (70 + 10 + 3) ÷ 100, or 0.83.</span></span> <span data-ttu-id="046dd-144">Eemalt vaadates tundub, et tulemus on parem kui eelmise mitme klassi mudeli tulemus (mudel 1), mis oli 0,73 täpsusega.</span><span class="sxs-lookup"><span data-stu-id="046dd-144">On the surface, this result seems better than result for the previous multi-class model (model 1), which has an accuracy of 0.73.</span></span> <span data-ttu-id="046dd-145">Aga kas see on parem?</span><span class="sxs-lookup"><span data-stu-id="046dd-145">But is it better?</span></span>

<span data-ttu-id="046dd-146">Selle küsimuse lahendamiseks arvestage naiivne oletuse täpsusega.</span><span class="sxs-lookup"><span data-stu-id="046dd-146">To begin to address this question, consider the accuracy of a naïve guess.</span></span> <span data-ttu-id="046dd-147">Klassifikatsiooni probleemi puhul ennustab tavaline oletus alati kõige levinumat klassi.</span><span class="sxs-lookup"><span data-stu-id="046dd-147">For a classification problem, a simple guess will always predict the most common class.</span></span> <span data-ttu-id="046dd-148">Mudeli 1 puhul on see „õigel ajal” ja see loob täpsuse 0,50.</span><span class="sxs-lookup"><span data-stu-id="046dd-148">For model 1, that guess will be "on time," and it will produce an accuracy of 0.50.</span></span> <span data-ttu-id="046dd-149">Mudeli 2 oletuse puhul on see „õigel ajal” ja see loob täpsuse 0,80.</span><span class="sxs-lookup"><span data-stu-id="046dd-149">The guess for model 2 will also be "on time," and it will produce an accuracy of 0.80.</span></span> <span data-ttu-id="046dd-150">Kuna mudel 1 parandab naiivset oletust 0,73 – 0,50 = 0,23 võrra, siis mudel 2 parandab naiivset oletust 0,83 – 0,80 = 0,03 võrra, mistõttu mudel 1 on parem mudel, kuigi selle täpsus on väiksem.</span><span class="sxs-lookup"><span data-stu-id="046dd-150">Because model 1 improves on the naïve guess by 0.73 – 0.50 = 0.23, whereas model 2 improves on the naïve guess by 0.83 – 0.80 = 0.03, model 1 is a better model, even though it has lower accuracy.</span></span> <span data-ttu-id="046dd-151">Arvutus näitab, et mudeli kvaliteedi tõhus hindamine nõuab rohkem konteksti kui täpsuse väärtus.</span><span class="sxs-lookup"><span data-stu-id="046dd-151">The calculation reveals that effective assessment of a model's quality requires more context than the accuracy value.</span></span>

<span data-ttu-id="046dd-152">Tähelepanu väärib veel üks asjaolu.</span><span class="sxs-lookup"><span data-stu-id="046dd-152">Another aspect is worth noting.</span></span> <span data-ttu-id="046dd-153">Kaaluge stsenaariumi, kus meditsiinilise testi abil tuvastatakse patsiendi haigus.</span><span class="sxs-lookup"><span data-stu-id="046dd-153">Consider a scenario where a medical test is used to detect a disease in a patient.</span></span> <span data-ttu-id="046dd-154">See probleem on binaarne klassifikatsiooni probleem, kus positiivne tulemus näitab, et patsiendil on haigus.</span><span class="sxs-lookup"><span data-stu-id="046dd-154">This problem is a binary classification problem where a positive result indicates that the patient has the disease.</span></span> <span data-ttu-id="046dd-155">Selle stsenaariumi puhul tuleb mõelda järgmiste vigade mõjule.</span><span class="sxs-lookup"><span data-stu-id="046dd-155">In this scenario, you must think about the impact of the following errors:</span></span>

- <span data-ttu-id="046dd-156">Valepositiivsed, kus test ütleb, et patsient on haige, kuid tegelikult tal haigust pole</span><span class="sxs-lookup"><span data-stu-id="046dd-156">False positives, where the test says that a patient has the disease, but she doesn't really have it</span></span>
- <span data-ttu-id="046dd-157">Valenegatiivsed, kus test ütleb, et patsiendil ei ole haigust, kuid tegelikult tal on haigus</span><span class="sxs-lookup"><span data-stu-id="046dd-157">False negatives, where the test says that a patient doesn't have the disease, but he really does have it</span></span>

<span data-ttu-id="046dd-158">Loomulikult, mõlemat tüüpi viga on soovimatu, kuid mis on halvem?</span><span class="sxs-lookup"><span data-stu-id="046dd-158">Obviously, both types of error are undesirable, but which is worse?</span></span> <span data-ttu-id="046dd-159">Jällegi, see sõltub asjaoludest.</span><span class="sxs-lookup"><span data-stu-id="046dd-159">Again, it depends.</span></span> <span data-ttu-id="046dd-160">Eluohtliku haiguse korral, mis nõuab kiiret ravi, on prioriteediks valenegatiivsete andmete minimeerimine (loodetavasti järgnevad sellele täiendavaid teste).</span><span class="sxs-lookup"><span data-stu-id="046dd-160">In the case of a life-threatening disease that requires fast treatment, minimization of false negatives (hopefully followed by additional tests) takes priority.</span></span> <span data-ttu-id="046dd-161">Teiste vähem kriitiliste olukordade puhul võivad mudeli loojad selle asemel minimeerida valepositiivseid.</span><span class="sxs-lookup"><span data-stu-id="046dd-161">In other, less critical situations, the model creators might minimize false positives instead.</span></span> <span data-ttu-id="046dd-162">Igal juhul on mõistlik järeldada, et mudeli kvaliteedi tõhususe määramiseks peab teil olema rohkem teavet kui täpsuse mõõdik annab.</span><span class="sxs-lookup"><span data-stu-id="046dd-162">At any rate, a reasonable conclusion is that to effectively determine a model's quality, you must have more information than an accuracy metric provides.</span></span>

### <a name="recommendations"></a><span data-ttu-id="046dd-163">Soovitused</span><span class="sxs-lookup"><span data-stu-id="046dd-163">Recommendations</span></span>

<span data-ttu-id="046dd-164">Täpsus on oluline vahend suhtlemiseks domeeni asjatundjatega, kes ei ole statistikaga tuttavad.</span><span class="sxs-lookup"><span data-stu-id="046dd-164">Accuracy is an important tool for communicating with domain experts who aren't familiar with statistics.</span></span> <span data-ttu-id="046dd-165">Selleks, et teave oleks kasulik, on oluline, et täiendav kontekst antaks koos täpsuse väärtusega.</span><span class="sxs-lookup"><span data-stu-id="046dd-165">However, to make the information useful, it's critical that additional context be provided together with the accuracy value.</span></span>

<span data-ttu-id="046dd-166">Makse prognoosimise stsenaariumi puhul saate seada eesmärgi ML-i mudeli jaoks, mis sisaldab erinevate makse käitumise tegureid.</span><span class="sxs-lookup"><span data-stu-id="046dd-166">For the payment prediction scenario, you can set a target for the ML model that includes factors in different payment behaviors.</span></span> <span data-ttu-id="046dd-167">Eesmärk on, et mudel peaks paranema pärast naiivset oletust, vähendades valede vastuste arvu vähemalt 50 protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="046dd-167">The target is that the model should improve upon a naïve guess by reducing the number of incorrect answers by at least 50 percent.</span></span> <span data-ttu-id="046dd-168">Teisisõnu on eesmärgiks täpsus, mis eraldab erineva täpsusega naiivse oletuse ja 100 protsenti.</span><span class="sxs-lookup"><span data-stu-id="046dd-168">In other words, you want a target accuracy that splits the different between the accuracy of a naïve guess and 100 percent.</span></span>

<span data-ttu-id="046dd-169">Järgmises tabelis summeeritakse see põhimõte selle teema segaduse maatriksite jaoks.</span><span class="sxs-lookup"><span data-stu-id="046dd-169">The following table summarizes this principle for the confusion matrices in this topic.</span></span>

| <span data-ttu-id="046dd-170">Mudel</span><span class="sxs-lookup"><span data-stu-id="046dd-170">Model</span></span>   | <span data-ttu-id="046dd-171">Naiivne oletus</span><span class="sxs-lookup"><span data-stu-id="046dd-171">Naïve guess</span></span> | <span data-ttu-id="046dd-172">Sihtkoht</span><span class="sxs-lookup"><span data-stu-id="046dd-172">Target</span></span> | <span data-ttu-id="046dd-173">Mudeli täpsus</span><span class="sxs-lookup"><span data-stu-id="046dd-173">Model accuracy</span></span> | <span data-ttu-id="046dd-174">Kas eesmärk on täidetud?</span><span class="sxs-lookup"><span data-stu-id="046dd-174">Is the goal met?</span></span>                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| <span data-ttu-id="046dd-175">Mudel 1</span><span class="sxs-lookup"><span data-stu-id="046dd-175">Model 1</span></span> | <span data-ttu-id="046dd-176">0.50</span><span class="sxs-lookup"><span data-stu-id="046dd-176">0.50</span></span>        | <span data-ttu-id="046dd-177">0.75</span><span class="sxs-lookup"><span data-stu-id="046dd-177">0.75</span></span>   | <span data-ttu-id="046dd-178">0.73</span><span class="sxs-lookup"><span data-stu-id="046dd-178">0.73</span></span>           | <span data-ttu-id="046dd-179">Peaaegu.</span><span class="sxs-lookup"><span data-stu-id="046dd-179">Almost.</span></span> <span data-ttu-id="046dd-180">See mudel parandab oluliselt oletust.</span><span class="sxs-lookup"><span data-stu-id="046dd-180">This model significantly improves upon the guess.</span></span> |
| <span data-ttu-id="046dd-181">Mudel 2</span><span class="sxs-lookup"><span data-stu-id="046dd-181">Model 2</span></span> | <span data-ttu-id="046dd-182">0.80</span><span class="sxs-lookup"><span data-stu-id="046dd-182">0.80</span></span>        | <span data-ttu-id="046dd-183">0.90</span><span class="sxs-lookup"><span data-stu-id="046dd-183">0.90</span></span>   | <span data-ttu-id="046dd-184">0.83</span><span class="sxs-lookup"><span data-stu-id="046dd-184">0.83</span></span>           | <span data-ttu-id="046dd-185">Nr</span><span class="sxs-lookup"><span data-stu-id="046dd-185">No.</span></span> <span data-ttu-id="046dd-186">Parandamine on nõutav.</span><span class="sxs-lookup"><span data-stu-id="046dd-186">Improvement is required.</span></span>                              |

## <a name="classification-f1-accuracy"></a><span data-ttu-id="046dd-187">Klassifikatsiooni F1 täpsus</span><span class="sxs-lookup"><span data-stu-id="046dd-187">Classification F1 accuracy</span></span>

<span data-ttu-id="046dd-188">Selle teema lõplik kasu on täpsem mõõtmise klassifikatsioon ML-i jõudluse kohta, mida tuntakse kui F1 täpsuse nime all.</span><span class="sxs-lookup"><span data-stu-id="046dd-188">The final consideration in this topic is a more advanced measure of classification ML performance that is known as F1 accuracy.</span></span>

<span data-ttu-id="046dd-189">Enne kui F1 täpsust saab määratleda, tuleb kehtestada kaks täiendavat mõõdikut: täpsus ja tagasikutsumine.</span><span class="sxs-lookup"><span data-stu-id="046dd-189">Before F1 accuracy can be defined, two additional metrics must be introduced: precision and recall.</span></span> <span data-ttu-id="046dd-190">Täpsus näitab, mitu positiivsete prognooside koguarvu on õigesti määratud.</span><span class="sxs-lookup"><span data-stu-id="046dd-190">Precision indicates how many of the total number of predictions that are specified as positive are correctly assigned.</span></span> <span data-ttu-id="046dd-191">Seda mõõdikut tuntakse ka positiivse prognoositava väärtusena.</span><span class="sxs-lookup"><span data-stu-id="046dd-191">This metric is also known as the positive predictive value.</span></span> <span data-ttu-id="046dd-192">Tagasikutsumine on tegelike positiivsete juhtumite koguarv, mida ennustati õigesti.</span><span class="sxs-lookup"><span data-stu-id="046dd-192">Recall is the total number of the actual positive cases that were predicted correctly.</span></span> <span data-ttu-id="046dd-193">Seda mõõdikut nimetatakse ka tundlikkuseks.</span><span class="sxs-lookup"><span data-stu-id="046dd-193">This metric is also known as sensitivity.</span></span>

<span data-ttu-id="046dd-194">[![Tegelikud tulemused vs valed tulemused](./media/tn-fn.png)](./media/tn-fn.png)</span><span class="sxs-lookup"><span data-stu-id="046dd-194">[![True results vs. false results](./media/tn-fn.png)](./media/tn-fn.png)</span></span>

<span data-ttu-id="046dd-195">Eelmise illustratsiooni segiajamise maatriksis arvutatakse need mõõdikud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="046dd-195">In the confusion matrix in the preceding illustration, these metrics are calculated in the following way:</span></span>

- <span data-ttu-id="046dd-196">Täpsus = TP ÷ (TP + FP)</span><span class="sxs-lookup"><span data-stu-id="046dd-196">Precision = TP ÷ (TP + FP)</span></span>
- <span data-ttu-id="046dd-197">Tagasikutsumine = TP ÷ (TP + FN)</span><span class="sxs-lookup"><span data-stu-id="046dd-197">Recall = TP ÷ (TP + FN)</span></span>

<span data-ttu-id="046dd-198">F1 mõõt ühendab täpsust ja tagasikutsumist.</span><span class="sxs-lookup"><span data-stu-id="046dd-198">The F1 measure combines precision and recall.</span></span> <span data-ttu-id="046dd-199">Tulemuseks on kahe väärtuse harmooniline keskväärtus.</span><span class="sxs-lookup"><span data-stu-id="046dd-199">The result is the harmonic mean of the two values.</span></span> <span data-ttu-id="046dd-200">See arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="046dd-200">It's calculated in the following way:</span></span>

- <span data-ttu-id="046dd-201">F1 = 2 × (täpsus × tagasikutsumine) ÷ (täpsus + tagasikutsumine)</span><span class="sxs-lookup"><span data-stu-id="046dd-201">F1 = 2 × (Precision × Recall) ÷ (Precision + Recall)</span></span>

<span data-ttu-id="046dd-202">Vaatame konkreetset näidet.</span><span class="sxs-lookup"><span data-stu-id="046dd-202">Let's look at a concrete example.</span></span> <span data-ttu-id="046dd-203">Selle teema alguses oli näide mudelist, mis ennustas, kas loom on koer või kass.</span><span class="sxs-lookup"><span data-stu-id="046dd-203">Earlier in this topic, there was an example of a model that predicted whether an animal was a dog or a cat.</span></span> <span data-ttu-id="046dd-204">Illustratsiooni korratakse siin.</span><span class="sxs-lookup"><span data-stu-id="046dd-204">The illustration is repeated here.</span></span>

<span data-ttu-id="046dd-205">[![Liikide prognoosi näide (korduv)](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="046dd-205">[![Species prediction example (repeated)](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)</span></span>

<span data-ttu-id="046dd-206">Siin on tulemused, kui positiivse vastusena kasutatakse valikut „koer”.</span><span class="sxs-lookup"><span data-stu-id="046dd-206">Here are the results if "Dog" is used as the positive answer.</span></span>

- <span data-ttu-id="046dd-207">Täpsis = 24 ÷ (24 + 2) = 0,9231</span><span class="sxs-lookup"><span data-stu-id="046dd-207">Precision = 24 ÷ (24 + 2) = 0.9231</span></span>
- <span data-ttu-id="046dd-208">Tagasikutsumine = 24 ÷ (24 + 6) = 0,8</span><span class="sxs-lookup"><span data-stu-id="046dd-208">Recall = 24 ÷ (24 + 6) = 0.8</span></span>
- <span data-ttu-id="046dd-209">F1 = 2 × (0,9231 × 0,8) ÷ (0,9231 + 0,8) = 0,8572</span><span class="sxs-lookup"><span data-stu-id="046dd-209">F1 = 2 × (0.9231 × 0.8) ÷ (0.9231 + 0.8) = 0.8572</span></span>

<span data-ttu-id="046dd-210">Nagu näete, on F1 väärtus täpsuse ja tagasikutsumise väärtuste vahel.</span><span class="sxs-lookup"><span data-stu-id="046dd-210">As you can see, the F1 value is between the values for precision and recall.</span></span>

<span data-ttu-id="046dd-211">Kuigi F1 täpsust ei ole nii lihtne mõista, lisab see nüansse täpsuse üldise täpsuse numbrile.</span><span class="sxs-lookup"><span data-stu-id="046dd-211">Although F1 accuracy isn't as easy to understand, it adds nuance to the basic accuracy number.</span></span> <span data-ttu-id="046dd-212">Samuti võib see aidata tasakaalustamata andmekogumite puhul, kuna kuvatakse järgmine arutelu.</span><span class="sxs-lookup"><span data-stu-id="046dd-212">It can also help with unbalanced datasets, as the following discussion will show.</span></span>

<span data-ttu-id="046dd-213">Selle teema jaotises [Mudeli täpsus](#model-accuracy) võrreldi järgmisi kahte segiajamise maatriksit.</span><span class="sxs-lookup"><span data-stu-id="046dd-213">The [Model accuracy](#model-accuracy) section of this topic compared the following two confusion matrices.</span></span> <span data-ttu-id="046dd-214">Kuigi esimesel mudelil oli madalam täpsus, peeti seda kasulikumaks mudeliks, sest see näitas suuremat paranemist, kui õigeaegselt tasumine.</span><span class="sxs-lookup"><span data-stu-id="046dd-214">Even though the first model had lower accuracy, it was deemed a more useful model because it showed more improvement than the default guess of an on-time payment.</span></span>

![Makse ennustus vs. tegelike näide](media/payment-prediction-matrix.png)

![Makseprognoosi näide suurema valimiga (korduv)](media/payment-prediction-matrix-2.png)

<span data-ttu-id="046dd-217">Vaatame, kuidas neid kahte mudelit võrreldakse, kui kasutatakse F1 skoori.</span><span class="sxs-lookup"><span data-stu-id="046dd-217">Let's see how these two models compare when the F1 score is used.</span></span> <span data-ttu-id="046dd-218">F1 skoori koefitsiendi täpsusega ja tagasikutsumisega on iga oleku jaoks ja F1 makro arvutamine seejärel keskmiselt F1 skoor kõikide olekute üleselt, et määrata üldine F1 skoor.</span><span class="sxs-lookup"><span data-stu-id="046dd-218">The F1 score factors in precision and recall for each state, and the F1 macro calculation then averages the F1 score across the states to determine an overall F1 score.</span></span> <span data-ttu-id="046dd-219">On ka teisi F1 variante, kuid suurem huvi on kasutada makro versiooni, arvestades kõigi kolme oleku võrdset kaalumist.</span><span class="sxs-lookup"><span data-stu-id="046dd-219">There are other F1 variants, but it's of greater interest to consider the macro version, given the equal consideration that is given to all three states.</span></span>

<span data-ttu-id="046dd-220">Arvutuste lihtsustamiseks ehitati valimi massiivid, et sobitada tegelike ja prognoositavate väärtustega.</span><span class="sxs-lookup"><span data-stu-id="046dd-220">To simplify the calculations, sample arrays were built to match the actual and predicted values.</span></span> <span data-ttu-id="046dd-221">Need massiivid kasutasid Pythonis sklearni mõõdikute teeki, et arvutada väärtused.</span><span class="sxs-lookup"><span data-stu-id="046dd-221">These arrays used sklearn's metrics library in Python to calculate the values.</span></span> <span data-ttu-id="046dd-222">Tulemus on järgmine.</span><span class="sxs-lookup"><span data-stu-id="046dd-222">Here is the result.</span></span>

| <span data-ttu-id="046dd-223">Mudel</span><span class="sxs-lookup"><span data-stu-id="046dd-223">Model</span></span>   | <span data-ttu-id="046dd-224">Naiivne oletus</span><span class="sxs-lookup"><span data-stu-id="046dd-224">Naive guess</span></span> | <span data-ttu-id="046dd-225">Täpsus</span><span class="sxs-lookup"><span data-stu-id="046dd-225">Accuracy</span></span> | <span data-ttu-id="046dd-226">F1 makro</span><span class="sxs-lookup"><span data-stu-id="046dd-226">F1 macro</span></span> |
|---------|-------------|----------|----------|
| <span data-ttu-id="046dd-227">Mudel 1</span><span class="sxs-lookup"><span data-stu-id="046dd-227">Model 1</span></span> | <span data-ttu-id="046dd-228">0.5</span><span class="sxs-lookup"><span data-stu-id="046dd-228">0.5</span></span>         | <span data-ttu-id="046dd-229">0.73</span><span class="sxs-lookup"><span data-stu-id="046dd-229">0.73</span></span>     | <span data-ttu-id="046dd-230">0.67</span><span class="sxs-lookup"><span data-stu-id="046dd-230">0.67</span></span>     |
| <span data-ttu-id="046dd-231">Mudel 2</span><span class="sxs-lookup"><span data-stu-id="046dd-231">Model 2</span></span> | <span data-ttu-id="046dd-232">0.80</span><span class="sxs-lookup"><span data-stu-id="046dd-232">0.80</span></span>        | <span data-ttu-id="046dd-233">0.83</span><span class="sxs-lookup"><span data-stu-id="046dd-233">0.83</span></span>     | <span data-ttu-id="046dd-234">0.66</span><span class="sxs-lookup"><span data-stu-id="046dd-234">0.66</span></span>     |

<span data-ttu-id="046dd-235">Üksikasjalikumat teavet selle kalkulatsiooni töötamise kohta leiate sklearni mõõdikute klassifikatsiooni aruandest mudelile 1.</span><span class="sxs-lookup"><span data-stu-id="046dd-235">For more detail about how this calculation works, here is the sklearn.metrics classification report for model 1.</span></span> <span data-ttu-id="046dd-236">Kolm olekut „õigel ajal”, „hilja” ja „väga hilja” tähistavad ridu, mis on vastavalt märgistatud kui 1, 2 ja 3.</span><span class="sxs-lookup"><span data-stu-id="046dd-236">The three states, "On time," "Late," and "Very late," are represented by the rows that are labeled 1, 2, and 3, respectively.</span></span> <span data-ttu-id="046dd-237">Makro keskmine on ainult veeru F1 skoori keskmine.</span><span class="sxs-lookup"><span data-stu-id="046dd-237">The macro average is just the average of the "f1-score" column.</span></span>

|           | <span data-ttu-id="046dd-238">täpsus</span><span class="sxs-lookup"><span data-stu-id="046dd-238">precision</span></span> | <span data-ttu-id="046dd-239">tagasikutsumine</span><span class="sxs-lookup"><span data-stu-id="046dd-239">recall</span></span>   | <span data-ttu-id="046dd-240">f1-score</span><span class="sxs-lookup"><span data-stu-id="046dd-240">f1-score</span></span> |
|-----------|-----------|----------|----------|
| <span data-ttu-id="046dd-241">**1**</span><span class="sxs-lookup"><span data-stu-id="046dd-241">**1**</span></span>     | <span data-ttu-id="046dd-242">0.83</span><span class="sxs-lookup"><span data-stu-id="046dd-242">0.83</span></span>      | <span data-ttu-id="046dd-243">0.80</span><span class="sxs-lookup"><span data-stu-id="046dd-243">0.80</span></span>     | <span data-ttu-id="046dd-244">0.82</span><span class="sxs-lookup"><span data-stu-id="046dd-244">0.82</span></span>     |
| <span data-ttu-id="046dd-245">**2**</span><span class="sxs-lookup"><span data-stu-id="046dd-245">**2**</span></span>     | <span data-ttu-id="046dd-246">0.68</span><span class="sxs-lookup"><span data-stu-id="046dd-246">0.68</span></span>      | <span data-ttu-id="046dd-247">0.71</span><span class="sxs-lookup"><span data-stu-id="046dd-247">0.71</span></span>     | <span data-ttu-id="046dd-248">0.69</span><span class="sxs-lookup"><span data-stu-id="046dd-248">0.69</span></span>     |
| <span data-ttu-id="046dd-249">**3**</span><span class="sxs-lookup"><span data-stu-id="046dd-249">**3**</span></span>     | <span data-ttu-id="046dd-250">0.50</span><span class="sxs-lookup"><span data-stu-id="046dd-250">0.50</span></span>      | <span data-ttu-id="046dd-251">0.50</span><span class="sxs-lookup"><span data-stu-id="046dd-251">0.50</span></span>     | <span data-ttu-id="046dd-252">0.50</span><span class="sxs-lookup"><span data-stu-id="046dd-252">0.50</span></span>     |

<span data-ttu-id="046dd-253">Need tulemused näitavad, et kahel mudelil on peaaegu identne F1 makro täpsuse punktisumma.</span><span class="sxs-lookup"><span data-stu-id="046dd-253">As these results show, the two models have nearly identical F1 macro accuracy scores.</span></span> <span data-ttu-id="046dd-254">Selles ja paljudel muudel juhtudel annab F1 täpsus mudeli võimekuse parema näidiku.</span><span class="sxs-lookup"><span data-stu-id="046dd-254">In this and many other cases, F1 accuracy provides a better indicator of a model's capability.</span></span> <span data-ttu-id="046dd-255">Täpsuse puhul nõuab tulemuste tõlgendamine, et mõistaksite, millega tuleb mudelis arvestada.</span><span class="sxs-lookup"><span data-stu-id="046dd-255">As for accuracy, interpretation of the results requires that you understand what is most important to consider in the model.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="046dd-256">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="046dd-256">Privacy notice</span></span>
<span data-ttu-id="046dd-257">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="046dd-257">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]