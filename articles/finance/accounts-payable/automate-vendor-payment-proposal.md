---
title: Hankija maksesoovituste automatiseerimine
description: Selles teemas selgitatakse, kuidas korduva graafiku alusel hankijatele maksvad organisatsioonid saavad automatiseerida hankija maksesoovituste loomise protsessi.
author: kweekley
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 238123f59c3d85b2b2c64aed9d94c7d8af27eaf2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820807"
---
# <a name="automate-vendor-payment-proposals"></a>Hankija maksesoovituste automatiseerimine

[!include [banner](../includes/banner.md)]

Korduva graafiku alusel hankijatele maksvad organisatsioonid saavad nüüd automatiseerida hankija maksesoovituste loomise protsessi. Hankija maksesoovituste automatiseerimisel määratletakse järgmised üksikasjad.

- Millal maksesoovitused käivitatakse
- Milliseid kriteeriume kasutatakse maksmisele kuuluvate arvete valimiseks
- Millisel hankija maksete töölehel tehtavad maksed salvestatakse

Maksesoovituste automatiseerimine ei sisesta makseid automaatselt. Seega saate loodud maksete kinnitamiseks jätkata mis tahes valideerimis- ja töövooprotsesside kasutamist.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Hankija maksesoovituste aset leidmise määratlemine

Hankija maksesoovituste automatiseerimisel kasutatakse protsessi automatiseerimise raamistikku. Erinevad äriprotsessid kasutavad seda raamistikku valitud protsessi kordumise määratlemiseks. Hankija maksesoovituste puhul saab automatiseerimisele ligi jaotises **Ostureskontro \> Makse seadistus \> Protsessi automatiseerimine**.

Esmalt kasutage automatiseerimise valikut **Loo uus protsess** ja valige **Hankija maksesoovitus**. Seejärel juhatab viisard teid läbi hankija maksesoovituse seadistamise protsessi.

## <a name="general-page"></a>Üldine lehekülg

Sisestage viisardi lehel **Üldine** loodava hankija maksesoovituse nimi. Näiteks kui maksate kõikidele riigisisestele hankijatele esmaspäeval tšeki alusel, siis sisestage kirjeldavaks nimeks **Riigisisene\_Tšekk**. Sisestatav nimi kuvatakse protsessi automatiseerimise nädalavaates tööruumis **Hankija maksed**.

Järgmisena määratlege loodava makse töölehe omanik. Omanik on tavaliselt ostureskontro makseametnik, kes vastutab makse töölehe eest pärast selle loomist.

Ülejäänud lehekülje sätted on üldised ja neid kasutatakse hankija maksesoovituse selle versiooni korduvusmustri määratlemiseks. Näiteks kui sündmus on loodud esmaspäevaste tšekimaksete jaoks, siis saate määratleda, et see toimuks iga nädal, ning valida selle käitamise päevaks esmaspäeva. Samuti saate sisestada varase graafikuaja, nt 02:00, et protsessi automatiseerimine viidaks lõpule enne järgmise tööpäeva algust.

On oluline mõista, et kasutate viisardit selleks, et määratleda, millal hankija maksesoovitust töödeldakse. Te ei määratle seda, millal hankija makseid luuakse, prinditakse ja sisestatakse. Nädalavaates kuvatakse hankija maksesoovituste protsessi automatiseerimine korduvusmustris valitud päevadel.

Muude väljade kohta leiate lisateavet lehel **Üldine**, vt protsessi automatiseerimise dokumentatsiooni.

## <a name="vendor-payment-proposal-page"></a>Hankija maksesoovituse leht

Viisardi järgmine leht on **Hankija maksesoovituse** leht. Seda kasutatakse selleks, et määratleda kriteeriumid maksmisele kuuluvate hankija arvete valimiseks. Üldiselt on samad valikud leitavad hankija maksetöölehe maksesoovituse all. Siiski on mõned erandid. Näiteks tuleb kõik lehel toodud kuupäevad määratleda suhteliste kuupäevadena, kuna maksesoovituse kuupäev muutub iga kord, kui soovitust käitatakse.

### <a name="journal-name"></a>Töölehe nimi

Väli **Töölehe nimi** määratleb töölehe nime, kus hankija maksed luuakse. Hankija maksesoovituse automatiseerimise tulemusel luuakse määratletud töölehel maksed, kuid töölehte ei sisestata.

