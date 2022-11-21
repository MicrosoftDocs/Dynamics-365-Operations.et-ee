---
title: Aastalõpu sulgemine
description: See artikkel kirjeldab pearaamatu aasta lõpu sulgemise protsessi käivitamiseks nõutavaid seadistusi ja etappe.
author: kweekley
ms.date: 11/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e1c7722b560246fb597f0b7f91a70afecf69e22
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779739"
---
# <a name="year-end-close"></a>Aastalõpu sulgemine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab pearaamatu aasta lõpu sulgemise protsessi käivitamiseks nõutavaid seadistusi ja etappe.

Rahandusaasta lõpus peate käivitama aastalõpu sulgemisprotsessi algsaldode ülekandmiseks uude aastasse. Enamik organisatsioone käivitavad aastalõpu sulgemise protsessi mitu korda. Esimene käitus teisaldab saldod uude rahandusaastasse. Protsessi saab seejärel uuesti käivitada nii palju kordi, kui on vaja, et teisaldada saldod kirjete reguleerimisest uude finantsaastasse.

Aastalõpu sulgemise protsessi käigus on loodud kaks võimalikku kannete tüüpi. Avamiskanne luuakse alati ja seda kasutatakse uues finantsaastas algsaldode loomiseks. Avamiskanne näitab uue finantsaasta bilansi pearaamatukonto saldosid ja jaotamata kasumi pearaamatukontol olevate kasumi ja kahjumi pearaamatukonto saldodest pärinevaid saldosid. Sulgemiskanne luuakse valikuliselt, et tuua kasumi- ja kahjumikontode saldod suletavas finantsaastas alla nullini.

## <a name="prepare-to-run-the-year-end-close"></a>Aastalõpu sulgemise käitamiseks ettevalmistamine

Enne aastalõpu sulgemisprotsessi käitamist kinnitage sätted järgmisesse kohta.

**Põhikonto** lehel

- Veenduge, et **Põhikonto tüüp** väli on iga põhikonto jaoks õigesti seadistatud. Põhikonto tüüp määrab, kas põhikonto saldo tuuakse edasi algsaldona või suletakse avamiskandes jaotamata kasumisse.
- Põhikonto jäägi saab aasta lõpus üle kanda uuele põhikontole. Sisestage uus põhikonto väljale **Avamiskonto**. Tavaliselt kasutatakse seda välja bilansi põhikontode jaoks, kui põhikonto on inaktiveeritud ja uut põhikontot kasutatakse uue finantsaasta jaoks.

Lehel **Pearaamatu parameetrid** valikus **Finantsaasta sulgemine** toimige järgmiselt.

- Valikut **Kustuta olemasolevad aastalõpu kanded aasta uuesti lõpetamisel** kasutatakse määramiseks, kas süsteemi loodud avamiskanne eelmisest aastalõpu sulgemisest tuleks kustutada, kui aastalõpu sulgemine käivitatakse uuesti. Kui see valik on seatud olekusse **Jah**, kustutatakse varasemad avamis- ja valikulised sulgemistehingud ning praeguste saldode põhjal luuakse uus avamis- või sulgemistehing. Kui see valik on seatud olekusse **Ei**, püsib eelmine avamis- ja valikuline sulgemiskanne ja luuakse täiendav avamis- või sulgemiskanne, et teisaldada saldod edasi pärast eelmist aastalõpu sulgemist sisestatud kannete reguleerimist.
- Suvandit **Loo sulgemiskanded** ülekande ajal kasutatakse sulgemiskannete loomiseks finantsaastas, mis suletakse, et kõigi põhikontode saldod nulliks tuua. Kui see valik on seatud olekusse **Jah**, luuakse nii avamis- kui ka sulgemiskanne. Kui see valik on seatud olekusse **Ei**, luuakse järgmisel finantsaastal saldode üleviimiseks ainult avamiskanne. Põhikonto saldod jäävad finantsaasta lõppu.
- Valik **Rahandusaasta oleku määramine püsivalt suletuks** kasutatakse finantsaasta seadmiseks püsivalt suletud olekusse. Kasutage seda valikut hoolikalt, sest jäädavalt suletud olekuga perioode ei saa uuesti avada. Seetõttu ei saa korrigeerimisi sisestada finantsaastasse. Parim tava näeb ette, et selle valiku väärtuseks on **Ei**.
- Suvand **Kande number peab olema täidetud** on eemaldatud. Aasta lõpu sulgemise protsessi käivitamisel on vaja kannet. Sel ajal sisestatakse kande number käsitsi.

