---
title: Keskmine jooksev omahind
description: Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Ent enne lao sulgemise käitamist arvutab süsteem jooksva keskmise omahinna, mida tavaliselt kasutatakse väljaminekukannete sisestamisel.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092185"
---
# <a name="running-average-cost-price"></a>Keskmine jooksev omahind

[!include [banner](../includes/banner.md)]

Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Ent enne lao sulgemise käitamist arvutab süsteem jooksva keskmise omahinna, mida tavaliselt kasutatakse väljaminekukannete sisestamisel.

Süsteem hindab seda kauba keskmist jooksevomahinda, kasutades järgmist valemit.

Eeldatav hind = (füüsiline summa + rahaline summa) ÷ (füüsiline kogus + rahaline kogus)

## <a name="default-item-cost"></a>Kauba vaikekulu

Väljastatud toote üksuse vaikemaksumuse saab konfigureerida kahel viisil **lehel Väljastatud toote üksikasjad**.

- Standardomahinna loomiseks valige **toimingupaani vahekaardi Kulude haldamine** jaotises Seadistamine **väärtus** Kauba **hind**. Kui kasutate seda meetodit, peate kasutama standardset kuluarvestusversiooni ja kulu peab olema aktiveeritud.
- Määratlege vabastatud toote kauba vaike omahind, sisestades väärtuse **kiirkaardi Halda kulusid** väljale **Hind**.

Lisaks hinna sisestamise või loomisele saate valida **lehe Väljastatud toote üksikasjad** kiirkaardil **Halda kulusid** märkeruut Kasuta uusimat **omahinda**. Sellisel juhul uuendab **süsteem finantsvärskenduse konteerimisel automaatselt välja Hind**. Näiteks kui konteerite ostutellimuse arve, seatakse väli selle arve ostuhinnale.

Kui teil on aktiivses kuluversioonis omahind ja sisestate hinna kiirkaardile **Halda kulusid**, kasutab süsteem aktiivse kuluversiooni hinda enne, kui ta kasutab kiirkaardil **Kulude** haldamine määratletud hinda.

## <a name="using-the-running-average-cost-price"></a>Jooksva keskmise omahinna kasutamine

Järgnev tabel näitab, millal süsteem sisestab laokanded, kasutades jooksvat keskmist omahinda, ja millal see kasutab hoopis kauba põhikirjes määratud omahinda.

| Tingimus | Süsteem kasutab hinnangulist jooksvat keskmist omahinda | Süsteem kasutab kauba vaikemaksuhindu. |
| --- | --- | --- |
| Nii lugeja\* kui ka nimetaja\*\* on positiivsed. | Jah | Nr |
| Lugeja\*, nimetaja\*\* või mõlemad on negatiivsed. | Ei | Jah |
| Nimetaja\*\* on 0 (null). | Ei | Jah |

\* Lugeja = (füüsiline summa + rahaline summa)  
\*\* Nimetaja = (füüsiline kogus + rahaline kogus)

