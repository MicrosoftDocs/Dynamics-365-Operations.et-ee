---
title: Miks ma ei saa seda kannet tühistada?
description: See artikkel kirjeldab erinevaid põhjusi, miks kandeid ei saa tühistada. Samuti loetletakse selle probleemi lahendusi.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9a8b26584b1a9b82440583db693cd14daa580e22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876178"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Miks ma ei saa seda kannet tühistada?

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab erinevaid põhjusi, miks kandeid ei saa tühistada. Samuti loetletakse selle probleemi lahendusi.

## <a name="symptom"></a>Sümptom

Organisatsioonidel võib tekkida olukord, kus nad peavad tühistama sisestatud kande. Mõnikord takistab süsteem neil neid kandeid tagasi võtta. Selline käitumine võib esitada kaks küsimust:

- Miks ma ei saa seda kannet tühistada?
- Kuidas mõjutab massilise tagasipööramise funktsioon seda käitumist?

## <a name="resolution"></a>Lahendus

Kanded peavad enne ümberpööramist vastama kindlatele kriteeriumidele. Selle artikli ülejäänud jaotised annavad kinnituse iga mooduli jaoks. Kuigi see artikkel keskendub kannetele Microsoft Dynamics 365 Finantsis, saab mõningaid mõisteid ja kinnitamist rakendada teistele rakendustele, nt Dynamics 365 Supply Chain Management.

Lisaks võib see koht, kus kanne tühistatakse, mõjutada, kas seda saab tagasi võtta. Näiteks saab müüja makset, mis on sisestatud tšekina, tühistada ainult pangakontode kandelehe jaotises **Tšekid**. Seda ei saab tühistada jaotisest **Vautcheri kanded** pearaamatu lehelt.

Kui **mitme dokumendi funktsiooni masspööramine** (tuntud ka kui masspööramise funktsioon) on sisse lülitataud **Funktsiooni halduses** mõjutab see seda, kui palju kandeid saab tagasi võtta ja kus neid saab tagasi võtta. See funktsioon pakub kahte soodustust, kui see on sisse lülitatud:

- Teatud tüüpi kannete puhul saab korraga valida ja tühistada mitu kannet töölehelt, millelt see sisestati, või **Kanded** lehelt. Üksikud kanded peavad olema tühistatavad enne funktsiooni sisse lülitamist. Enne selle funktsiooni sisestamist tuleb kanded ühe korraga tühistada.
- *Mõned* alam pearaamatukanded saab tühistada töölehel (peatööleht) või **Voucher kannete** lehel. Neid ei pea alamtöölehelt tühistama. Näiteks saab hankija arve töölehte varem tühistada ainult lehelt **Hankija kanded**. Nüüd saab seda siiski tühistada ka pearaamatu poolelt, töölehelt või kande **Voucher kannete** lehelt. Selle artikli iga jaotis selgitab kandetüüpe, mille puhul seda soodustust ei rakendata.

Masspööramise funktsioon **ei** võimalda rohkem kandetüüpe tagasi võtta. Kui kandetüüpi ei saanud varem tühistada, ei saa seda enam tagasi võtta, kui funktsioon on sisse lülitatud. Näiteks ei saa ostutellimuse hankijaarveid tühistada, olenemata sellest, kas hulgipööramise funktsioon on sisse lülitatud.

Lisateavet hulgipööramise funktsiooni kohta vt [Vastupidine töölehe sisestamine](reverse-journal-posting.md).

## <a name="general-ledger"></a>Pearaamat

Pearaamatu korrigeerimised sisestatakse ainult pearaamatukontosid kasutades. Seetõttu uuendavad nad ainult pearaamatut.

Kui hulgipööramise funktsioon on välja lülitatud, saab enamike pearaamatu korrigeerimiste eest tühistada ükshaaval **Kanded \<main account\>** pearaamatu lehelt (**LedgerTransAccount**). (Lehekülje täpne pealkiri erineb sõltuvalt valitud põhikontost.) Lehel kuvatakse kõik põhikontole sisestatud kanded. See avatakse tavaliselt **proovibilansi** kaudu või valides **Kande** leheküljelt **Voucher kanded**.

