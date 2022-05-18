---
title: Keskmine jooksev omahind
description: Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Ent enne lao sulgemise käitamist arvutab süsteem jooksva keskmise omahinna, mida tavaliselt kasutatakse väljaminekukannete sisestamisel.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672174"
---
# <a name="running-average-cost-price"></a>Keskmine jooksev omahind

[!include [banner](../includes/banner.md)]

Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Ent enne lao sulgemise käitamist arvutab süsteem jooksva keskmise omahinna, mida tavaliselt kasutatakse väljaminekukannete sisestamisel.

Süsteem hindab seda kauba keskmist jooksevomahinda, kasutades järgmist valemit.

Eeldatav hind = (füüsiline summa + rahaline summa) ÷ (füüsiline kogus + rahaline kogus)

## <a name="default-item-cost"></a>Kauba vaikekulu

Väljastatud toote kauba vaikekulu saab konfigureerida ühel kahest väljastatud toote üksikasjade lehel olevast **viisist**:

- Looge standardne kulu, **valides tegevuspaani** **vahekaardi** Halda kulusid **grupis** Seadista üksuse hind. Kui kasutate seda meetodit, peate kasutama standardset kuluarvestuse versiooni ja kulu tuleb aktiveerida.
- Määrake väljastatud toote vaikimisi kauba omahind, sisestades **väärtuse** väljale Hind kiirkaardil **Kulude** haldamine.

Lisaks hinna sisestamisele või loomisele **saate** **·** **märkeruudu Kasuta uusimat omahinda lehel Väljastatud toote üksikasjade kiirkaardil Kulude haldamine.** Sel juhul uuendab süsteem välja Hind finantsvärskenduse **sisestamisel** automaatselt. Näiteks kui sisestate ostutellimuse arve, seatakse väljale selle arve ostuhind.

Kui teil on **kuluhind** aktiivses kuluversioonis ja te sisestate hinna kiirkaardile Kulude haldamine, kasutab süsteem hinda aktiivsest kuluversioonist, enne kui see kasutab hinda, mis on **määratletud** kiirkaardil Kulude haldamine.

## <a name="using-the-running-average-cost-price"></a>Jooksva keskmise omahinna kasutamine

Järgnev tabel näitab, millal süsteem sisestab laokanded, kasutades jooksvat keskmist omahinda, ja millal see kasutab hoopis kauba põhikirjes määratud omahinda.

| Tingimus | Süsteem kasutab hinnangulist jooksvat keskmist omahinda | Süsteem kasutab kauba vaikehinda |
| --- | --- | --- |
| Nii lugeja\* kui ka nimetaja\*\* on positiivsed. | Jah | Nr |
| Lugeja\*, nimetaja\*\* või mõlemad on negatiivsed. | Ei | Jah |
| Nimetaja\*\* on 0 (null). | Ei | Jah |

\* Lugeja = (füüsiline summa + rahaline summa)  
\*\* Nimetaja = (füüsiline kogus + rahaline kogus)

