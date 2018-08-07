---
title: Finantsaruannete vaatamine ja kujundamine
description: See artikkel sisaldab harjutusi, mis selgitavad teile Microsoft Dynamics 365 for Finance and Operationsis finantsaruannete vaatamist ja loomist.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 86597a81b4dcfb14cbc88667fbb1db214133c6e5
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-design-financial-reports"></a>Finantsaruannete vaatamine ja kujundamine

[!include [banner](../includes/banner.md)]

See artikkel sisaldab harjutusi, mis selgitavad teile Microsoft Dynamics 365 for Finance and Operationsis finantsaruannete vaatamist ja loomist. Finantsaruandlus hõlmab vaatamist Dynamics 365 for Finance and Operationsis ja korra klõpsatavat aruandekujundajat, mis võimaldab teil finantsaruandeid luua ja redigeerida.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>1. harjutus: vaikimisi finantsaruande loomine ja uurimine
-----------------------------------------------------------

Selle harjutuse puhul loote ja uurite olemasolevat vaikearuannet. See aruanne sisaldab kõiki kontosid ja ka kontode konto atribuute. Saate minna kande üksikasjadesse süvitsi, rakendada dimensioonifiltreid, muuta aruande valuutat. Esmalt värskendame finantsaruandluse dimensioonide kuvamise järjestust. See võimaldab teil valida, kuidas dimensioone kuvatakse, ja seda mitte ainult finantsaruannete kujundamisel ja kuvamisel.

1.  Avage **Finantsdimensiooni konfiguratsioon rakenduste integreerimiseks** pearaamatu osas **Kontoplaani dimensioonid**.
2.  Teisaldage dimensioone järgmises järjestuses.
    1.  Põhikonto
    2.  Äriüksus
    3.  Kulukeskus
    4.  Osakond

    Märkus. Teised dimensioonid võivad jääda järjestusse, milles need praegu on.
3.  Salvestage dimensiooni konfiguratsioon. Järgmisena loome aruande ja uurime aruande andmeid.
4.  Avage **Finantsaruanded** pearaamatu osas **Päringud ja aruanded**.
5.  Valige rida aruande puhul, mille nimi on **Pearaamatu üksikasjad – vaikimisi.**
6.  Valige suvand **Redigeeri.** Märkus. Teil palutakse korra klõpsatav aruandekujundaja alla laadima ja sisse logima. Kasutage sisselogimiseks oma identimisteavet.
7.  Muutke baasaastaks 2012 ja valige **Loo**. Kui aruanne on aruandekoosturis loodud, avatakse see uuel brauseri vahekaardil. Saate aruannet uurida kas brauseri vahekaardil või minna oma algse brauseri vahekaardile ja avada aruande sealt, valides selle loendist **Finantsaruanded**.
8.  Valige avatud aruandes üks summadest, et minna aruande konto üksikasjadesse süvitsi.
9.  Kui olete konto üksikasjades, valige konto andmetega ja **minge süvitsi aruande kande tasemele**. Aruande kande tasemel näete selle aruande kujundusse kaasatud atribuute. Kandest ja kontost olenevalt võidakse kuvada mõni atribuut või kõik atribuudid.
10. Sulgege aruande kande tasand.
11. Valige sama või teine konto ja **avage kanded.** Kanded on filtritud valitud konto perioodi, aasta ja konto + dimensiooni kombinatsiooni järgi. Kannetest saate valida kande muu teabe uurimise.
12. Sulgege kanded. Finantsaruandes saate andmeid vaadata kas eri perioodi ja aasta või eri rakendatud atribuutide ja dimensioonide järgi. Seda tehakse suvandit **Aruandevalikud** kasutades.
13. Valige suvand **Aruandevalikud**.
14. Valige **Lisa dimensioonifilter** ja valige **Äriüksus**.
15. Sisestage väljale 001 ja valige **OK**. Aruandes kuvatakse nüüd ainult äriüksuse 001 andmed. See on aruande isikupärastatud vaade ja pole saadaval teistele vaatamiseks.
16. Sulgege filtritud aruanne. Finantsaruandeid saab kuvada mis tahes valuutas, mis on Dynamics 365 for Finance and Operationsisse lisatud.
17. Valige **Valuuta**, seejärel valige **EUR.** Aruanne kuvatakse nüüd eurodes. Aruande kujundusse kaasatud mis tahes valuutakoodid või -tähised kuvatakse nüüd rakendatud valuutas. Kui valuuta puhul pole ühtegi valuutatähist määratletud, siis valuuta tähist ei kuvata.
18. Sulgege aruanne **Pearaamatu üksikasjad**.
19. Sulgege **aruande kujundaja**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>2. harjutus: täiendavate konto atribuutide lisamine aruande kujundusse
Selles harjutuses muudate olemasolevat vaikearuannet. Värskendate nii readefinitsiooni kõiki kontosid hõlmama kui ka veeru definitsiooni konto atribuute hõlmama. Kui värskendused on lõpetatud, saate luua äsjaloodud aruande ja aruannet uurida. Alustame loendist Finantsaruanded.