Lehel **Rahanduskalender** toimige järgmiselt.

- Järgmine finantsaasta peab eksisteerima enne aastalõpu sulgemise käitamist. Vastasel juhul ei saa algsaldosid avamisperioodis luua.

Lehel **Pearaamatu kalender** toimige järgmiselt.

- Valikuline: iga suletavat finantsaasta rahandusaastat saab määrata olekusse **Ootel**, et takistada uute kannete sisestamist. Korrigeerivate sisestuste tuvastamisel saab ooteloleku perioodid korrigeerivate sisestuste sisestamiseks taasavada isegi siis, kui aastalõpu sulgemisprotsess on juba käivitatud.

**Aasta lõpu sulgemise malli seadistus** lehel:

- Kui **pearaamatu aasta lõpu täiustuste** funktsioon on sisse lülitatud, eraldatakse aasta lõpu sulgemise malli seadistamise protsess aasta lõpu sulgemise protsessist. Malli saab määratleda **Aastalõpu sulgemise malli seadistuse** lehel (**Pearaamat \> Raamatu häälestus \> Aasta lõpu sulgemise malli häälestus**) või pääseb sellele juurde aasta lõpu sulgemise protsessist.

## <a name="define-year-end-close-templates"></a>Aastalõpu sulgemismallide määratlemine

Pärast konfiguratsiooni lõpule viimist saab käivitada aasta lõpu sulgemise protsessi. Lehel **Aastalõpu sulgemine malli seadistamine** saab määratleda malli selliste juriidiliste isikute grupile, mille jaoks aastalõpu sulgemisprotsess käivitatakse. Malli taaskasutatakse igal aastalõpu sulgemisel, kuid seda saab muuta, kui teie organisatsioon muutub.

Esmalt määratlege malli jaoks väli **Grupi nimi** ja valige rahanduskalender. Grupi nimi peaks identifitseerima lisatud juriidiliste isikute gruppi. Juriidiliste isikute rühmade määramisel pidage meeles, et juriidilisi isikuid saab samasse rühma kaasata ainult siis, kui nende jaoks on valitud sama eelarvekalender. Näiteks saab mallid seadistada geograafia põhjal nii, et Põhja-Ameerika, Euroopa, Kesk-ida ja Aafrika (EMEA) ja Aasia-Vaikse ookeani piirkond (APAC) juriidiliste isikute jaoks on loodud eraldi grupid.

Järgmisena saab mallile lisada juriidilised isikud. Juriidilisi isikute lisamiseks saate valida organisatsioonihierarhia või valida juriidilised isikud. Organisatsioonihierarhia valimisel lisatakse malli ainult hierarhiasisesed juriidilised isikud, kes kasutavad valitud rahanduskalendrit. Kui kasutate malli lisamiseks juriidilisi isikuid, saab lisada ainult sama rahanduskalendriga juriidilisi isikuid. Sama rahanduskalender on vajalik, kuna aastalõpu sulgemine käivitatakse finantsaasta valimisega, mis võib varieeruda olenevalt kalendrist.

Pärast juriidiliste isikute lisamist määratlege iga juriidilise isiku jaoks kinnipeetud tulude põhikontod.

Vahekaarti **Finantsdimensioon** kasutatakse määratlemiseks, milliseid finantsdimensioone avamiskandel kasutatakse. Pange tähele, et sellel vahekaardil olevad seadistused kehtivad ainult ruudustikus **Juriidilised isikud** valitud juriidilisele isikule. Korrake seadistust iga ruudustikus oleva juriidilise isiku jaoks.

