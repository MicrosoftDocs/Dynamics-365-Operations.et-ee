---
title: Tasakaalustuse ülevaade
description: Selles teemas antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab, milliseid kandetüüpe saab tasakaalustada ning nende tasakaalustamise ajastust ja protsessi. Samuti kirjeldatakse teemas tasakaalustamisprotsessi tulemusi.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d8b7bec73b0461f286165cd36e61c6e8b5a6270b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225532"
---
# <a name="settlement-overview"></a>Tasakaalustuse ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab, milliseid kandetüüpe saab tasakaalustada ning nende tasakaalustamise ajastust ja protsessi. Samuti kirjeldatakse teemas tasakaalustamisprotsessi tulemusi.

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

## <a name="additional-resources"></a>Lisaressursid

- [Jäägi tasakaalustus](settle-remainder.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]