Kui hulgipööramise funktsioon on sisse lülitatud, saab ühe või mitu pearaamatukannet nüüd tagasi võtta **Kannete** leheküljelt ja töölehelt, millelt kanne proovibilanssi sisestati. Erandid on pearaamatu välisvaluuta ümberarvutamine, konsolideerimine ja aasta lõpu sulgemise kanded. Need kanded tühistatakse lehtedelt, millelt aasta lõpetamise sulgemine käivitati.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Kannete tühistamise põhjused

Kandeid ei saa järgmistel põhjustel tagasi pöörata:

- Päevaraamat:

    - Rahandusperiood on ootel või jäädavalt suletud:

        - Kui tühistamise kuupäev on rahandusperioodis, mis pole avatud, ei saa kannet tühistada.
        - Kui kanne toetab tühistamiskuupäeva sisestamist, saab kannet siiski tagasi võtta, muutes tagasipööramise kuupäeva avatud perioodiks.

    - Aasta lõpu sulgemisprotsess on käitatud:

        - Kande raamatupidamiskuupäev on rahandusaastas, mis on läbinud aasta lõpetamise. Kuigi rahandusaasta periood võib siiski olla avatud, ei saa kannet tühistada, kui rahandusaasta kohta on käitatud aasta lõpetamise sulgemisprotsess. Finantsaasta olek erineb selle perioodi olekust.
        - Aasta lõpu sulgemise saab tühistada ja seejärel kande tühistada. See lähenemine ei pruugi olla suvand. Sõltuvalt fiskaal sulgemise protsessi olekust, võib olla lihtsam sisestada tagasipööratud kanne käsitsi kas suletud rahandusaasta või järgmise rahandusaasta avatud perioodi. Kui uus kanne sisestatakse finantsaasta avatud perioodi, mis on läbinud aasta lõpu sulgemise protsessi, tuleb aasta lõpu sulgemine uuesti käivitada.

    - Kande tühistamine on juba kestev:

        - Kui kannet tühistatakse, tuleb see protsess lõpule viia. Eraldi ümberpööramisprotsessi ei saa teha. 
        - Pärast tühistamise lõpetamist saab ümber pööratud kande uuesti tühistada (st stornatsiooni saab tagasi võtta).

    - Pearaamatu tasakaalustamine:

        - Kui tehingu üks või mitu rida on arveldatud perioodilise toimingu **Pearaamat tasakaalustamine** perioodilised ülesanded (**Pearaamat \> Perioodilised ülesanded \> Pearaamatu rveldus**), nii et kirje on olemas LedgerTransSettlement tabelis, ei saa kannet tühistada.
        - Pearaamatu arrvelduse saab tühistada ja seejärel kande tühistada.

    - Kontsernisisene:

        - Kui kanne on kontsernisisene kanne, ei saa seda tühistada.
        - Kanne pole **pole** kontsernisisene kanne, kuid see sisestatakse kontsernisisese seadistuse lehel määratletud põhikontole **Kontsernisisene seadistus** lehel.

    - Viitvõlad:

        - Kui viitvõla pearaamatukanne tühistatakse, tühistatakse viitvõla kirje ja kõik vastavad viitvõla alamkanded.
        - Üksikuid tekkepõhiseid alamkandeid ei saa tühistada.

- Tulu tuvastamise päevik:

    - Tulude kajastamise tehinguid ei saa tagasi pöörata.
    - Kui tulu tuvastatakse tuluarvestustöölehe kaudu, sisestatakse see kanne ainult pearaamatukontodele. Seetõttu ilmuvad kanded sellistele lehtedele nagu **Kande**, kanded ilmuvad, nagu oleks need ainult pearaamatukirjed.