### <a name="from-date-and-to-date"></a>„Alates“ kuupäev ja „kuni“ kuupäev

Tähtaja või skonto kuupäeva alusel arvete valimisel „alates“ kuupäev ja „kuni“ kuupäeva määratlemise asemel peate „kuni“ kuupäeva määratlemiseks kasutama suvandit **Kuni kuupäeva kriteeriumide määratlemine** ja välja **Kuni kuupäeva päevade arvu korrigeerimine**. Maksesoovituse automatiseerimisel puudub „alates“ kuupäeva mõiste.

Vaikesättena on suvandi **Kuni kuupäeva kriteeriumide määratlemine** väärtuseks määratud **Ei**. Vaikeväärtust kasutades valib protsess käitamise korral kõik maksmisele kuuluvad arved, kuna „kuni“ kuupäeva ei ole määratletud.

Kui seate suvandi **Kuni kuupäeva kriteeriumide määratlemine** väärtuseks **Jah**, siis kasutage välja **Kuni kuupäeva päevade arvu korrigeerimine**, et määratleda kuupäev, mil arved valitakse, võttes aluseks täpsustatud päevade arvu enne või pärast protsessi käitamise kuupäeva. Number võib olla positiivne, negatiivne või 0 (null). Seejärel maksab süsteem arved, mille tähtaeg või skonto kuupäevad on täpsustatud arv päevi enne või pärast protsessi käitamise kuupäeva. Näiteks kõigi reedel või enne reedet maksmisele kuuluvate arvete korral loob makseseeria kõikide hankijate jaoks tšeki alusel maksed kolmapäeval. Sel juhul määrake välja **Kuni kuupäeva päevade arvu korrigeerimine** väärtuseks **2**. Kui maksesoovituse sündmus käitatakse kolmapäeval, 25. märtsil, siis valitakse maksmiseks kõik arved, mille tähtaeg või skonto kuupäev on 27. märts või enne seda.

### <a name="minimum-payment-date"></a>Varaseim maksekuupäev

Varaseim maksekuupäev määratleb varaseima kuupäeva, mida maksete loomisel kasutatakse. Esmalt peate seadma suvandi **Varaseima maksekuupäeva kriteeriumide määratlemine** väärtuseks **Jah**. See säte võimaldab teil kasutada varaseima maksekuupäeva funktsiooni. Kui seate suvandi väärtuseks **Jah**, siis kasutage välja **Varaseima maksekuupäeva päevade arvu korrigeerimine**, et määratleda varaseim maksekuupäev konkreetse päevade arvuna enne või pärast kuupäeva, mil protsessi käitatakse. Number võib olla positiivne, negatiivne või 0 (null). Näiteks loob makseseeria maksed kolmapäeval, hõlmates kõik maksed, mille varaseim maksekuupäev on esmaspäevale eelnev kuupäev. Sel juhul määrake välja **Varaseima maksekuupäeva päevade arvu korrigeerimine** väärtuseks **-2**.

Siin on näide, mis illustreerib, kuidas „kuni“ kuupäeva ja varaseima maksekuupäeva väljad koos toimivad. Maksesoovituse automatiseerimine on seadistatud käivituma kolmapäeval. Välja **Kuni kuupäeva päevade arvu korrigeerimine** väärtuseks on seatud **1**, et määratleda tähtaja alusel „kuni“ kuupäev. Välja **Varaseima maksekuupäeva päevade arvu korrigeerimine** väärtuseks on seatud **-2**. Kui makse protsessi automatiseerimine algab kolmapäeval, 25. märtsil, siis kaasatakse maksesoovitusse kõik arved, mille maksetähtaeg on 26. märtsil või enne seda. Maksesoovitused luuakse alltoodud moel.

- Kõigi arvete, mille tähtaeg on 23. märtsil või enne seda, maksetähtaeg on 23. märts.
- Arvete, mille tähtaeg on 24. märtsil, maksetähtaeg on 24. märts.
- Arvete, mille tähtaeg on 25. märtsil, maksetähtaeg on 25. märts.
- Arvete, mille tähtaeg on 26. märtsil, maksetähtaeg on 26. märts.

### <a name="summarized-payment-date"></a>Maksekuupäeva kokkuvõte

