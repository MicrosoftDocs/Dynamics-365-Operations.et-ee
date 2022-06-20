---
title: Ostureskontro arvete võrdlemise häälestus
description: See artikkel annab teavet, kuidas seadistada Ostureskontro arvete vastendamise kinnitamist.
author: abruer
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86cc5cf688e3b66cf976fc7f507bd8f8df757612
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904955"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Ostureskontro arve vastenduse kinnitamise seadistamine

[!include [banner](../../includes/banner.md)]

Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine. Kui teie juriidiline isik jälgib tasude abil kulusid (nt veokulu), siis veenduge, et on valitud konfiguratsioonivõti Tasud.  Ostureskontro arvete võrdlemine on hankija arve, ostutellimuse ja toote sissetuleku teabe vastavusse viimise protsess. Nende dokumentide vahelisi erinevusi nimetatakse vastendamise lahknevusteks. Vastavusseviimise lahknevusi võrreldakse määratud hälvetega. Kui võrdlemise lahknevus ületab lubatud kõikumisprotsendi või summa, kuvatakse võrdlemise hälbe ikoonid lehel **Hankija arve** ja lehel **Arvete võrdlemise üksikasjad**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Määratlege, millist arvete võrdlemise kinnitamist kasutada
Saadaval on neli erinevat tüüpi võrdlemise kinnitamist. 

- **Reataseme võrdlemine** – kõige levinum võrdlemise tüüp on rea võrdlemine. Reataseme võrdlemine võib olla kahe-või kolmesuunaline võrdlemine. Juriidilisele isikule saab seadistada vaikimisi reataseme võrdlemise **Ostureskontro parameetri** lehel. Kahesuunaline võrdlemine võrdleb arve ühikuhinda ostutellimuse ühikuhinnaga. Kolmesuunaline võrdlemine võrdleb lisaks arve kogust võrreldava toote sissetuleku kogusega.
- **Arvesummade võrdlemine** – arve koondsummade võrdlemine ostutellimuse koondsummadega. Seda tüüpi arvete vastavusseviimine sisaldab kõige vähem üksikasju, seega saab selle suvandi abil määrata juhtelemendid, mis minimeerivad töötajate arvete vastavusseviimise teabe ülevaatamisele kuluvat aega. Võrreldakse kuut kogusummat, sealhulgas vahesummat, kogu allahindlust, tasusid, käibemakse, ümardamist ja arve summat. Süsteem kontrollib, kas mõni nendest väärtustest arvel erineb eeldatavatest summadest rohkem kui vastuvõetav hälve.
- **Tasude võrdlemine** – arvel olevate tasude andmeid (summad) võrreldakse ostutellimusel olevate tasude andmetega (summadega)
- **Koguhindade võrdlemine rea kaubaga** – selline võrdlemine on kasulik ettevõtetele, kas saavad harilikult ühe ostutellimuse rea kohta mitu arvet. Kui saate ostutellimuse rea kohta tavaliselt ainult ühe arve, ei ole seda tüüpi võrdlemine vajalik. See võrdlemine nõuab, et kahe- või kolmesuunaline võrdlemine on lubatud ja toimib mitteületatava netosumma kinnitamisena, põhinedes hälbeprotsendil ja -summadel.  Selline võrdlemine võrdleb iga arve rea ja kõikide ootel ja varem sisestatud arve ridade netosumma hinnateavet asjakohase ostutellimuse rea netosummaga. Netosumma määratakse järgmise valemiga: (ühiku hind * rea kogus) + rea tasud – rea allahindlused. Koguhindasid protsendi järgi vastavusse viies võrdleb süsteem väärtusi kandevaluutat kasutades. Koguhindasid summa järgi vastavusse viies võrdleb süsteem väärtusi arvestusvaluutat kasutades.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Parmeetrite seadistamine arvete võrdlemise kinnitamise lubamiseks
1. Avage **Ostureskontro > Seadistus > Ostusreskontro parameetrid**.
2. Valige vahekaart **Arve kinnitamine**.
3. Valige või tühjendage märkeruut **Luba arvete võrdlemise kinnitamine**.
    * Valige, kas enne arvete võrdlemisel erinevusi sisaldava arve sisestamist on nõutav kinnitus. Kui see on seatud valikule **Luba hoiatusega**, kuvatakse visuaalne näit, kui arvete võrdlemise erinevus ületab lubatud hälbe. Saate arve siiski sisestada. Töövoogude kasutamiseks koos arvete võrdlemise kinnitamisega veenduge, et väli **Lahknevustega arvete sisestamine** on määratud suvandile **Luba hoiatusega**, et vältida korduvat kinnitamist.  
    * Valige väljalt **Arve päise võrdlemise oleku automaatne värskendamine**, kas süsteem võrdleb arve andmete sisestamisel automaatselt. Soovitatav säte on **Jah**, v.a juhul, kui teil on tekkinud andmete sisestamise jõudluse probleeme. Automaatsete värskenduste keelamine võib lubada süsteemi jõudluse kiirenemist, kuna arvete võrdlemise kontrollimine jäetakse andmesisestusel vahele. Andmete sisestamise ametnik peab arvete võrdlemise olekut käsitsi värskendama, et näha arvete võrdlemise kinnitamise tulemusi, kui see on seatud väärtusele **Ei**.  