1.  Avage **Finantsaruanded** pearaamatu osas Päringud ja aruanded.
2.  Valige rida aruande puhul, mille nimi on **Proovibilansi kokkuvõte – vaikimisi**
3.  Valige suvand **Redigeeri**. **Proovibilansi kokkuvõte – vaikimisi** avaneb aruande kujundajas.
4.  Valige **Fail**, seejärel **Salvesta nimega** ja pange aruande nimeks Üksikasjalik proovibilanss atribuutidega. Märkus. Aruande loomisel mis tahes ajal aruandekujundajas uuendatakse finantsaruannete loendit Dynamics 365 for Finance and Operationsis.
5.  Valige aruande definitsioonist readefinitsiooni ikoon, et avada **Proovibilanss – vaikimisi readefinitsioon**.
6.  Salvestage readefinitsioon kui **Üksikasjalik proovibilanss atribuutidega**.
7.  Suunates kursori reale 50, valige **Redigeeri**, seejärel **Sisesta read dimensioonidest**. Sisesta read dimensioonidest võimaldab teil valida, milliseid dimensioone soovite readefinitsiooni kaasata. Selle harjutuse puhul loome readefinitsiooni põhikonto abil.
8.  Veenduge, et **Põhikonto** sisaldab kõiki ampersande ja valige **OK**. Readefinitsioon sisaldab nüüd kõiki USMF-i juriidilise isiku põhikontosid.
9.  Kerige alla reani 11110 ja kustutage rida 11110.
10. Valige reas 11080 **--- (allkriipsuga summad)**.
11. Sisestage reale 11140 veerus B **kõikide kontode kogusumma**.
12. Valige veerus C ripploendist suvand **TOT**.
13. Sisestage veergu D **50:11080**.
14. **Salvesta** rea definitsioon. Rea definitsioon sisaldab nüüd kõiki kontosid pluss kokkuvõtterida kõikide kontode koos lisamiseks. Järgmisena värskendame veeru definitsiooni täiendavaid konto atribuute hõlmama.
15. Valige aruande definitsioonist **Üksikasjalik proovibilanss atribuutidega** veeru definitsiooni ikoon, et avada veeru definitsioon **Proovibilansi kokkuvõte – vaikimisi** .
16. Salvestage veeru definitsioon kui **Üksikasjalik proovibilanss atribuutidega**. Veeru definitsioon sisaldab finantsandmete veerge, kirjelduse veergu ja arvutusveerge. Kontode kohta täiendavate üksikasjade pakkumiseks lisame veeru definitsiooni atribuudi veerud.
17. Veeru definitsiooni lisatakse järgmised atribuudid.
    -   Töölehe number
    -   Töölehe kirjeldus
    -   Kande kuupäev
    -   Looja:
    -   Viimati muutis

18. Valige I veerus veeru tüübi puhul suvand **ATTR**. Seejärel valige atribuudi kategooriana **Töölehe number**.
19. Jätkake veergude lisamist ülejäänud atribuutide puhul.
20. Lisage reale **Päis 2** kirjeldusi iga uue loodud veeru puhul.
21. Salvestage veeru definitsioon. Nüüd kui rea definitsiooni ja veeru definitsioon on värskendatud, tuleb need aruande definitsiooni lisada.
22. Valige aruande definitsioonist **Üksikasjalik proovibilanss atribuutidega** üksikasjalik proovibilanss koos atribuutidega nii readefinitsiooni kui ka veeru definitsiooni puhul.
23. Muutke baasaastaks **2012.**
24. **Salvesta** aruande definitsioon ja **loo**. Pärast aruande loomist ja avamist saate aruannet uurida, nagu esimeses harjutuses. Minge eri kontodel süvitsi, et näha, kuidas täiendavaid atribuute kuvatakse.
25. Sulgege aruanne **Üksikasjalik proovibilanss atribuutidega**.
26. Sulgege **aruande kujundaja**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>3. harjutus: mitmedimensioonilise aruande loomine aruandluspuu abil
Selle harjutuse puhul muudate olemasolevat vaikearuannet. Saate luua aruandluspuu ja lisada aruande definitsiooni kulukeskuse/osakondade kasumiaruande loomiseks. Kui värskendused on lõpetatud, saate luua kulukeskuse/osakondade kasumiaruande ja uurida aruannet aruandluspuu abil. Alustame loendist Finantsaruanded.