Maksekuupäeva kokkuvõtet kasutatakse vaid juhul, kui välja **Periood** väärtus on arvete maksemeetodi puhul **Kokku**. Kui välja **Periood** väärtus on maksemeetodite puhul **Kokku**, siis peate määrama suvandi **Maksekuupäeva kokkuvõtte kriteeriumide määratlemine** väärtuseks **Jah**. Kui seate suvandi väärtuseks **Jah**, siis kasutage välja **Maksekuupäeva kokkuvõtte päevade arvu korrigeerimine**, et määratleda maksekuupäeva kokkuvõte konkreetse päevade arvuna enne või pärast kuupäeva, mil protsessi käitatakse. Number võib olla positiivne, negatiivne või 0 (null). Näiteks loob seeria maksed kolmapäeval ja ettevõte soovib luua kolmapäeval maksekokkuvõtte. Sel juhul määrake välja **Maksekuupäeva kokkuvõtte päevade arvu korrigeerimine** väärtuseks **0**.

### <a name="records-to-include"></a>Kaasatavad kirjed

Maksesoovituse jaoks saab siiski määratleda filtrisuvandid. Kui filter on määratletud, siis filtri kriteeriume viisardilehel ei kuvata. Neid saab filtri taasavamisel siiski kuvada.

Ülejäänud soovituse väljad töötavad samamoodi kui hankija makse töölehel esitatud maksesoovituse korral. Teiste väljade kohta vt lisateavet teemast [Hankija maksete loomine maksesoovituse abil](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Mõned riigi-/piirkonnapõhised väljad ja mõned avaliku sektori väljad ei ole hetkel veel hankija maksesoovituse automatiseerimise funktsioonides saadaval.

Soovitame esmalt hinnata, kas automatiseerimine on teie organisatsiooni nõuete põhjal kasulik.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Hankija maksesoovituse automatiseerimise tulemuste kuvamine

Pärast hankija maksesoovituse automatiseerimise seeria loomist kuvatakse iga makse sündmused protsessi automatiseerimise nädalavaates. Hankija maksete puhul on protsessi automatiseerimise nädalavaade lisatud nii tööruumi **Hankija maksed** kui ka lehele **Protsessi automatiseerimine**.

[![Protsessi automatiseerimise nädalavaade hankija maksete tööruumis](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Tööruumis **Hankija maksed** kuvatavas protsessi automatiseerimise nädalavaates kuvatakse vaid hankija maksesoovituste automatiseerimised. Seal kuvatakse kõik käimasoleva nädala maksesündmused kõigi juriidiliste isikute kohta, kelle suhtes on sisselogitud kasutajal turbeõigused. Näiteks kui ostureskontro makseametnik vastutab USMF ja USSI ettevõtete maksete eest, siis näeb ta hankija maksesoovituste automatiseerimise sündmusi nende kahe ettevõtte, kuid mitte muude ettevõtete kohta.

[![USMF ja USSI ettevõtete protsessi automatiseerimise nädalavaade](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Iga sündmus kuvab ettevõtet, milles maksetööleht loodi või luuakse. Kui maksed luuakse tsentraliseeritud makseid kasutades, siis on kuvatav ettevõte see ettevõte, kus maksed luuakse. Sündmus ei pruugi tingimata kuvada, milliste ettevõtete arved tasutakse.

Lisaks kuvatakse maksesoovituse tuvastamise lihtsustamiseks iga sündmuse nimi.

Samuti kuvatakse iga sündmuse olek. Kasutatakse järgmisi olekuid.

- **Plaanitud** – maksesoovitus on plaanitud, kuid seda pole veel käivitatud.
- **Tõrge** – maksesoovitus on käivitatud, kuid ilmnes tõrge. Tõrkeid saate kuvada, kui klõpsate nupul **Tulemuste kuvamine**.
- **Lõpule viidud** – maksesoovitus on edukalt käitatud. Makseid saate kuvada, kui klõpsate lingil **Maksete kuvamine**. See link avab sündmuse loodud maksetöölehe.

Pärast maksete loomist saate kuvada maksete summasid töölehel. Summad kuvatakse kande valuutades. Näiteks kui maksetööleht hõlmab makseid nii USA dollarites kui ka Kanada dollarites, siis kuvatakse kummaski valuutas tehtud maksete kogusumma. 

Maksetöölehe saab pärast protsessi automatiseerimise kaudu loomist kustutada. Kui makse on täielikult kustutatud, leiavad aset järgmised sündmused.

- Nädala protsessi automatiseerimise olekuks jääb **Lõpule viidud**.
- Protsess eemaldab makse kogusummad ning lingi **Maksete kuvamine** asemel kuvatakse nupp **Tulemuste kuvamine**.
- Tulemuste kuvamisel saate teate, milles antakse teada, et esialgne tööleht on kustutatud.

Pärast makse kustutamist avanevad arved uuesti makse tegemiseks. Seejärel saab luua uue sündmuse arvete uuesti maksmiseks.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Hankija maksesoovituse automatiseerimise redigeerimine

Protsessi automatiseerimise raamistik võimaldab teil redigeerida maksesoovituse jaoks loodud makset, seeriat ja sündmuseid. Seeriat saab redigeerida lehel **Protsessi automatiseerimine** või protsessi automatiseerimise nädalavaates. Näiteks kui ostureskontro haldur otsustab luua kõik riigisiseste hankijate tšekid esmaspäeva asemel kolmapäeval, siis võib ta leida nädalavaates sündmuse ja valida **Kuva/Redigeeri – seeria**. Seeria redigeerimisel palub süsteem teil määratleda, kas muudatus tuleks rakendada kõikide sündmuste või ainult uute sündmuste puhul. Selliste varasemate sündmuste, mille olek on juba **Lõpule viidud** või mis lõppesid olekuga **Tõrge**, olekut ei muudeta.

Samuti saate lisada uue sündmuse või muuta olemasolevat sündmust. Näiteks järgmine maksesoovituse sündmus on ajastatud käitamiseks kolmapäeval, 1. jaanuaril, kuid tegemist on pühaga. Te saate muuta sündmust protsessi automatiseerimise nädalavaates või lehel **Protsessi automatiseerimine**. Avaneb lehekülg, kus kuvatakse graafiku üksikasjad ja maksesoovituse kriteeriumid. Siin saate redigeerida plaanitud kellaaega ja kuupäeva. Samuti saate vajaduse korral redigeerida maksesoovituse kriteeriume. Näiteks kui muudate maksesündmuse plaanitud kuupäeva 1. jaanuarilt 2. jaanuarile, võite soovida muuta ka „kuni“ kuupäeva suhtelisi kuupäevasid.

Samuti saate sündmuse või seeria keelata. Sündmuse keelamiseks ja selle töötlemise peatamiseks valige asjaomane sündmus protsessi automatiseerimise nädalavaates ja seejärel valige **Keela**. Seeria saate keelata lehel **Protsessi automatiseerimine**.

## <a name="security-for-payment-proposal-automations"></a>Hankija maksesoovituse automatiseerimiste turvalisus

Hankija maksesoovituste automatiseerimistele on lisatud järgmised kohustused ja privileegid. Nende kohustuste ja privileegide näol on tegemist turvalisuse vaikesätetega, kuid neid saab teie organisatsiooni nõuete alusel muuta. Näiteks kui graafiku korduvust saab lisaks ostureskontro haldurile redigeerida ja luua ka ostureskontro makseametnik, siis määrake ostureskontro makseametniku rolli täitvale isikule kohustus **Graafiku sündmuste haldamine**.

| Lõiv                              | Roll                                                                       | Privileegid |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Graafiku seeria haldamine          | Ostureskontro juht                                                   | See kohustus annab õiguse luua ja hallata maksesoovituse automatiseerimise seeriaid ja sündmusi järgmiste privileegide kaudu.<ul><li>Graafiku sündmuste haldamine</li><li>Graafiku seeria haldamine</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Sündmuste nädalavaate kuvamine</li></ul> |
| Graafiku sündmusi puudutav päring | Ostureskontro makseametnik, ostureskontro tsentraliseeritud makseametnik | See kohustus annab õiguse kuvada maksesoovituse automatiseerimise sündmusi järgmiste privileegide kaudu.<ul><li>Graafiku sündmuste kuvamine</li><li>Sündmuse nädalavaate kuvamine</li></ul> |
| Graafiku seeriaid puudutav päring      | None                                                                       | See kohustus annab õiguse kuvada seeriate ja sündmuste sätteid järgmiste privileegide kaudu.<ul><li>Graafiku sündmuste kuvamine</li><li>Sündmuste loendi lehe kuvamine</li><li>Sündmuse nädalavaate kuvamine</li></ul>|
| Graafiku sündmuste haldamine     | None                                                                       | See kohustus annab õiguse luua ja hallata sündmusi järgmiste privileegide kaudu.<ul><li>Graafiku sündmuste haldamine</li><li>Sündmuse nädalavaate kuvamine</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]