4. Seadke **Arvesummade võrdlemine**.
5. Märkige või tühjendage märkeruut **Võrdle arvesummasid**, et võrrelda tegelikke arvesummasid eeldatavate kogusummadega.
    * Valige, kas kuvada ikoon, kui erinevus ületab arvete võrdlemisel lubatud hälbe. Saate valida ikooni kuvamise, kui positiivne erinevus ületab lubatud hälbe, või kui positiivne või negatiivne erinevus ületab lubatud hälbe.  
    * Näide: hälve on 5 protsenti ja ostutellimuse arve kogusumma on 100.00. Seetõttu kuvatakse hinna vastavuse ikoon, kui arve kogusumma ületab 105.00. Kui teete valiku **Kui kõikumisest suuremad või väiksemad**, kuvatakse samuti ikoon, kui arve summa on väiksem kui 95,00.  
6. Sisestage väljale **Arve kogusummade hälbe protsent** aktsepteeritava hälbe protsent. See väärtus on ettevõtte vaikeväärtus. Selle väärtuse saab teatud hankijate puhul alistada, kasutades lehte **Arve kogusumma hälbed**. Teavet selle kohta, kuidas alistada arve kogusummade kõikumisprotsent konkreetse hankija jaoks, vt selles artiklis hiljem jaotisest "Hankijatele vastavate arve kogusummade seadistamine".
7. Seadke **Hinna ja koguse võrdlemine**.
8. Valige väljalt **Rea vastavusse viimise poliitika** väärtus, mida kasutada vaikepoliitikana juriidilise isiku puhul, kellega töötate. **Pole nõutav** tähendab, et üksiku arverea hindade kinnitamine ostutellimuse hinnaga või arve koguste kinnitamine saatelehe kogustega pole nõutav. **Kahesuunaline võrdlemine** tähendab, et arveridade kontrollimine on nõutav, kuid kontrollimine hõlmab ainult ostutellimust ja tarnija arve dokumente. Toote sissetulekut vastavusse viimise kontrollimisel ei arvestata. **Kolmesuunaline võrdlemine** tähendab, et arve ühiku netohinda võrreldakse ostutellimuse ühiku netohinnaga ja ühtivat toote sissetuleku kogust võrreldakse arve kogusega.
9. Teistsuguse võrdlemise taseme rakendamise lubamiseks kauba, hankija, hankija ja kauba kombinatsiooni või ostutellimuse rea puhul valige väärtus väljalt **Luba vastavusse viimise poliitika alistamine**. Juriidilise isiku rea vastavusse viimise poliitika saab alistada kindla hankija, kauba või hankija ja kauba kombinatsiooni puhul lehel **Vastavusse viimise poliitika**
    * Kui kasutate rea vastavusse viimise poliitika kahesuunalist vastavusse viimist või kolmesuunalist vastavusse viimist, saate seadistada hinnakõikumisprotsendid juriidilise isiku, kaupade ja hankijate puhul lehel **Kauba hinna kõikumine**. Juriidilise isiku vaikimisi hinna kõikumine seatakse kahe-ja kolmesuunalise vastavusse viimise jaoks nullprotsendile. Kui hankijaarveid ostutellimuste teabega võrreldakse, otsitakse sobivat hinnakõikumisprotsenti.   
10. Rea kaupade hinna kogusummade vastavusse viimiseks arvetel valige väärtus väljalt **Hinna kogusumma vastendamine**. Seda tüüpi vastendamine on kasulik, kui hankija saadab sama ostutellimuse rea puhul mitu arvet. Saate võrrelda iga arve rea ja kõikide ootel ja varem sisestatud arve ridade netosumma hinnateavet asjakohase ostutellimuse rea netosummaga.  Valikute **hulka** kuuluvad **pole**, **protsent**, summa **või protsent ja summa**.
11. Sisestage väljale **Ostuhinna kogusumma hälbe protsent** hälbe protsent, millega nõustute. See väli on saadaval üksnes juhul, kui väljal **Hinna kogusumma võrdlemine** on valitud **Protsent** või **Protsent ja summa**.
12. Sisestage väljale **Ostuhinna kogusumma hälve** summa arvestusvaluutas. See väli on saadaval üksnes juhul, kui väljal **Hinna kogusumma võrdlemine** on valitud **Summa** või **Protsent ja summa**.
13. Valige väljalt **Kogusumma võrdlemise ikooni kuvamine**, millal kuvada ikoon, kui erinevus ületab arve vastendamisel lubatud ühiku netohinna hälbe. Ikooni saab kuvada, kui positiivne erinevus ületab lubatud hälbe, või kui positiivne või negatiivne erinevus ületab lubatud hälbe.
Näide: hälve on 5 protsenti ja ostutellimuse rea hinna kogusumma on 10.00. Seetõttu kuvatakse hinna vastavuse ikoon, kui arve rea hinna kogusumma ületab 10.50. Kui teete valiku **Kui kõikumisest suuremad või väiksemad**, kuvatakse ikoon ka siis, kui arve rea hinna kogusumma on väiksem kui 9,50.
13. Häälestage kulude **võrdlemine**.
14. Tegelike tasude võrdlemiseks eeldatavate tasudega, tuginedes ostutellimuse teabele, märkige ruut **Võrdle tasusid**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Seadistage ühiku hinnakõikumisprotsendid
Lubatud hinnakõikumise protsentide määramiseks avage **Ostusreskontro > Seadistus > Arvete võrdlemise seadistus > Hinnakõikumised**. Kui kasutate rea vastavusse viimise poliitika kahesuunalist või kolmesuunalist vastavusse viimist, saate juriidilise isiku, kaupade ja hankijate puhul seadistada hinnakõikumisprotsendid. Kui hankijaarveid ostutellimuste teabega võrreldakse, otsitakse sobivat hinnakõikumisprotsenti. Vaikimisi toimub otsimine järgmises järjekorras.
* Tabel/tabel
* Tabel/grupp
* Tabel/kõik
* Grupp/tabel
* Grupp/grupp
* Grupp/kõik
* Kõik/tabel
* Kõik/grupp
* Kõik/kõik