1.  Avage **Finantsaruanded** pearaamatu osas Päringud ja aruanded.
2.  Valige rida aruande puhul, mille nimi on **Kasumiaruanne – vaikimisi**
3.  Valige suvand **Redigeeri**. **Kasumiaruanne – vaikimisi** avaneb aruande kujundajas.
4.  Osutage menüüs **Fail** suvandile **Uus** ja seejärel klõpsake suvandit **Aruandluspuu definitsioon**
5.  Klõpsake menüüs **Redigeeri** suvandit **Sisesta aruandlusüksused dimensioonidest**...
6.  Tühjendage märkeruudud kõikide dimensioonide, välja arvatud suvandi **Kulukeskus** puhul.
7.  Klõpsake dimensiooni Kulukeskus puhul välja **Dimensioonist**, sisestage **007** ja seejärel vajutage tabeldusklahvi. Sisestage väljale **Dimensioonini** number **018**.
8.  **Salvesta** tulemuste puu nimega **Kulukeskused osakonniti.** Nüüd kui aruandluspuu on loodud, saate muuta aruandluspuud nii, et see sisaldaks uusi ümberarvestuse üksusi, turundust, toimingud ja jaemüüki.
9.  Klõpsake menüüs **Aken** suvandit **Kulukeskused osakonniti**. (Kui aruandluspuu on suletud, valige see navigeerimispaani suvandi Aruandluspuu definitsioonid hulgast.)
10. Klõpsake üksust number kaks, **Kaubandusnäitused**, ja klõpsake ikooni **Sisesta aruandlusüksus**.
11. Topeltklõpsake tühjal real üksuse veergu ja valige **USMF**.
12. Sisestage veergudesse B ja C **Turundus**.
13. Klõpsake üksust number viis, **Teenusetoimingud**, ja paremklõpsake. **Valige Sisesta aruandlusüksus**.
14. Korrake etappi 11.
15. Sisestage veergudesse B ja C **Toimingud**.
16. Klõpsake üksust number kaksteist, **Väljund**, ja paremklõpsake. Valige **Sisesta aruandlusüksus**.
17. Korrake etappi 11.
18. Sisestage veergudesse B ja C **Jaemüük**. Pange tähele, et üksused Turundus, Toimingud ja Jaemüük kuvatakse samal tasemel kui praegused ümberarvestuse üksused. Järgmisena korraldatakse uued üksused. Aruandlusüksusi korraldatakse paremklõpsatavate suvandite, edendamise ja alandamise või pukseerimise kaudu.
19. Veenduge, et üksus kolm, **Kaubandusnäitused**, oleks aktiivne ja paremklõpsake.
20. Valige **Alanda aruandlusüksus**. Pange tähele, et üksus kuvatakse nüüd suvandi **Turundus** tütrena.
21. Klõpsake üksust neli, **Turundus****kampaania**, ja paremklõpsake.
22. Valige **Alanda aruandlusüksus**.
23. Klõpsake graafilisel kuval suvandit **Teenusetoimingud**. Vajutage ja hoidke vasakut hiirenuppu all, lohistades samas üksust suvandini **Toimingud**. Üksuse vabastamiseks ümberarvestusse Toimingud vabastage hiire vasak nupp. Korrake seda suvandite **Tootmine, Kvaliteedikontroll, Logistika, Hange ja Haldus** puhul.
24. Muutke **Väljund**, **Ülem**, **Mall** ja **Võrgus** suvandi **Jaemüük** tütardeks, neid alandades või pukseerides.
25. Salvestage tulemuseks saadud reorganisatsioon. Nüüd kui aruandluspuu on loodud ja korraldatud, saab selle aruande definitsiooni lisada.
26. Valige menüüs **Aken** aruande definitsiooni avamiseks suvand **Kasumiaruanne – vaikimisi**.
27. Klõpsake rippnoolt **Puu tüüp** ja valige suvand **Aruandluspuu**.
28. Klõpsake puu rippnoolt ja valige suvand **Kulukeskused osakonniti**.
29. Muutke baasaastaks **2012**, **salvestage** muudatused ja **looge** aruanne. Pärast aruande loomist ja avamist saate aruannet uurida.
30. Aruandlusüksuste kuvamiseks valige rippmenüüst **Aruandluspuu**. Teise võimalusena saate minna aruande reas süvitsi kõikide aruandluspuu üksuste saldode vaatamiseks.
31. Sulgege **Kasumiaruanne – vaikimisi**.
32. Sulgege **aruande kujundaja**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>4. harjutus: konsolideeritud aruande loomine organisatsiooni hierarhia abil
Selle harjutuse puhul muudate olemasolevat vaikearuannet. Lisate organisatsiooni hierarhia aruande definitsiooni konsolideeritud kasumiaruande ja bilansi loomiseks. Kui värskendused on lõpetatud, saate luua konsolideeritud aruande ja uurida aruannet aruandluspuu abil. Alustame loendist Finantsaruanded.

