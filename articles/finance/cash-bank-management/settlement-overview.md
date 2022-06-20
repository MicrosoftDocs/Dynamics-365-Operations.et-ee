---
title: Tasakaalustuse ülevaade
description: Selles artiklis antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab, milliseid kandetüüpe saab tasakaalustada ning nende tasakaalustamise ajastust ja protsessi. Samuti kirjeldatakse teemas tasakaalustamisprotsessi tulemusi.
author: panolte
ms.date: 07/30/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14551"
- intro-internal
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a495a71a95032a0022cbab2783f356db48ee349d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887944"
---
# <a name="settlement-overview"></a>Tasakaalustuse ülevaade

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Selles artiklis antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab, milliseid kandetüüpe saab tasakaalustada ning nende tasakaalustamise ajastust ja protsessi. Samuti kirjeldatakse teemas tasakaalustamisprotsessi tulemusi.

Tasakaalustuse ajal rakendatakse ühe dokumendi kanded teise dokumendi kannetele, et suurendada või vähendada kummagi dokumendi saldot. Näiteks saate makse arvele rakendada. Erinevaid kandetüüpe saab erinevatel aegadel ja erinevate meetodite kaudu tasakaalustada. Tasakaalustamisprotsessi käigus võidakse luua ka uusi kandeid.

## <a name="what-transactions-can-be-settled"></a>Milliseid kandeid saab tasakaalustada?

Ostureskontro ja müügireskontro tasakaalustamine võib toimuda mis tahes kandetüüpide vahel, mis mõjutavad hankija saldot või kliendi saldot. Need kandetüübid võivad hõlmata arveid, makseid, kreeditarveid ja tasusid. Iga kandetüübi saab tasakaalustada teise kandetüübi suhtes. Näiteks saate tasakaalustada makse arve suhtes, kreeditarve arve suhtes, ühe arve teise arve suhtes ja ühe makse teise makse suhtes.

Saate tasakaalustada makseid samas juriidilises isikus või teises juriidilises isikus olevate kannete suhtes. Organisatsioonid, mis kasutavad tsentraliseeritud maksemudelit, [tsentraliseeritud maksed](set-up-centralized-payments.md) saavad aidata makseprotsessi sujuvamaks muutmisel.

## <a name="when-to-settle-transactions"></a>Millal kandeid tasakaalustada?

Kandeid saab tasakaalustada maksete sisestamisel. Näiteks kui teete makse hankijale, valite tavaliselt makstavad arved. Arvete valimisega märgistate need makse suhtes tasakaalustamiseks. Kui müügireskontro makseametnikud kirjendavad kliendimaksed, saavad nad kliendimaksesse lisatud teabe põhjal sobivad arved tasakaalustamiseks märgistada. Maksete tasakaalustamiseks märkimiseks kasutate lehte **Kannete tasakaalustamine**. Selle lehe saate avada mis tahes sisestamata arvelt või makselt. Kande sisestamisel sisestatakse ka tasakaalustus. 

Kandeid saab tasakaalustada ka pärast sisestamist. Saate sisestada kliendimakse ilma seda arvete suhtes tasakaalustamata. Siiski peate võib-olla enne kande sisestamist esmalt uurima, kas makse on õige arve suhtes tasakaalustatud. Lehe **Kannete tasakaalustamine** saab avada lehelt **Kõik kliendid** või **Kõik hankijad** või mis tahes kliendi või hankija lehelt **Kanded**.

Samuti saate arve jaoks sisestatud ettemakseid reserveerida, märkides makse ostutellimuse või müügitellimuse suhtes tasakaalustamiseks. Sellisel juhul on maksel endiselt avatud saldo, kuid selle saab tasakaalustada teise arve suhtes. Makse tasakaalustatakse automaatselt ostu- või müügitellimusest loodud arve suhtes.

## <a name="how-to-settle-transactions"></a>Kuidas kandeid tasakaalustada?

Kandeid saab tasakaalustada käsitsi, automaatselt või kaht meetodit kombineerides. Tasakaalustamisviis sõltub teie äriprotsessidest. Kandeprotsesse saate konfigureerida lehtedel **Ostureskontrode parameetrid** ja **Müügireskontrode parameetrid**, et kindlustada nende vastavus antud äriprotsessidele.