- Välisvaluuta ümberarvutamine:

    - Välisvaluuta ümberarvutamise kandeid saab tühistada, kuid ainult pearaamatu **välisvaluuta ümberarvutamise** lehelt, millelt ümberhindamine käivitati.
    - Tagasipööramise saab lõpule viia ainult siis, kui see on sisestatud avatud rahandusperioodi.

- Konsolideerimine:

    - Konsolideerimiskandeid saab tagasi pöörata, kuid ainult lehelt **Konsolideerimiskanded**.
    - Tagasipööramise saab lõpule viia ainult siis, kui see on sisestatud avatud rahandusperioodi.

- Aastalõpu sulgemine:

    - Aasta lõpu sulgemiskandeid (nii sulgemis- kui ka avamiskandeid) saab järgmisel viisil tagasi pöörata:

        - Kui pearaamatu aasta lõpu sulgemise täiustuste funktsioon on välja lülitatud, valige suvand **Tühista eelmine sulgemine** dialoogiboksis **Aasta lõpetamise sulgemine**.
        - Kui pearaamatu aasta lõpu täiustuste funktsioon on sisse lülitatud, valige ettevõtte ja finantsaasta kirjed, mis loodi aasta lõpus sulgemise lehel ja seejärel valige **Aasta lõpu sulgemine** **Tühista aasta lõpu sulgemine**.

    - Pange tähele, et aasta lõpu sulgemise tagasipööramine kustutab tegelikult sulgemis- ja avamiskanded. Tagasipööratud kannet ei sisestata kunagi.

## <a name="accounts-payable"></a>Ostureskontro

Mitu kandetüüpi uuendab ostureskontro alamtüüpi. Näited hõlmavad hankijaarveid, hankijaarvete töölehti ja kuluaruandeid.

Kui hulgipööramise funktsioon on välja lülitatud, saab kandeid tühistada ükshaaval kas arvete **hankija kannete** lehelt või **pangakonto** tšekimaksete tegemiseks.

Kui hulgipööramise funktsioon on sisse lülitatud, saab ühe või mitu pearaamatukannet nüüd tagasi võtta **Kannete** leheküljelt ja töölehelt, millelt kanne proovibilanssi sisestati. Hankija makseid saab siiski tühistada ainult pangakontolt. Hankijakandeid ei saa tühistada **kannetest \<main account\>** pearaamatu lehel. Neid saab tagasi pöörata ainult leheküljel **Kanded**.

Pange tähele, et mõningaid kandeid ei saa üldse tühistada. Näited hõlmavad ostutellimuse hankijaarveid ja elektroonilist hankijamakset.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Põhjused, miks kandeid ei saa tühistada

Kandeid ei saa järgmistel põhjustel tagasi pöörata:

- Rahandusperiood on ootel või jäädavalt suletud:

    - Kui tühistamise kuupäev on rahandusperioodis, mis pole avatud, ei saa kannet tühistada.
    - Kui kanne toetab tühistamiskuupäeva sisestamist, saab kannet siiski tagasi võtta, muutes tagasipööramise kuupäeva avatud perioodiks.

- Pearaamatu aasta lõpu sulgemisprotsess on käitatud:

    - Kande raamatupidamiskuupäev on rahandusaastas, mis on läbinud aasta lõpetamise. Kuigi rahandusaasta periood võib siiski olla avatud, ei saa kannet tühistada, kui rahandusaasta kohta on käitatud aasta lõpetamise sulgemisprotsess. Finantsaasta olek erineb selle perioodi olekust.
    - Aasta lõpu sulgemise saab tühistada ja seejärel kande tühistada. See lähenemine ei pruugi olla suvand. Sõltuvalt fiskaal sulgemise protsessi olekust, võib olla lihtsam sisestada tagasipööratud kanne käsitsi kas suletud rahandusaasta või järgmise rahandusaasta avatud perioodi. Kui uus kanne sisestatakse finantsaasta avatud perioodi, mis on läbinud aasta lõpu sulgemise protsessi, tuleb aasta lõpu sulgemine uuesti käivitada.