> [!NOTE]
> Kui üksuse **puhul ei ole** valitud valikut Kaasa füüsiline väärtus, kasutab süsteem 0 (null) nii füüsilise summa kui füüsilise koguse puhul. Lisateavet selle valiku kohta leiate jaotisest [Füüsilise väärtuse kaasamine](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnakujunduse amplifikatsiooni vältimine

Harvadel juhtudel kujundab süsteem mitme väljamineku hinna, enne kui hinna aluseks on piisavalt sissetulekuid. See stsenaarium võib põhjustada ülemäära paisutatud jooksva keskmise omahinna hinnangud. Kuid on olemas võimalusi, kuidas hinna amplifikatsiooni vältida või selle ilmnemisel selle mõju vähendada.

**Stsenaarium:** järgmised kanded ilmnevad kauba puhul, mille jaoks **olete valinud suvandi Kaasa füüsiline** väärtus:

1. Saate rahaliselt koguse 100 hinnaga USD 100.00.
2. Väljastate rahaliselt koguse 200.
3. Saate füüsiliselt koguse 101 hinnaga USD 202.00.

Kui uurite kauba eeldatavat jooksvat keskmist omahinda, eeldate omahinda USD 1.51. Selle asemel leiate hinnangulise jooksva USD 102.00, mis põhineb järgmisel valemil:

Hinnanguline hind = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Selline hinnakujunduse amplifikatsioon leiab aset, kuna kui 200 üksust väljastatakse finantsiliselt sammus 2, peab süsteem enne, kui on saanud mis tahes vastavaid sissetulekuid, hinnata 100 üksust. Selline olukord põhjustab negatiivse laovaru. Süsteem hindab siis hinnangulist ühikuhinda USD 1.00, nagu te võite eeldada. Kuid kui vastavad 100 sissetulekut saabuvad, on nende iga ühiku hind USD 2.00.

> [!NOTE]
> Ehkki väljaminek loob negatiivse laovaru, on laovaru väljamineuhinna arvutamisel positiivne. Seetõttu kasutataksegi kauba põhikirje hinna asemel jooksvat keskmist omahinda. Selles punktis on süsteemil laoväärtuse tasakaalustus USD 100.00. Ehkki see vastaskonto ehitati üle 100 tüki, kus ühikute vastaskonto oli USD 1.00 igaüks, on teil laos nüüd ainult üks tükike. Seega eraldatakse tasakaalustus USD 100.00 sellele ühele ühikule. Tulemuseks on liigselt paisutatud eeldatav omahind.
>
> Võrdluseks pange tähele, et kui stsenaariumis tühistatakse 2. ja 3. etapp, väljastatakse 200 kaupa USD 1.51 ühiku hinnaga ja üks tüki jääb ühiku hinnaks, mis USD 1.51. Kuna selline hinnakujunduse amplifikatsiooni stsenaarium võib tekkida negatiivse laovaru puhul, on seda raske vältida järgmistel juhtudel.
>
> - Peate hinnanguliselt määrama väljalaske hinnad vaba väärtuse ja koguse kohta.
> - Peate korrigeerima väljaminekute ja sissetulekute vaba väärtust ja kogust.
> - Teie äritegevuse mudel võimaldab saata välja või hinnata rohkem tooteüksusi, kui teil on.
> - Peate aktsepteerima mis tahes sissetuleku väärtuse ja koguse, mis teile edastatakse.

Ent kui teie äritegevuse mudel lubab, võivad järgmised praktikad aidata teil vältida negatiivseid koguseid, mis muudavad hinnakujunduse amplifikatsiooni stsenaariumi võimalikuks.

- Kui valite kaubale **valiku** Kaasa füüsiline väärtus, tühjendage märkeruut **Füüsiline negatiivne** laovaru **kauba mudeligruppide lehel**.
- Kui te **ei** tee kauba puhul valikut **Kaasa füüsiline väärtus**, eemaldage valik **Negatiivne rahaline laovaru** lehel **Kauba mudeligrupid**.

Lisaks arvestage, et maksimaalne vastaskonto teie füüsilises laoväärtuses on piiratud füüsiliste kannete arvuga ja füüsiliste ja rahaliste hindade vahega. Eeldusel, et kõik füüsilised kanded lõpuks rahaliselt värskendatakse, ei saa füüsiline väärtus äärmuslikele tasanditele tõusta. Lõpuks arvestage, et amplifikatsiooniefekt väheneb oluliselt, kui akumuleeritud tasakaalustus ulatub üle mitme, mitte ainult ühe vaba kaubaühiku.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Vältige väljamineu puhul nullhinda

Kui kauba **mudeligrupi lehel** **pole** valitud valikut Kaasa füüsiline väärtus, võib lao väljaminek omahinnaks olla null, kui laos pole finantsiliselt värskendatud sissetulekuid. Selle stsenaariumi vältimiseks kaaluge järgmisi valikuid.

- Valige kauba **mudeligrupi lehel** suvand **Kaasa füüsiline** väärtus. See valik takistab nullhinna omahinda väljastamisel, eeldusel, et sissetulek on füüsiliselt uuendatud. Kui te ei luba negatiivset füüsilist laovaru, arvutavad väljaminek füüsiliselt värskendatud kannete jooksva keskmise.
- Looge kauba vaikekulu hind, aktiveerides standardkuluga kuluversiooni **või** **sisestage hind kiirkaardile Väljastatud toote üksikasjad.** See valik on parim, **kui kauba** mudeligrupi lehel ei ole valitud valikut Kaasa füüsiline väärtus, sest süsteemil on **alati** kasutamiseks varuhind.
- Valige suvand **Kasuta viimast omahinda** lehel **Väljastatud** toote üksikasjad kiirkaardil **Kulude** haldamine. See valik säilitab **välja** Hind aja aja järgi iga kord, kui värskendate sissetulekut finantsiliselt. Kui valite selle suvandi, kuid te ei sisesta vaikehinda ega aktiveeri kulu standardses kuluversioonis, võib teil väljastamisel olla nullkulu.

Kui teil on väljastuskandeid, mille maksumus on null, *parandab* lao sulgemise ja korrigeerimise protsess omahinda, luues korrektsiooni pärast sissetulekute finantsiliselt uuendamist. Pidage silmas, et finantsperiood, mil see värskendus toimub, võib finantsperioodist erineda, kui kaubad füüsiliselt sisse saadi või väljastati.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