Vaikimisi on juriidilise isiku hinnakõikumine 0 protsenti ja see hinnakõikumine rakendub kõigile kaupadele ja kontodele (Kõik, Kõik). Ettevõtte vaikehinnakõikumise kirjet ei saa kustutada.

Vaikimisi on negatiivsed hinnaerinevused lubatud. Kuid te ei saa sisestada hinnakõikumisprotsendina negatiivset arvu. Negatiivse hinna hälbeprotsendi jälgimiseks tehke lehe **Ostureskontro parameetrid** väljal **Kuva tasude võrdlemise ikoon** valik **Kui hälbest suuremad või väiksemad**. Seejärel sisestage lehel **Hinnakõikumised** hinnakõikumisprotsendid

## <a name="set-up-matching-policy-override"></a>Vastavusse viimise poliitika alistamise seadistamine

Minge ostureskontro **> ja > häälestage vastavusse viimise poliitika >** **·** **vastavusse viimise poliitika abil, et määrata ostutellimuse lehe ridadele vastavusse viimise poliitika välja vaikesisestus.** See on valikuline seadistus. Kasutage seda lehekülge, et seadistada kaupade, hankijate või kauba- ja hankijakombinatsioonide kahe- või kolmepooleline vastavusse viimine. Need kirjed võimaldavad teil määratleda üksikasjalikumaid vastavusse viimise poliitikaid kui lehel **Ostusreskontro parameetrid** määratud juriidilise isiku vastavusse viimise poliitika. Vaikeseadistatud juriidilise isiku rea vastavusse viimise poliitika rakendub kõigile kaupadele ja hankijatele, välja arvatud neile, millele on sel lehel määratud muu rea vastavusse viimise poliitika.

Valige sellel lehel **Vastavusse viimise poliitika tase**. Valige vastavusse viimise poliitika hierarhia tase, millele soovite rea vastavusse viimise poliitika seadistada.

- **Kaup ja hankija** – saate määrata vastavusse viimise poliitika kindlatelt hankijatelt ostetud kindlatele kaupadele.
- **Kaup** – saate määrata mis tahes hankijalt ostetud kaupade vastavusse vimise poliitika, välja arvatud neile, mis on määratud kauba ja hankija tasemel.
- **Hankija** – saate määrata kindlatelt hankijatelt ostetud kõikide kaupade vastavusse viimise poliitika, välja arvatud neile, mis on määratud kauba ja hankija tasemel.
  
Järgnevat hierarhiat kasutatakse vastavusse viimise poliitika määratlemiseks, mida kasutatakse järgmiseks.
  *  Kaup ja hankija
  *  Üksus
  *  Tarnija
  *  Juriidiline isik
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Hankijatele arve kogusummade võrdlemise kõikumiste seadistamine

Avage **Ostusreskontro > Seadistus > Arvete võrdlemise seadistus > Arvesummade lubatud kõikumised**, et määrata hankijaspetsiifilised arvesummade võrdlemised. Võrdlemise kalkulatsioon kasutab arvesummade lubatud kõikumisprotsenti hankija kontolt, mis määratakse tellimuse kontona hankija arvel. Kui hankija kontol pole arve kogusummade jaoks määratud kõikumise protsenti, kasutatakse lehel **Ostureskontro parameetrid** juriidilise isiku jaoks määratud arvesumma lubatud kõikumisprotsenti.

1. Üksikhankijatele vaikeseadistatud kõikumisi ületavate hankimiste määramiseks valige **Hankija konto**
2. Sisestage hälbe protsent, mida olete nõus aktsepteerima selle hankija puhul.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