Saate luua hankijamakseid ja kliendi otsekorraldusmakseid, kasutades maksesoovitust. Maksesoovitust kasutatakse makstavate arvete valimiseks. Maksesoovitus algatatakse käsitsi ja seejärel märgib süsteem valitud arved maksete loomisel automaatselt tasakaalustamiseks.

Kui maksed luuakse käsitsi, saate tasakaalustatavad arved valida lehel **Kannete tasakaalustamine**. Saate arveid käsitsi valida või kasutada suvandit **Märgi prioriteedi alusel**, et arved märgitaks tasakaalustamiseks automaatselt. Suvand **Märgi prioriteedi alusel** on saadaval ainult müügireskontro puhul. Selle suvandi saate sisse lülitada lehe **Müügireskontrode parameetrid** vahekaardil **Tasakaalustamise prioriteet**.

Kui makseametnik sisestab makse, kuid ei tasakaalusta seda makset enne sisestamist, saab makse automaatselt tasakaalustada. Saate automaatse tasakaalustamise sisse lülitada lehtedel **Müügireskontro parameetrid** ja **Ostureskontro parameetrid**. Automaatne tasakaalustamine tasakaalustab vaid ühe juriidilise isiku kanded. See ei tasakaalusta mitme juriidilise isiku kandeid.

Automaatse tasakaalustuse kasutamisel saate kasutada eelmääratletud tasakaalustuse prioriteeti või saate määratleda teie enda tasakaalustuse prioriteedi lehel **Müügireskontro parameetrid**. See funktsioon on saadaval ainult müügireskontro puhul.

## <a name="results-of-settlement"></a>Tasakaalustamise tulemused

Kui kanded on tasakaalustatud, suurendatakse või vähendatakse iga kande saldot vastavalt vajadusele. Kui arve ja makse on tasakaalustatud, siis värskendatakse iga kande olekut ja saldot tavaliselt järgmiste reeglite järgi.

- Kui makse summa on suurem kui arve summa, vähendatakse arve saldo väärtusele 0,00 ja arve suletakse. Makse jääb avatuks ja saldo on maksesumma ja arvesumma vahe.
- Kui makse summa on väiksem kui arve summa, vähendatakse makse saldo väärtusele 0,00 ja makse suletakse. Arve jääb avatuks ja saldo on arvesumma ja maksesumma vahe.
- Kui makse summa on arve summaga võrdne, suletakse nii makse kui ka arve ja mõlema saldo alandatakse 0,00-ni.

Kui [maksesumma on väiksem kui arve summa](../accounts-payable/vendor-payments-partial-amount.md) ja selle põhjuseks on skonto, mahakandmine või alamakse, võidakse arve ja makse siiski sulgeda, olenevalt tasakaalustuste konfigureerimise sätetest lehtedel **Ostureskontro parameetrid** ja **Müügireskontro parameetrid**.

Tasakaalustused saavad luua ka kandeid. Näiteks võib arve ja makse tasakaalustamine tekitada skonto, realiseeritud kasumi või kahjumi, käibemaksu korrigeerimisi, mahakandmisi või sendierinevusi.

## <a name="identifying-marked-transactions-during-settlement"></a>Märgitud kannete tuvastamine tasakaalustuse ajal

Kui proovite tasakaalustada kannet, siis võite märgata sümbolit, mis viitab sellele, et kanne on märgistatud teises asukohas. Sel juhul võite valida kande lehel **Kannete tasakaalustamine** ja valida suvandi **Päringud \> Tasakaalustamine tasakaalustamise aknas**. Selle päringu vaates kuvatakse töölehed, müügitellimused, arved, maksesoovitused ja kliendi asukohad, mis võivad blokeerida kande tasakaalustamist. Probleemi lahendamiseks võite valida lingi, et minna otse päringust blokeeritud asukohta. Seejärel saate dokumenti uuendada, sisestades tasakaalustamiseks vajalikud korrektsioonid. Lisaks saate kasutada näitajat **Märgitud**, et tuvastada teised samas blokeerimisasukohas paiknevad dokumendid.

## <a name="resolve-issues-with-transactions-that-cant-be-settled"></a>Kannete, mida ei saa tasakaalustada, probleemide lahendamine