1.  Avage **Finantsaruanded** pearaamatu osas Päringud ja aruanded.
2.  Valige rida aruande puhul, mille nimi on **Kõrvuti bilanss ja kasumiaruanne – vaikimisi**
3.  Valige suvand **Redigeeri**. **Kõrvuti bilanss ja kasumiaruanne – vaikimisi** avaneb aruande kujundajas.
4.  Valige **Fail** &gt; **Salvesta nimega** ning pange aruande nimeks **Kõrvuti konsolideeritud bilanss ja kasumiaruanne**.
5.  Muutke baasaastaks 2012.
6.  Klõpsake puu tüübi rippnoolt ja valige suvand **Organisatsiooni hierarhiad**.
7.  Klõpsake puu tüübi rippnoolt ja valige suvand **Contoso Holdings.**
8.  Salvestage muudatused ja looge aruanne. Viipamisel valige kõik aruandlusüksused. Pärast aruande loomist ja avamist saate aruannet uurida.
9.  Valige suvand **Aruandevalikud**.
10. Valige **Lisa dimensioonifilter** ja valige **Osakond**.
11. Sisestage väljale **022** ja valige **OK**.
12. Sulgege filtritud aruanne.
13. Aruandlusüksuste kuvamiseks valige rippmenüüst **Aruandluspuu**. Teise võimalusena saate minna aruande reas süvitsi kõikide aruandluspuu üksuste saldode vaatamiseks.
14. Sulgege **Kõrvuti konsolideeritud bilanss ja kasumiaruanne**.
15. Sulgege **aruande kujundaja**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>5. harjutus: osakondade kõrvutiaruande loomine
Selles harjutuses loote uue aruande. Aruanne on osakondade kasumi kõrvutiaruanne. Kasutate olemasolevat readefinitsiooni, kuid loote uue aruande definitisiooni ja uue veeru definitsiooni, mis kasutab dimensiooni filtreid. Alustame loendist Finantsaruanded.

1.  Avage **Finantsaruanded** pearaamatu osas Päringud ja aruanded.
2.  Valige **Uus**. Aruande kujundaja avab tühja avatud aruande definitsiooni. Teie esimeseks ülesandeks on luua veeru definitsioon.
3.  Looge uus veeru definitsioon, klõpsates suvandit **Fail**, seejärel suvandit **Uus** ja seejärel suvandit **Veeru definitsioon**.
4.  Valige **veerus A** veeru tüübi puhul suvand **DESC**.
5.  Valige **veerus B** veeru tüübi puhul suvand **FD**.
6.  Topeltklõpsake väljal **Dimensioonifilter**.
7.  Topeltklõpsake aknas **Dimensioon** veergu **Osakond**.
8.  Klõpsake dialoogiboksi üksikus või vahemiku jaotises **kolmikpunkti** välja **Saatja** puhul osakondade loendi kuvamiseks.
9.  Valige osakond **022** **Müük ja turundus** ja seejärel klõpsake nuppu **OK**.
10. Korrake etappe 5 kuni 8 osakondade 23–25 puhul.
11. Sisestage iga FD veeru puhul reale **Päis 2** järgmine osakonna kirjeldus.
    -   Veerg B – Müük ja turundus
    -   Veerg C – Toimingud
    -   Veerg D – Finants
    -   Veerg E – IT

12. Salvestage veeru definitsioon kõrvuti osakondadena. Kuna kasutame olemasolevat readefinitsiooni, saab aruande definitsiooni nüüd muuta vastloodud veeru definitsiooni ja olemasoleva readefinitsiooni kasutamiseks.
13. Valige menüüs **Aken** aruande definitsiooni avamiseks suvand **Uus aruande definitsioon**.
14. Valige readefinitsiooniks **Kasumiaruanne – vaikimisi** ja veeru definitsiooniks **Kõrvuti osakonnad**.
15. Salvestage aruande definitsioon kui **Kõrvuti osakondade kasumiaruanne**.
16. Muutke baasaastaks **2012**.
17. Muutke üksikasjatase valikule **Rahaline, Konto ja Kanne**.
18. **Salvesta** muudatused ja **loo**. Pärast aruande loomist ja avamist saate aruannet uurida.

## <a name="additional-resources"></a>Lisaressursid
[Finantsaruandlus](../../financials/general-ledger/financial-reporting-getting-started.md) 
[Finantsaruannete kuvamine](../../financials/general-ledger/view-financial-reports.md) 
[Dynamicsi finantsaruandluse ajaveeb](http://blogs.msdn.com/b/dynamics_financial_reporting/)