- Alammooduli töölehe kirjet pole pearaamatusse üle kantud:

    - See põhjus rakendub ainult mitte ostutellimuse hankija arvetele.
    - Kasutage **alammooduli töölehe kirjete lehte, mida pole veel üle kantud**, et kanda kirje pearaamatusse üle. Seejärel saab mitteostutellimuse hankija arve tühistada lehelt **Hankija kanded**.

- Tasakaalustus:

    - Kanne (nt arve või makse) tasakaalustatakse või märgitakse tasakaalustamiseks.

        - Saate kontrollida, kas kanne on tasakaalustatud või tasakaalustamiseks märgitud, valides lehel Hankija kanded valiku **Vaata tasakaalustusi** või **Tasakaalustus \> Tasakaalustuse ajalugu** lehel **Tasakaalustuse ajalugu**.
        - Tasakaalustuse saate tühistada ka leheküljel **Hankija kanded** lehel (**Tasakaalustus \> Tasakaalustuse tagasivõtmine**) kui üks kannetest tuleb tühistada.

- Kanne sisaldab mitut alam pearaamatukannet, mis sisestati sama kandenumbriga (üks kande väljaminek).
- Arve pole kinnitatud:

    - Kui **Kinnitus** märkeruudus pole märgitud ruut Kinnitus, ei saa arvet tagasi võtta.

        - Sel juhul ei viita kinnitus töövoo protsessi kinnitustele, vaid arve **Kinnitamise** suvandile arvel. Selle valiku abil saate vältida arve tasumist. Tavaliselt kasutatakse seda hankija arve registreerimisarvete puhul.

- Kanne arvete kogumis:

    - Kaustas asuvat arvet ei saa otse **hankija kannete** lehelt tagasi pöörata. Selle asemel tuleb see tühistada tühistamisprotsessi kaudu lehel **Arve kinnitamise tööleht**.

- Kandel on emaarve, mis on parandatud (India lokaliseerimine).
- Kandel on võlatähe olek **Arve ületud**.
- Kannet kasutatakse osaliseks maksu tasakaalustamiseks.
- Kanne sisaldab hankijakontot, kuid on ümber pööratud valelt leheküljelt, nt **Kanded \<main account\>** jaoks lehel:

    - Nagu sel põhjusel soovitatakse, isegi kui hulgipööramise funktsioon on sisse lülitatud, saab mõningaid alam pearaamatukandeid tühistada ainult konkreetsetelt lehtedelt.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Kannete tüübid, mida ei saa tühistada

Järgmist tüüpi kandeid ei saa tagasi pöörata:

- Välisvaluuta ümberarvutamine:

    - Erinevalt pearaamatu välisvaluuta ümberarvutamisest ei saa müügireskontrot ja ostureskontro välisvaluuta ümberarvutamisest tühistada. Selle asemel tuleb ümberhindamine uuesti käivitada, kasutades arve kuupäeva. Sel juhul kasutab ümberhindamine arve kuupäeva vahetuskurssi ning toob realiseerimata kasumi või kahjumi 0 (nulliks). Seetõttu sarnaneb tulemus eelmise ümberhindamise ümberpööramise tulemusega. Pange siiski tähele, et sama summat ei tühistata, kui arvel on muudetud vaikimisi vahetuskurssi.