Mõnikord ei saa kandeid tasakaalustada, kuna dokumenti töötleb parajasti mõni muu tegevus. Kui proovite kandeid tasakaalustada, ilmneb tõrge, sest neid kandeid kasutatakse. Probleemi lahendamiseks saate kasutada lehte **Märgitud kande üksikasjad**, et leida tasakaalustamiseks märgitud kandeid ja tuvastada mis tahes muid protsesse, mis neile juurde pääsevad.

Kanded märgitakse tasakaalustamiseks hankijaarvete maksmisel või siis, kui kliendid maksavad ära oma avatud arved. Mõnikord võivad need arved juba tasakaalustuseks märgitud olla. Seetõttu ei saa kasutajad neid maksmiseks valida. Arved võivad praeguses juriidilises isikus või mõnes muus juriidilises isikus olla märgitud teise kliendi maksetöölehe, müügitellimuse, hankija maksetöölehe või ostutellimuse poolt.

Kui kanne on kliendimakse sisestamisel tasakaalustamiseks blokeeritud, avage leht **Kliendi märgitud kande üksikasjad** (**Müügireskontro \> Perioodilised ülesanded \> Kliendi märgitud kande üksikasjad**). Kande blokeerimise asukoha kiireks tuvastamiseks saate seadistada ühe järgmistest valikuparameetritest: **Kliendi konto**, **Kanne**, **Kuupäev** või **Arve**. Kui te valikuparameetreid ei määra, kuvab süsteem kõik praeguse ettevõtte või mõne teise valitud ettevõtte blokeeritud dokumendid. Kui tasakaalustamiseks blokeeritud kanne on tuvastatud, saate selle valida ja seejärel teha valiku **Eemalda valitud kannetelt märge**. Seejärel eemaldatakse valitud kanne mis tahes töölehelt, mis seda sisaldab. Kuid dokumenti ei eemaldata muust asukohast. Töölehelt eemaldatakse ainult märgistusteave.

Kui kanne on hankijamakse sisestamisel tasakaalustamiseks blokeeritud, avage leht **Hankija märgitud kande üksikasjad** (**Ostureskontro \> Perioodilised ülesanded \> Hankija märgitud kande üksikasjad**). Kande blokeerimise asukoha kiireks tuvastamiseks saate seadistada ühe järgmistest valikuparameetritest: **Hankija konto**, **Kanne**, **Kuupäev** või **Arve**. Kui te valikuparameetreid ei määra, kuvab süsteem kõik praeguse ettevõtte või mõne teise valitud ettevõtte blokeeritud dokumendid. Kui tasakaalustamiseks blokeeritud kanne on tuvastatud, saate selle blokeeringu eemaldamiseks valida ja seejärel teha valiku **Eemalda valitud kannetelt märge**. Seejärel eemaldatakse valitud kanne mis tahes muult töölehelt, kus see on valitud. Kuid dokumenti ei eemaldata muust asukohast. Töölehelt eemaldatakse ainult märgistusteave.

Kõigi blokeeritud dokumentide tuvastamiseks avage leht **Kõik märgitud kande üksikasjad** (**Müügireskontro \> Perioodilised ülesanded \> Kõik märgitud kande üksikasjad** või **Ostureskontro \> Perioodilised ülesanded \> Kõik märgitud kande üksikasjad**). Kande blokeerimise asukoha kiireks tuvastamiseks saate seadistada ühe järgmistest valikuparameetritest: **Kliendi konto**, **Hankija konto**, **Kanne**, **Kuupäev** või **Arve**. Kui te valikuparameetreid ei määra, kuvab süsteem kõik praeguse ettevõtte või mõne teise valitud ettevõtte blokeeritud dokumendid. Kui tasakaalustamiseks blokeeritud kanne on tuvastatud, saate selle blokeeringu eemaldamiseks valida ja seejärel teha valiku **Eemalda valitud kannetelt märge**. Seejärel eemaldatakse valitud kanne mis tahes muult töölehelt, kus see on valitud. Kuid dokumenti ei eemaldata muust asukohast. Töölehelt eemaldatakse ainult märgistusteave.

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada **funktsioonihalduse** tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** sularaha- ja pangahaldus
- **Funktsiooni nimi:** märgitud kande üksikasjade vorm

## <a name="additional-resources"></a>Lisaressursid

- [Jäägi tasakaalustus](settle-remainder.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
