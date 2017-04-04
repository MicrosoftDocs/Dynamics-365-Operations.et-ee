---
title: Keskmine jooksev omahind
description: "Varude kohtuasi settib väljaminekukannete sissetulekukanded, valitud kauba kauba tootemudeli grupi varude hindamise meetodi. Enne varude lähedal arvutab süsteem töötab keskmise omahinna, mida kasutatakse tavaliselt probleemi kannete sisestamisel."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Keskmine jooksev omahind

Varude kohtuasi settib väljaminekukannete sissetulekukanded, valitud kauba kauba tootemudeli grupi varude hindamise meetodi. Enne varude lähedal arvutab süsteem töötab keskmise omahinna, mida kasutatakse tavaliselt probleemi kannete sisestamisel.

Süsteem arvutab see töötab üksuse jaoks järgmise valemi abil: arvestuslik hind = (füüsilise summa + summat) ÷ (füüsiline kogus + rahaline koguse)

## <a name="using-the-running-average-cost-price"></a>Jooksva keskmise omahinna kasutamine
Järgmine tabel näitab, millal süsteemi ametikohad laokannete abil töötab keskmise omahinna ja kuna ta kasutab määratletud kauba põhikirje asemel omahind.

| Tingimus                                               | Süsteem kasutab hinnanguliselt töötab keskmise omahinna | Süsteem kasutab määratletud kapten kauba omahind |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Nii lugeja\* ja nimetaja\*\* on positiivne.  | Jah                                                      | Ei                                                                |
| Lugeja\*, nimetaja\*\*, või mõlemad on negatiivne. | Ei                                                       | Jah                                                               |
| Nimetaja\*\* on 0 (null).                        | Ei                                                       | Jah                                                               |

\*Lugeja (füüsilise summa + rahaline summa) = \*\*nimetaja = (füüsiline kogus + rahaline koguse) **Märkus:** kui ka **kaasa füüsiline väärtus** suvand ei ole valitud üksuse, kasutab süsteem füüsilise suuruse ja füüsiline kogus 0 (null). Lisateavet selle valiku kohta leiate jaotisest [Füüsilise väärtuse kaasamine](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnakujunduse amplifikatsiooni vältimine
Harvadel juhtudel süsteemi hinnad mitmeid küsimusi enne, kui see on piisavalt sissetulekuid aluseks hind. See stsenaarium võib põhjustada ülemäära paisutatud jooksva keskmise omahinna hinnangud. Kuid on olemas võimalusi, kuidas hinna amplifikatsiooni vältida või selle ilmnemisel selle mõju vähendada. **Stsenaarium** Kauba puhul, millele olete teinud valiku **Kaasa füüsiline väärtus**, toimuvad järgmised kanded.

1.  Saate rahaliselt koguse 100 hinnaga USD 100.00.
2.  Väljastate rahaliselt koguse 200.
3.  Saate füüsiliselt koguse 101 hinnaga USD 202.00.

Kui uurite kauba eeldatavat jooksvat keskmist omahinda, eeldate omahinda USD 1.51. Selle asemel leiate hinnanguliselt töötab Keskmine USD 102.00, mis põhineb järgmise valemi abil: arvestuslik hind = \[202 + (– 100)\] ÷ \[101 + (– 100)\] = 102 ÷ 1 = 102 hinnakujunduse amplifikatsiooni ilmneb seetõttu väljaandmisel 200 nimetuse rahaliselt juhises 2 süsteemi must hind 100 kaupade enne vastavaid tulusid. Selline olukord põhjustab negatiivse laovaru. Süsteem hindab seejärel ühikuhind USD 1.00, nagu me oodata. Kuid kui vastavad 100 sissetulekut saabuvad, on nende iga ühiku hind USD 2.00. **Märkus:** kuigi väljaminekud tekitavad negatiivse laovaru, on väljastamise hinna arvutamisel laovaru positiivne. Seetõttu kasutataksegi kauba põhikirje hinna asemel jooksvat keskmist omahinda. Sel hetkel süsteem on varude väärtuse nihet USD 100.00. Kuigi see tasakaalustus kogunes 100 ühikult, kui iga ühiku tasakaalustus oli USD 1.00, on meil nüüd laos üks ühik. Seega eraldatakse tasakaalustus USD 100.00 sellele ühele ühikule. Tulemuseks on liigselt paisutatud eeldatav omahind. **Märkus:** võrdluseks pange tähele, et kui sammud 2 ja 3 ülaltoodud näites tagasi võtta, antakse välja 200 üksust ühikuhinnaga USD 1.51 ja üks tooteühik jääb ühiku hinnaga USD 1.51. Kuna selline hinnakujunduse amplifikatsiooni stsenaarium võib tekkida negatiivse laovaru puhul, on seda raske vältida järgmistel juhtudel.

-   Peate hinnanguliselt määrama väljalaske hinnad vaba väärtuse ja koguse kohta.
-   Peate korrigeerima väljaminekute ja sissetulekute vaba väärtust ja kogust.
-   Teie äritegevuse mudel võimaldab saata välja või hinnata rohkem tooteüksusi, kui teil on.
-   Peate aktsepteerima mis tahes sissetuleku väärtuse ja koguse, mis teile edastatakse.

Ent kui teie äritegevuse mudel lubab, võivad järgmised praktikad aidata teil vältida negatiivseid koguseid, mis muudavad hinnakujunduse amplifikatsiooni stsenaariumi võimalikuks.

-   Kui teete kauba puhul valiku **Kaasa füüsiline väärtus**, tühjendage märkeruut **Füüsiline negatiivne laovaru** lehel **Kauba mudeligrupid**.
-   Kui te *ei* tee kauba puhul valikut **Kaasa füüsiline väärtus**, eemaldage valik **Negatiivne rahaline laovaru** lehel **Kauba mudeligrupid**.

Lisaks arvestage, et maksimaalne vastaskonto teie füüsilises laoväärtuses on piiratud füüsiliste kannete arvuga ja füüsiliste ja rahaliste hindade vahega. Eeldusel, et kõik füüsilised kanded lõpuks rahaliselt värskendatakse, ei saa füüsiline väärtus äärmuslikele tasanditele tõusta. Lõpuks arvestage, et amplifikatsiooniefekt väheneb oluliselt, kui akumuleeritud tasakaalustus ulatub üle mitme, mitte ainult ühe vaba kaubaühiku.


