---
title: Keskmine jooksev omahind
description: "Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Ent enne lao sulgemise käitamist arvutab süsteem jooksva keskmise omahinna, mida tavaliselt kasutatakse väljaminekukannete sisestamisel."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a73ce12f1064c44b2af0fa4f33c63f1a6bddab89
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="running-average-cost-price"></a>Keskmine jooksev omahind

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Ent enne lao sulgemise käitamist arvutab süsteem jooksva keskmise omahinna, mida tavaliselt kasutatakse väljaminekukannete sisestamisel.

Süsteem hindab seda kauba keskmist jooksevomahinda, kasutades järgmist valemit. 

Eeldatav hind = (füüsiline summa + rahaline summa) ÷ (füüsiline kogus + rahaline kogus)

## <a name="using-the-running-average-cost-price"></a>Jooksva keskmise omahinna kasutamine
Järgnev tabel näitab, millal süsteem sisestab laokanded, kasutades jooksvat keskmist omahinda, ja millal see kasutab hoopis kauba põhikirjes määratud omahinda.

| Tingimus                                               | Süsteem kasutab hinnangulist jooksvat keskmist omahinda | Süsteem kasutab kauba põhikirjes määratud omahinda |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Nii lugeja\* kui ka nimetaja\*\* on positiivsed.  | Jah                                                      | Ei                                                                |
| Lugeja\*, nimetaja\*\* või mõlemad on negatiivsed. | Ei                                                       | Jah                                                               |
| Nimetaja\*\* on 0 (null).                        | Ei                                                       | Jah                                                               |

\* Lugeja = (füüsiline summa + rahaline summa) \*\* Nimetaja = (füüsiline kogus + rahaline kogus) 

**Märkus.** Kui valik **Kaasa füüsiline väärtus** pole kauba jaoks valitud, kasutab süsteem väärtust 0 (null) nii füüsilise summa kui ka füüsilise koguse puhul. Lisateavet selle valiku kohta leiate jaotisest [Füüsilise väärtuse kaasamine](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnakujunduse amplifikatsiooni vältimine
Harvadel juhtudel kujundab süsteem mitme väljamineku hinna, enne kui hinna aluseks on piisavalt sissetulekuid. See stsenaarium võib põhjustada ülemäära paisutatud jooksva keskmise omahinna hinnangud. Kuid on olemas võimalusi, kuidas hinna amplifikatsiooni vältida või selle ilmnemisel selle mõju vähendada. **Stsenaarium** Kauba puhul, millele olete teinud valiku **Kaasa füüsiline väärtus**, toimuvad järgmised kanded.

1.  Saate rahaliselt koguse 100 hinnaga USD 100.00.
2.  Väljastate rahaliselt koguse 200.
3.  Saate füüsiliselt koguse 101 hinnaga USD 202.00.

Kui uurite kauba eeldatavat jooksvat keskmist omahinda, eeldate omahinda USD 1.51. Selle asemel leiate hinnangulise jooksva keskmise USD 102.00, mis põhineb järgmisel valemil: hinnanguline hind = \[202 + (–100)]\] ÷ \[101 + (–100)\] = 102 ÷ 1 = 102 See hinnavõimendus toimub, kuna 200 üksuse väljastamisel rahaliselt sammus 2 peab süsteem määrama hinna 100 üksusele enne, kui on olemas vastavaid sissetulekuid. Selline olukord põhjustab negatiivse laovaru. Süsteem prognoosib siis ühiku hinnaks USD 1.00, nagu võib eeldada. Kuid kui vastavad 100 sissetulekut saabuvad, on nende iga ühiku hind USD 2.00. 

**Märkus:** kuigi väljaminekud tekitavad negatiivse laovaru, on väljastamise hinna arvutamisel laovaru positiivne. Seetõttu kasutataksegi kauba põhikirje hinna asemel jooksvat keskmist omahinda. Selles punktis on süsteemil laoväärtuse tasakaalustus USD 100.00. Kuigi see tasakaalustus kogunes 100 ühikult, kui iga ühiku tasakaalustus oli USD 1.00, on meil nüüd laos üks ühik. Seega eraldatakse tasakaalustus USD 100.00 sellele ühele ühikule. Tulemuseks on liigselt paisutatud eeldatav omahind. 

**Märkus:** võrdluseks pange tähele, et kui sammud 2 ja 3 ülaltoodud näites tagasi võtta, antakse välja 200 üksust ühikuhinnaga USD 1.51 ja üks tooteühik jääb ühiku hinnaga USD 1.51. Kuna selline hinnakujunduse amplifikatsiooni stsenaarium võib tekkida negatiivse laovaru puhul, on seda raske vältida järgmistel juhtudel.

-   Peate hinnanguliselt määrama väljalaske hinnad vaba väärtuse ja koguse kohta.
-   Peate korrigeerima väljaminekute ja sissetulekute vaba väärtust ja kogust.
-   Teie äritegevuse mudel võimaldab saata välja või hinnata rohkem tooteüksusi, kui teil on.
-   Peate aktsepteerima mis tahes sissetuleku väärtuse ja koguse, mis teile edastatakse.

Ent kui teie äritegevuse mudel lubab, võivad järgmised praktikad aidata teil vältida negatiivseid koguseid, mis muudavad hinnakujunduse amplifikatsiooni stsenaariumi võimalikuks.

-   Kui teete kauba puhul valiku **Kaasa füüsiline väärtus**, tühjendage märkeruut **Füüsiline negatiivne laovaru** lehel **Kauba mudeligrupid**.
-   Kui te *ei* tee kauba puhul valikut **Kaasa füüsiline väärtus**, eemaldage valik **Negatiivne rahaline laovaru** lehel **Kauba mudeligrupid**.

Lisaks arvestage, et maksimaalne vastaskonto teie füüsilises laoväärtuses on piiratud füüsiliste kannete arvuga ja füüsiliste ja rahaliste hindade vahega. Eeldusel, et kõik füüsilised kanded lõpuks rahaliselt värskendatakse, ei saa füüsiline väärtus äärmuslikele tasanditele tõusta. Lõpuks arvestage, et amplifikatsiooniefekt väheneb oluliselt, kui akumuleeritud tasakaalustus ulatub üle mitme, mitte ainult ühe vaba kaubaühiku.