Suvandit **Bilansi dimensioonide ülekandmine** kasutatakse määratlemiseks, kas bilansikontodele sisestatud kannetel olevaid finantsdimensioone tuleks säilitada avamiskandes. Parim tava näeb ette, et selle valiku väärtuseks on **Jah**. Bilansimõõtmete seade ei mõjuta jaotamata kasumi pearaamatukontode olemasolevaid saldosid. Need saldod määratletakse järgmises jaotises määratletud tulu ja kulu dimensioonidega. Näiteks rahandusaasta 2019 oli esimene, mis suleti ja suvandit **Sule kõik** kasutati **osakonna** ja **kulukeskuse** dimensioonide sulgemise valimiseks. Sel juhul loodi osakonna ja kulukeskuse iga kombinatsiooni jaoks eraldi jaotamata kasumi konto. Kui rahandusaasta 2020 aasta lõpu sulgemine on toimunud, jääb eelmise aasta jaotamata kasum täpselt selle seisuga, nagu need sisestati, isegi kui **Kande bilansi dimensioonide väärtuseks** on seatud **Ei**. Eelmise aasta lõpu sulgemiste jaotamata kasumile sisestatud saldosid ei muudeta kunagi.

Jaotist **Kasumi ja kahjumi dimensioonide ülekandmine** kasutatakse määratlemiseks, millised kasumi- ja kahjumikontole sisestatud finantsdimensioonid viiakse üle jaotamata kasumi põhikontole. Esmalt tuvastage valitud juriidilisele isikule asjakohased finantsdimensioonid. Need finantsdimensioonid hõlmavad finantsdimensiooni, mille suhtes on aasta jooksul sisestatud, isegi kui finantsdimensioon ei ole osa aktiivsest kontostruktuurist. Järgmisena määratlege iga dimensioon kui **Sule üksik** või **Sule kõik**. Vaikesuvandiks on **Sule kõik**. See suvand säilitab algsed finantsdimensiooni väärtused sisestatud kannetest ja kasutab neid jaotamata kasumi konto jaoks avamissaldode loomiseks. Eraldi jaotamata kasumi algsaldod luuakse iga unikaalse finantsdimensiooni väärtuste unikaalse kombinatsiooni puhul. Valiku **Sule üksik** tegemisel võetakse kõik selle finantsdimensiooniga sisestatud kanded kokku jaotamata kasumi algsaldosse valiku **Sule üksik** väljale sisestatud dimensiooniväärtuse puhul. Näiteks kõik finantsaasta kanded sisestati kontostruktuuriga **Põhikonto – osakond**. Malli **Osakond** finantsdimensioonis tehakse valik **Sule üksik** ja sisestatakse väärtus **100** dimensiooni väärtusena. Kui kõik osakondadesse 200, 300 ja 400 sisestatud kanded on 100 000 dollarit, luuakse **jaotamata kasumi -100** jaoks üks algsaldo. Kui teete valiku **Sule üksik** ja jätate finantsdimensiooni väärtuse tühjaks, sisestatakse kõik kanded jaotamata kasumisse nii, et dimensiooni väärtus on tühi.

## <a name="run-the-year-end-close-process"></a>Aastalõpu sulgemisprotsessi käivitamine

Pärast aasta lõpu sulgemise mallide loomist saate aasta lõpu sulgemise protsessi käivitada lehel **Aasta lõpu sulgemine** (**Pearaamat \> Perioodi sulgemine \> Aasta lõpu sulgemine**). Enne aasta lõpu sulgemise käivitamist saate lisada uusi aasta lõpu sulgemise malle või muuta olemasolevaid malle, valides mallide seadistamise lehe avamiseks **Aastalõpu sulgemise malli seadistamine**.

Valige aastalõpu sulgemise mall ja seejärel valige tegevuspaanil suvand **Käivita aastalõpu sulgemine**. Valige mallist, mille jaoks aasta lõpupoole kasutate, kas kõik juriidilised isikud või juriidiliste isikute alamhulk. Finantsaastas esimest korda aastalõpu sulgemise käivitamisel valite tõenäoliselt kõik juriidilised isikud, et luua kõikide jaoks algsaldod. Kui olete aastalõpu varem lõpetanud, võiksite seda uuesti teha ainult nende juriidiliste isikute jaoks, kelle jaoks korrigeerivaid kirjeid postitati.

Järgmisena valige finantsaasta, et käivitada aastalõpu sulgemisprotsess uuesti. Kui rahandusaasta viimase perioodi kohta on olemas rohkem kui üks sulgemisperiood, muutub väli **Perioodi nimi** kättesaadavaks. Seejärel saate valida sulgemisperioodi postitamiseks kasutatava sulgemisperioodi, kui seadistus on määratud lõpptehingu loomiseks.