- Ostutellimuse hankija arve:

    - Hankija arve tühistamiseks tuleb luua kreeditarve. Lisateavet selle kohta, kuidas luua vastupidist kannet, vt [ostu tagastustellimuse loomine](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Võlatäht
- Panga akreditiivi ekspordisaadetis

## <a name="accounts-receivable"></a>Müügireskontro

Mitu kandetüüpi uuendab ostureskontro alamtüüpi. Näited hõlmavad kliendiarveid müügitellimustest, kliendiarvetest, mis sisestatakse üldise töölehe kaudu, vabas vormis arveid, kliendimakseid ja mahakandmist.

Kui hulgipööramise funktsioon on välja lülitatud, saab kandeid tühistada ükshaaval kas arvete **hankija kannete** lehelt või **pangakonto** hoiuste lehel. Makse tühistamise kohta lisateabe saamiseks vt selle artikli [jaotist](cant-reverse-transctns.md#cash-and-bank-management) Sularaha ja panga haldus.

Kui hulgipööramise funktsioon on sisse lülitatud, saab ühe või mitu pearaamatukannet nüüd tagasi võtta **Kannete** leheküljelt ja töölehelt, millelt kanne proovibilanssi sisestati. Deposiite saab siiski tagasi võtta ainult pangakontolt ja vabas vormis arveid saab tagasi võtta ainult lähtelehelt (kui parandusi lubav funktsioon lülitatakse sisse). Lisaks, kliendikandeid ei saa tühistada **kannetest \<main account\>** jaoks pearaamatu lehel. Kuid neid saab tagasi pöörata leheküljel **Kanded**.

Pange tähele, et mõningaid kandeid ei saa üldse tühistada. Näited hõlmavad müügitellimuse kliendiarveid ja mahakandmist.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Kannete tühistamise põhjused

Kandeid ei saa järgmistel põhjustel tagasi pöörata:

- Rahandusperiood on ootel või jäädavalt suletud:

    - Kui tühistamise kuupäev on rahandusperioodis, mis pole avatud, ei saa kannet tühistada.
    - Kui kanne toetab tühistamiskuupäeva sisestamist, saab kannet siiski tagasi võtta, muutes tagasipööramise kuupäeva avatud perioodiks.

- Pearaamatu aasta lõpu sulgemisprotsess on käitatud:

    - Kande raamatupidamiskuupäev on rahandusaastas, mis on läbinud pearaamatus aasta lõpetamise. Kuigi rahandusaasta periood võib siiski olla avatud, ei saa kannet tühistada, kui rahandusaasta kohta on käitatud aasta lõpetamise sulgemisprotsess. Finantsaasta olek erineb selle perioodi olekust.
    - Aasta lõpu sulgemise saab tühistada ja seejärel kande tühistada. See lähenemine ei pruugi olla suvand. Sõltuvalt fiskaal sulgemise protsessi olekust, võib olla lihtsam sisestada tagasipööratud kanne käsitsi kas suletud rahandusaasta või järgmise rahandusaasta avatud perioodi. Kui uus kanne sisestatakse finantsaasta avatud perioodi, mis on läbinud aasta lõpu sulgemise protsessi, tuleb aasta lõpu sulgemine uuesti käivitada.

- Alammooduli töölehe kirjet pole pearaamatusse üle kantud:

    - See põhjus kehtib ainult vabas vormis arvete puhul.
    - Kasutage **alammooduli töölehe kirjete lehte, mida pole veel üle kantud**, et kanda kirje pearaamatusse üle. Vabas vormis arvet saab seejärel tagasi pöörata või parandada, kui paranduste funktsioon on lubatud.

- Tasakaalustus:

    - Kanne (nt arve või makse) tasakaalustatakse või märgitakse tasakaalustamiseks.

        - Saate kontrollida, kas kanne on tasakaalustatud või tasakaalustamiseks märgitud, valides **Vaata tasakaalustusi** või **Tasakaalustus \> Tasakaalustuse ajalugu** lehel **Kliendikanded**.
        - Tasakaalustuse saate tühistada ka leheküljel **Hankija kanded** lehel (**Tasakaalustus \> Tasakaalustuse tagasivõtmine**) kui üks kannetest tuleb tühistada.

- Kanne sisaldab mitut alam pearaamatukannet, mis sisestati sama kandenumbriga (üks kande väljaminek).
- Arve pole kinnitatud:

    - Kui **Kinnitus** märkeruudus pole märgitud ruut Kinnitus, ei saa arvet tagasi võtta.

        - Sel juhul ei viita kinnitus töövoo protsessi kinnitustele, vaid arve **Kinnitamise** suvandile arvel. Selle valiku abil saate vältida arve tasumist. Ehkki seda valikut kasutatakse tavaliselt ostureskontros, on see saadaval ka töölehtede kaudu sisestatud müügireskontro arvete puhul.

- Kandel on emaarve, mis on parandatud (India lokaliseerimine).
- Kanne sisaldab kliendikontot, kuid on ümber pööratud valelt leheküljelt, nt **Kanded \<main account\>** jaoks lehel:

    - Nagu sel põhjusel soovitatakse, isegi kui hulgipööramise funktsioon on sisse lülitatud, saab mõningaid alam pearaamatukandeid tühistada ainult konkreetsetelt lehtedelt.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Kannete tüübid, mida ei saa tühistada

Järgmist tüüpi kandeid ei saa tagasi pöörata:

- Välisvaluuta ümberarvutamine:

    - Erinevalt pearaamatu välisvaluuta ümberarvutamisest ei saa müügireskontrot ja ostureskontro välisvaluuta ümberarvutamisest tühistada. Selle asemel tuleb ümberhindamine uuesti käivitada, kasutades arve kuupäeva. Sel juhul kasutab ümberhindamine arve kuupäeva vahetuskurssi ning toob realiseerimata kasumi või kahjumi 0 (nulliks). Seetõttu sarnaneb tulemus eelmise ümberhindamise ümberpööramise tulemusega. Pange siiski tähele, et sama summat ei tühistata, kui arvel on muudetud vaikimisi vahetuskurssi.

- Kanne, millega on korrigeeritud maksu kinnipidamist
- Müügi kliendiarve:

    - Hankija arve tühistamiseks tuleb luua kreeditarve. Lisateavet selle kohta, kuidas luua vastupidist kannet, vt [Müügitagastus](../../supply-chain/warehousing/sales-returns.md).

- Käskveksel
- Registreerige sularahakanded
- Täpsem korrigeerimine
- Viivisearve
- Kogumiskirjad
- Panga akreditiiv
- Eksportsaadetis
- Tulu tuvastamise päevik:

    - Kui tulu tuvastatakse tuluarvestustöölehe kaudu, sisestatakse see kanne ainult pearaamatukontodele. Seetõttu ilmuvad nad nii, nagu oleks need ainult pearaamatukirjed. Neid kirjeid ei saa tagasi võtta, kuna tulugraafikut ei avata uuesti tulu äratundmiseks.

## <a name="cash-and-bank-management"></a>Sularaha- ja pangahaldus

Mitu kandetüüpi uuendavad panga alamlegerit üldise töölehe kaudu. Näited hõlmavad hankijamakseid, kliendimakseid ja pangaülekandeid.

Kui hulgipööramise funktsioon on välja lülitatud, saab kandeid tühistada ükshaaval kus avate **Panga kontod** lehe kontrolliks või deposiidiks või **kliendikannete** lehel kliendimaksete jaoks.

Kui hulgipööramise funktsioon on sisse lülitatud, saab ühe või mitu pearaamatukannet nüüd tagasi võtta **Kannete** leheküljelt ja töölehelt, millelt kanne proovibilanssi sisestati. Hankija deposiiti saab siiski tühistada ainult pangakontolt. Lisaks, kliendikandeid ei saa tühistada raamatu **kannetest \<main account\>** jaoks lehel. Kuid neid saab tagasi pöörata leheküljel **Kanded**.

Pange tähele, et mõningaid kandeid ei saa üldse tühistada. Näited hõlmavad elektroonilist hankijamakset.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Kannete tühistamise põhjused

Kandeid ei saa järgmistel põhjustel tagasi pöörata:

- Rahandusperiood on ootel või jäädavalt suletud:

    - Kui tühistamise kuupäev on rahandusperioodis, mis pole avatud, ei saa kannet tühistada.
    - Kui kanne toetab tühistamiskuupäeva sisestamist, saab kannet siiski tagasi võtta, muutes tagasipööramise kuupäeva avatud perioodiks.

- Pearaamatu aasta lõpu sulgemisprotsess on käitatud:

    - Kande raamatupidamiskuupäev on rahandusaastas, mis on läbinud pearaamatus aasta lõpetamise. Kuigi rahandusaasta periood võib siiski olla avatud, ei saa kannet tühistada, kui rahandusaasta kohta on käitatud aasta lõpetamise sulgemisprotsess. Finantsaasta olek erineb selle perioodi olekust.
    - Aasta lõpu sulgemise saab tühistada ja seejärel kande tühistada. See lähenemine ei pruugi olla suvand. Sõltuvalt fiskaal sulgemise protsessi olekust, võib olla lihtsam sisestada tagasipööratud kanne käsitsi kas suletud rahandusaasta või järgmise rahandusaasta avatud perioodi. Kui uus kanne sisestatakse finantsaasta avatud perioodi, mis on läbinud aasta lõpu sulgemise protsessi, tuleb aasta lõpu sulgemine uuesti käivitada.

- Tasakaalustus:

    - Kanne (nt arve või makse) tasakaalustatakse või märgitakse tasakaalustamiseks.

        - Saate kontrollida, kas kanne on tasakaalustatud või tasakaalustamiseks märgitud, valides **Vaata tasakaalustusi** või **Tasakaalustus \> Tasakaalustuse ajalugu** lehel **Hankija kanded** või **Kliendikanded**.
        - Tasakaalustuse saate tühistada ka leheküljel **Hankija kanded** lehel **Kliendi kanded** (**Tasakaalustus \> Tasakaalustuse tagasivõtmine**) kui üks kannetest tuleb tühistada.

- Kanne sisaldab mitut alam pearaamatukannet, mis sisestati sama kandenumbriga (üks kande väljaminek).
- Vahekonto kanded:

    - Kui kanne on seotud kontomaksega, ei saa seda tühistada.
    - Kui sildmakse tuleb tühistada, tuleb makse esmalt pangale üle võtta. Makse saab seejärel tagasi pöörata, kui see vastab teistele kinnitamiskriteeriumidele.

- Kanne sisaldab pangakontot, kuid on ümber pööratud lehekülje **Kannetelt \<main account\>** või valelt alamtüübilt, nt Müügireskontrovõi Ostureskontro:

    - Nagu sel põhjusel soovitatakse, isegi kui hulgipööramise funktsioon on sisse lülitatud, saab mõningaid alam pearaamatukandeid tühistada ainult konkreetsetelt lehtedelt.

- Panga välisvaluuta ümberarvutamine:

    - Panga välisvaluuta ümberarvutamise saab tühistada. Ümberpööramine võib siiski olla takistatud, kui lõpetate tagasipööramised kronoloogilisest järjekorrast välja. Kui käivitate näiteks ümberhindamise märtsis ja aprillis, ei saa märtsi ümberhindamist tühistada enne aprilli ümberhindamise toimumist.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Kannete tüübid, mida ei saa tühistada

Järgmist tüüpi kandeid ei saa tagasi pöörata:

- Hankijamaksed, mis tehti elektrooniliste ülekannetena (EFT-d)
- Võlatähed
- Käskvekslid

## <a name="fixed-assets"></a>Põhivarad

Mitu kande tüüpi värskendab põhivara alamhaldurit. Näited hõlmavad soetamist ja kulumit.

Kui hulgipööramise funktsioon on välja lülitatud, saab kandeid tühistada ükshaaval lehelt **Hankija kanded** lehelt **Põhivarakanded**, sõltuvalt kande tüübist.

Kui hulgipööramise funktsioon on sisse lülitatud, saab ühe või mitu parandatud kannet nüüd tagasi võtta **Kannete** leheküljelt ja töölehelt, millelt kanne proovibilanssi sisestati.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Kannete tühistamise põhjused

Kandeid ei saa järgmistel põhjustel tagasi pöörata:

- Rahandusperiood on ootel või jäädavalt suletud:

    - Kui tühistamise kuupäev on rahandusperioodis, mis pole avatud, ei saa kannet tühistada.
    - Kui kanne toetab tühistamiskuupäeva sisestamist, saab kannet siiski tagasi võtta, muutes tagasipööramise kuupäeva avatud perioodiks.

- Pearaamatu aasta lõpu sulgemisprotsess on käitatud:

    - Kande raamatupidamiskuupäev on rahandusaastas, mis on läbinud aasta lõpetamise. Kuigi rahandusaasta periood võib siiski olla avatud, ei saa kannet tühistada, kui rahandusaasta kohta on käitatud aasta lõpetamise sulgemisprotsess. Finantsaasta olek erineb selle perioodi olekust.
    - Aasta lõpu sulgemise saab tühistada ja seejärel kande tühistada. See lähenemine ei pruugi olla suvand. Sõltuvalt fiskaal sulgemise protsessi olekust, võib olla lihtsam sisestada tagasipööratud kanne käsitsi kas suletud rahandusaasta või järgmise rahandusaasta avatud perioodi. Kui uus kanne sisestatakse finantsaasta avatud perioodi, mis on läbinud aasta lõpu sulgemise protsessi, tuleb aasta lõpu sulgemine uuesti käivitada.

- Soetamised:

    - Kui soetamine toimus ostutellimuse hankijaarvel, tuleb tagasipööramine teha hankija kreeditarve sisestamisega. Lisateavet selle kohta, kuidas sisestada vastupidist kannet, vt [ostu tagastustellimuse loomine](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Soetamine toimus projektikandel.
    - Soetusmaksumust ei saa tühistada pärast vara kulumise sisestamist. Amortisatsioon tuleb tagasi pöörata, enne kui omandamist saab tagasi pöörata.
    - Kui põhivara väärtusmudeli või kulumiraamatu olek ei ole avatud, ei saa kannet tühistada.

- Likvideerimised:

    - Likvideerimine toimub vabas vormis arve kaudu:

        - Kui see sisaldab põhivara, on vabas vormis arve parandus blokeeritud. Kui aga vara likvideeritakse töölehe kaudu, saab vabas vormis arve põhivarakirjelt tagasi võtta.

    - Kui põhivara väärtusmudeli või kulumiraamatu olek ei ole avatud, ei saa kannet tühistada.

- Amortisatsioon:

    - Kulumise **saab** tagasi võtta, kui sisestatakse ka järgnev kulum. Te saate siiski hoiatuse, sest see lähenemine pole hea tava.
    - Kui põhivara väärtusmudeli või kulumiraamatu olek ei ole avatud, ei saa kannet tühistada.

- Kande kandekuupäeval või hilisemal kuupäeval on olemas kindla vara ja vararaamatu kanded (või tühista kanded).
- Kanne sisaldab vara kontot, kuid on ümber pööratud lehekülje **Kannetelt \<main account\>** või valelt alamtüübilt, nt Müügireskontrovõi Ostureskontro:

    - Nagu sel põhjusel soovitatakse, isegi kui hulgipööramise funktsioon on sisse lülitatud, saab mõningaid alam pearaamatukandeid tühistada ainult konkreetsetelt lehtedelt.
    - Kui soetamine toimub mitteostutellimuse hankijaarvel või hankija arve töölehel, saab seda tagasi võtta ainult ostureskontro **hankija kannete** leheküljelt.
    - Kui vara soetakse varade aruandest, saab selle tühistada varade halduse lehel **Kohustuste kanded**.