> [!NOTE]
> **Kui kauba puhul pole valitud valikut Kaasa füüsiline väärtus**, kasutab süsteem nii füüsilise kui ka füüsilise koguse jaoks 0 (null). Lisateavet selle valiku kohta leiate jaotisest [Füüsilise väärtuse kaasamine](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnakujunduse amplifikatsiooni vältimine

Harvadel juhtudel kujundab süsteem mitme väljamineku hinna, enne kui hinna aluseks on piisavalt sissetulekuid. See stsenaarium võib põhjustada ülemäära paisutatud jooksva keskmise omahinna hinnangud. Kuid on olemas võimalusi, kuidas hinna amplifikatsiooni vältida või selle ilmnemisel selle mõju vähendada.

**Stsenaarium:** kauba puhul, mille olete valinud suvandi **Kaasa füüsiline väärtus**, ilmnevad järgmised kanded.

1. Saate rahaliselt koguse 100 hinnaga USD 100.00.
2. Väljastate rahaliselt koguse 200.
3. Saate füüsiliselt koguse 101 hinnaga USD 202.00.

Kui uurite kauba eeldatavat jooksvat keskmist omahinda, eeldate omahinda USD 1.51. Selle asemel leiate hinnangulise jooksva keskmise USD 102.00, mis põhineb järgmisel valemil.

Eeldatav hind = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

See hinnakujunduse võimendamine toimub seetõttu, et kui 200 üksust väljastatakse rahaliselt 2. etapis, peab süsteem enne vastavate sissetulekute saamist maksma 100 kaupa. Selline olukord põhjustab negatiivse laovaru. Seejärel hindab süsteem ühikuhinnaks USD 1.00, nagu võite arvata. Kuid kui vastavad 100 sissetulekut saabuvad, on nende iga ühiku hind USD 2.00.

> [!NOTE]
> Kuigi väljaminek loob negatiivse varu, on varud väljaminekhinna arvutamisel positiivsed. Seetõttu kasutataksegi kauba põhikirje hinna asemel jooksvat keskmist omahinda. Selles punktis on süsteemil laoväärtuse tasakaalustus USD 100.00. Kuigi see nihe oli üles ehitatud üle 100 tükki, kus oli ühiku nihe USD 1.00 iga, siis nüüd on ainult üks tükk laos. Seega eraldatakse tasakaalustus USD 100.00 sellele ühele ühikule. Tulemuseks on liigselt paisutatud eeldatav omahind.
>
> Võrdluseks pange tähele, et kui stsenaariumis pööratakse ümber 2. ja 3. osa, väljastatakse 200 kirjet ühikuhinnaga USD 1.51 ja üks tükk jääb ühikuhinnale USD 1.51. Kuna selline hinnakujunduse amplifikatsiooni stsenaarium võib tekkida negatiivse laovaru puhul, on seda raske vältida järgmistel juhtudel.
>
> - Peate hinnanguliselt määrama väljalaske hinnad vaba väärtuse ja koguse kohta.
> - Peate korrigeerima väljaminekute ja sissetulekute vaba väärtust ja kogust.
> - Teie äritegevuse mudel võimaldab saata välja või hinnata rohkem tooteüksusi, kui teil on.
> - Peate aktsepteerima mis tahes sissetuleku väärtuse ja koguse, mis teile edastatakse.

Ent kui teie äritegevuse mudel lubab, võivad järgmised praktikad aidata teil vältida negatiivseid koguseid, mis muudavad hinnakujunduse amplifikatsiooni stsenaariumi võimalikuks.

- Kui valite kauba suvandi **Kaasa füüsiline väärtus**, tühjendage **lehel Kauba mudeligrupid** ruut **Füüsiline negatiivne varu**.
- Kui te **ei** tee kauba puhul valikut **Kaasa füüsiline väärtus**, eemaldage valik **Negatiivne rahaline laovaru** lehel **Kauba mudeligrupid**.

Lisaks arvestage, et maksimaalne vastaskonto teie füüsilises laoväärtuses on piiratud füüsiliste kannete arvuga ja füüsiliste ja rahaliste hindade vahega. Eeldusel, et kõik füüsilised kanded lõpuks rahaliselt värskendatakse, ei saa füüsiline väärtus äärmuslikele tasanditele tõusta. Lõpuks arvestage, et amplifikatsiooniefekt väheneb oluliselt, kui akumuleeritud tasakaalustus ulatub üle mitme, mitte ainult ühe vaba kaubaühiku.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Vältige null omahinna vältimist probleemide korral

**Kui lehel Kauba mudeligrupp** pole valitud **valikut Kaasa füüsiline väärtus**, võib varude väljaminekel olla nullomahind, kui varudes pole finantsiliselt uuendatud sissetulekuid. Selle stsenaariumi vältimiseks kaaluge järgmisi võimalusi.

- **Valige lehel Kauba mudelirühm** suvand **Kaasa füüsiline väärtus**. See suvand takistab probleemi nullmaksumuse hinda tingimusel, et kviitungit uuendatakse füüsiliselt. Kui te ei luba negatiivset füüsilist inventuuri, arvutavad väljaminevad füüsiliselt värskendatud kannete jooksva keskmise.
- Looge kauba omahind vaikimisi, aktiveerides standardomahinnaga kuluversiooni, või sisestage hind lehe Väljastatud toote üksikasjad **kiirkaardile** **Kulude** haldamine. See suvand on parim, kui **lehel Kauba mudelirühm** pole valitud suvandit Kaasa füüsiline väärtus **, kuna süsteemil** on alati varuhind, mida kasutada.
- **Valige lehe Väljastatud toote üksikasjad** kiirkaardil **Kulude** **haldamine suvand Kasuta uusimat omahinda**. See suvand hoiab **välja Hind** ajakohasena iga kord, kui kviitungit rahaliselt värskendate. Kui valite selle suvandi, kuid te ei sisesta vaikehinda ega aktiveeri kulu standardne kuluversioon, võib teil siiski olla probleemi nullkulu.

Kui teil on nullkuluga väljalaskekandeid, *parandab varude sulgemine ja korrigeerimisprotsess* omahinna, luues pärast sissetulekute finantsilist uuendamist korrigeerimise. Pidage meeles, et finantsperiood, mil see värskendus toimub, võib erineda finantsperioodist, mil kaubad füüsiliselt vastu võeti või välja anti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