Järgmisena sisestage kande number. Sama kandenumbrit kasutatakse kõikide aastalõpu sulgemisprotsessi jaoks valitud juriidiliste isikute puhul. Kandenumbrit ei looda numbriseeriat kasutades.

Vaikimisi läheb aastalõpu sulgemise protsess vaikimisi pakktöötlusrežiimi. Seetõttu saate pärast selle käivitamist naasta teiste tegevuste juurde.

Kuna konto struktuurid võivad kogu rahandusaasta jooksul muutuda, ei saa asjakohast kontostruktuuri alati tuvastada. Seetõttu aastalõpu sulgemise protsess ei järgi kontostruktuure. Avamiskannete loomisel tuuakse saldod edasi finantsdimensioonidega, nagu on määratletud aastalõpu sulgemise mallis. Algsaldo kirjed võivad hõlmata praeguses kontostruktuuris ja segmendikombinatsioonides mittesisalduvaid finantsdimensioone, mis ei kehti enam praeguses kontostruktuuris. Kui teie organisatsioon soovib jaotamata kasumi algsaldo puhul finantsdimensiooni välja arvata, seadke finantsdimensioon valikule **Sule üksik** ja jätke dimensiooni väärtus tühjaks.

Pärast protsessi lõpuleviimist luuakse kirje iga juriidilise isiku ja eelarveaasta kombinatsiooni kohta. Näete ainult nende juriidiliste isikute kirjeid, millele teil on juurdepääs. Iga kirje sisaldab süsteemi kuupäeva ja kellaaega, mil protsess käivitati ning otsesed seosed aasta lõpu sulgemise jaoks loodud kannetega.

[![Aastalõpu lõpetamise ajaloo kiirkaardil aastalõpu lõpetamise lehel loodud kirjed](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Kui käivitate aastalõpu lõpetamise uuesti, näete ühte või mitut kirjet juriidilise isiku ja rahandusaasta iga kombinatsiooni kohta, sõltuvalt suvandist **Kustuta olemasolevate aastalõpu kirjete aasta korduval lõpetamisel** lehel  **Pearaamatu parameetrid**:

- Kui suvandiks on **Jah**, siis eelmise aasta lõpu kupong kustutatakse. Kirje on märgitud kui **Tagasipööratud** ja tembeldatakse kuupäeva ja kellaajaga, mil tagasipööramine tehti. Lisaks eemaldatakse seos kande numbriga. Kui aastalõpu sulgemine on lõpule viidud, luuakse loodava uue kande jaoks uus kirje.
- Kui valiku väärtuseks on määratud **Ei**, jääb eelmise aasta lõpu sulgemise kirje koos lingiga kandega alles. Iga kord kui aasta lõpu sulgemine uuesti käivitatakse, luuakse uus kirje koos lingiga uutele kannetele.

## <a name="reverse-the-year-end-close-process"></a>Aastalõpu sulgemisprotsessi ümberpööramine

**Aastalõpu sulgemise** lehel saate aastalõpu lõpetamise tühistada. Valige juriidilise isiku ja finantsaasta kombinatsiooni kirje, mis tuleb tühistada, ja seejärel valige **Pöörake tagasi aastalõpu sulgemine**. Tagasipööramise protsess kustutab kõik rahandusaasta jaoks loodud avamis- ja sulgemiskanded. Kirje on märgitud kui **Tagasipööratud** ja tembeldatakse kuupäeva ja kellaajaga, mil tagasipööramine tehti. Lisaks eemaldatakse seos kande numbriga. Sarnaselt aastalõpu sulgemisprotsessile toimub tagasipööramine partii režiimis.

Ruudustiku kohal asuv märkeruut **Kuva tagurpidi** võimaldab teil peita või kuvada vastupidiseid aastalõpu sulgemisprotsesse. Pärast **Aastalõpu sulgemise pöörd** protsessi käivitamist peate võib-olla kirje avamiseks valima märkeruudu **Kuva ümberpööratud**. Muu teabe vaatamiseks saate määrata täiendavaid filtreid.

[![Kasutades märkeruutu Kuva tagurpidi, näete aasta lõpu sulgemislehe tagasipööratud protsesside kirjeid](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Lisateabe saamiseks vt [Pearaamatu sulgemine perioodi lõpus](close-general-ledger-at-period-end.md) ja [Rahandusaasta sulgemine](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
