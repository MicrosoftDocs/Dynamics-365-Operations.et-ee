---
title: Puhkuse ja puudumise plaani loomine
description: Looge rakenduses Dynamics 365 Human Resources erinevat tüüpi puhkuste jaoks puhkuseplaane.
author: andreabichsel
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26d85ce226bd601e3ce0bc789e54a7a1a7ec6812
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057570"
---
# <a name="create-a-leave-and-absence-plan"></a>Puhkuse ja puudumise plaani loomine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Määratlege rakenduses Dynamics 365 Human Resources iga pakutava puhkuse tüübi jaoks puhkuse ja puudumise plaanid. Puhkuse ja puudumise plaanid võivad koonduda erinevatel sagedustel, nt igal aastal, igakuiselt või kaks korda kuus. Saate määratleda plaani kui hüvitise, kus kogu lisandumine omistatakse kindlale kuupäevale. Näiteks võite luua plaani, mis avab igal aastal ujuvad pühad.

Mitmetasemelised puhkuseplaanid võimaldavad töövõtjatel saada soodustusi, võttes aluseks aja, mille nad on organisatsioonis veetnud. Mitmetasemelised plaanid võimaldavad automaatset lisasoodustuse tundide registreerimist.

Saate määrata maksimaalsed ülekandmise summad või minimaalsed saldod, et tagada töötajate ainult koondatud soodustuse tundide kasutamine.

Näiteks mitmetasemelise plaaniga saate anda uutele töötajatele soodustuse 80 tundi tasustatud puhkust (PTO). Seejärel saate anda 120 tundi 60 kuu teenistuse eest.

Saate luua ka ametikohal põhinevaid puhkuse soodustusi, nt ainult juhtivtöötajate soodustuse tunnid.

## <a name="create-a-leave-plan"></a>Puhkuseplaani loomine

1. Lehel **Puhkused ja puudumised** valige suvand **Loo uus plaan**.

2. Jaotises **Üksikasjad** sisestage oma plaani jaoks suvandid **Nimi**, **Alguskuupäev**, **Kirjeldus** ja **Puhkuse tüüp**.

Kui funktsioon **Mitme puhkuse tüübi konfigureerimine ühe puhkuse ja puudumise plaani jaoks** on lubatud, konfigureeritakse puhkuse tüübid jaotises **Lisandumise graafik**, mitte jaotises **Üksikasjad**. Iga lisandumisgraafiku tabeli kirjes saate määratleda puhkuse tüübi. Kui see funktsioon on lubatud, peate kasutama uusi andmeüksusi integreerimiseks või muude stsenaariumide jaoks, mille korral kasutatakse üksuseid. 

Uued üksused on järgmised.

- Puhkuste ja puudumise panga kanne V2
- Puhkuse ja puudumise registreerimine V2
- Puhkuse ja puudumise plaani järk V2
- Puhkuse ja puudumise plaan V2
- Puhkusetaotlus V2

 > [!IMPORTANT]
   > Pärast selle funktsiooni lubamist ei saa seda välja lülitada.

3. Määratlege lisandumised vahekaardil **Lisandumised**. Lisandumised määratlevad, millal ja kui sageli töövõtjale vaba aega antakse. Selles etapis määratlete poliitikad, millal tuleks lisandumisi premeerida, ja puhkuse soodustuste proportsionaalse jaotamise poliitika kohta.

   1. Valige ripploendist väärtus **Lisandumiste sagedus**.

      - Kord päevas
      - Iganädalane
      - Kahenädalane
      - Kaks korda kuus
      - Kord kuus
      - Kord kvartalis
      - Poolaasta kohta
      - Kord aastas
      - Puudub

   2. Lisandumiste perioodide arvutamiseks kasutatava alguskuupäeva määratlemiseks valige ripploendist suvand **Puhkuseperioodi alus**.

      | Puhkuseperioodi alus | Kirjeldus |
      | --- | --- |
      | **Plaanitav alguskuupäev** | Lisandumisperioodi alguskuupäev on kuupäev, mil plaan on saadaval. |
      | **Kindel töövõtja kuupäev** | Lisandumisperioodi alguskuupäev sõltub töövõtja sündmusest.</br><ul><li>Kohandatud (peate määrama iga registreerimise jaoks lisandumiskuupäeva aluse)</li><li>Tähtpäeva kuupäev</li><li>Värbamise algne kuupäev</li><li>Staaž kuupäeval</li><li>Töötaja töösuhte korrigeeritud alguskuupäev</li><li>Töötaja töösuhte alguskuupäev</li></ul> |

   3. Valige ripploendist suvand **Lisandumise andmise kuupäev**.

      - **Lisandumisperioodi lõpukuupäev** – töötajale määratakse vaba aeg omistamisperioodi viimasel päeval. Õige koguse lisandumisel peab viitvõlgade protsess sisaldama kogu perioodi. Näiteks kui lisandumisperiood on 1. jaanuar 2020 kuni 31. jaanuar 2020, peate käivitama lisandumise 1. veebruaril 2020, et kaasata jaanuar.

      - **Lisandumise alguskuupäev** – töötajale määratakse vaba aeg omistamisperioodi esimesel päeval.

   4. Valige ripploendist suvand **Registreerimise lisandumise poliis**. See väärtus määratleb, kuidas arvutada lisandumist, kui töövõtja registreerub lisandumisperioodi keskel.

      - **Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani. Viitvõlgade töötlemisel rakendatakse seda erinevust.

      - **Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel lisandumise töötlemisel.

      - **Arvestus puudub** – lisandumisi ei anta enne järgmist lisandumisperioodi.

   5. Valige ripploendist suvand **Registreerimise tühistamise lisandumise poliis**. See väärtus määratleb, kuidas arvutada lisandumist, kui töövõtja tühistab registreerimise lisandumisperioodi keskel.

      - **Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani. Viitvõlgade töötlemisel rakendatakse seda erinevust.

      - **Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.

      - **Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.

4. Määratlege lisandumise graafik vahekaardil **Lisandumise graafik**. Lisandumise graafik määratleb järgnevat.

   - Kuidas töötaja vaba aega juurde tekitab?
   - Kui palju töövõtja aega tekitab?
   - Millised kogused kanduvad edasi?

   Saate luua tasemeid, et premeerida vaba aega erinevate tasemete põhjal.

   Kui teil on tunnipalgalised töötajad, saate vaba aega anda töötundide, mitte tööstaaži alusel organisatsioonis. Töötundide andmeid talletatakse tavaliselt aja ja kohaloleku süsteemis. Saate importida aja ja kohaloleku süsteemist tavalised töötunnid ja ületunnitöö ning kasutada neid töövõtjale määramise alusena.
   
    1. Valige ripploendist suvand **Lisandumise tüüp**.

      - **Töötatud kuud** – võtke lisandumise graafiku aluseks töötatud kuud.

      - **Töötatud tunnid** – võtke lisandumise graafiku aluseks töötatud tunnid. Lisateavet töötatud tundide lisandumiste kohta vt teemast [Töötatud tundidel põhinev kumulatiivne vaba aja arvestus](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Lisateavet lisandumiste saldode kohta vt teemast [Töötatud tundidel põhinev kumulatiivne vaba aja arvestus](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Sisestage väärtused lisandumise graafiku tabelisse.

      - **Töötatud kuud** – minimaalne kuude arv, kui palju töötaja peab töötama, et tal oleks õigus lisandumistele. Kui te ei nõua miinimumi, seadke väärtuseks 0.

      - **Töötatud tunnid** – minimaalne tundide arv, kui palju töötaja peab puhkuseperioodi kohta töötama, et tal oleks õigus lisandumistele. Kui te ei nõua miinimumi, seadke väärtuseks 0.

      - **Lisandumise kogus** – tundide või päevade arv, mille töövõtjad perioodi eest koguvad. Periood põhineb puhkuse andmise sageduse põhjal.

      - **Minimaalne saldo** – kui töötajad võtavad rohkem puhkust välja, kui neile on ette nähtud, saate anda miinimumsaldole negatiivse väärtuse.

      - **Maksimaalne edasikandmine** – lisandumisprotsess kohandab puhkusesaldod, mis ületavad alguskuupäeva aastapäeva edasikandmise maksimumsaldot.

      - **Hüvitise summa** – tundide või päevade esmane arv, mis töötajale antakse, kui nad esmakordselt registreeruvad puhkuseplaani. See summa ei kogune iga viitvõlaperioodiga.
      
Kui funktsioon **Mitme puhkuse tüübi konfigureerimine ühe puhkuse ja puudumise plaani jaoks** on lubatud, valige suvand jaotisest **Puhkuse tüüp**. 

   > [!IMPORTANT]
   > Pärast selle funktsiooni lubamist ei saa seda välja lülitada.

Kui funktsioon **Täistööaja vaste kasutamine** on lubatud, kasutab rakendus Human Resources töövõtja lisandumise proportsionaalseks jaotamiseks täistööaja vastet. Näiteks kui täistööaja vaste on 0,5 ja lisanduv summa on 10, siis töövõtjale lisandub 5. Seda funktsiooni saate kasutada ainult juhul, kui lubate mitme puhkuse tüübid.  

5. Valige käsk **Salvesta**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Töötatud tundidel põhinev kumulatiivne vaba aja arvestus

Kui teil on tunnipalgalised töötajad, saate vaba aega anda töötundide, mitte tööstaaži alusel organisatsioonis. Töötundide andmete andmed talletatakse tavaliselt aja ja kohaloleku süsteemis. Saate importida oma aja ja kohaloleku süsteemist tavalised töötunnid ja ületunnitöö ning kasutada seda töövõtjale määramise alusena.

Kui valite lisandumise tüübiks töötatud tunnid, saate kasutada lisandumiseks kahte töötuni tüüpi: tavaline ja ületunnitöö. Töötunniplaanide arvestuse töötlus kasutab arvestatavate tundide määramiseks arvestussagedust koos arvestusperioodi alusega.

### <a name="annual-accrual-frequency"></a>Iga-aastane arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018–12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018–12/31/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Igakuine arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018–8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018–8/31/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Poolekuine arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8/16/2018–8/31/2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8/16/2018–8/31/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Iganädalane arvestussagedus

| Arvestuse preemiakuupäev    | Töötundide kiht    | Juurdekasvu summa        | Töötundide kuupäevad   | Tegelik töötundide arv| Preemia               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018–8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018–8/31/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Töövõtjale määratud puhkuseplaanid

Töövõtja määratud puhkuseplaanides kuvatakse töötundide plaanide jaoks taseme alus ja tundide tüüp. Aktiivsete plaanide puhul kuvatakse ka tegelik töötundide arv lisandumisperioodiks tänase kuupäeva seisuga.

### <a name="loading-data"></a>Andmete laadimine

Saate importida tegelikud tunnid, kasutades andmehalduses üksust **Töötunnid puhkuste ja puudumiste eest**. Tööajakalendrite kasutamisel kontrollib import, ega tavalised töötunnid ei ületa kalendris määratletud päevale planeeritud tunde. Import kontrollib ka, ega antud päeval töötatud tundide arv ei ületa 24 tunni. 

Puhkusea lisandumisprotsessis kasutatavate tegelike tundide importimiseks vajate järgmist teavet.

- Personalinumber 
- Töötamise kuupäev
- Tüüp
- Tunnid

Ühe kuupäevaga saab olla seostatud ainult üks tüüp.

| Personalinumber       | Töötamise kuupäev           | Tüüp                  | Tunnid                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Tavaline               | 8                    |       
| 000337                | 8/7/2018             | Tavaline               | 8                    |
| 000337                | 8/7/2018             | Ületunnitöö              | 3                    |
| 000337                | 8/8/2018             | Tavaline               | 8                    |
| 000337                | 8/7/2018             | Tavaline               | 8                    |
| 000337                | 8/9/2018             | Tavaline               | 8                    |

## <a name="enrollments-and-balances"></a>Registreerimised ja saldod

### <a name="enrollment-date"></a>Registreerimise kuupäev

Registreerimise kuupäev määratleb, millal töötaja saaks alustada vaba aja kogumist. Näiteks kui töötaja on liitunud 15. juunil 2018 puhkusekavasse, ei saa tal vaba aega koguneda enne 15. juunit 2018.

### <a name="current-balance"></a>Praegune saldo

Praegune saldo on puhkuse aja taotluste jaoks saadaolev summa. See summa sisaldab viitvõlgu, kinnitatud taotlusi ja korrigeerimisi kuni praeguse kuupäevani.

### <a name="current-balance-examples"></a>Praeguse saldo näited

#### <a name="annual-plan"></a>Aastaplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Aastane            | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Lisandumised töödeldakse 1. jaanuaril 2019 (01/01/2019), et kaasata kogu periood.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Taotletud summa | Praegune saldo (01. jaanuari 2019 seisuga) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Praegune saldo (160) = viitvõla summa (200) – taotluse summa (40)

#### <a name="semimonthly-plan"></a>Poole kuu plaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Lisandumised töödeldakse 1. mail 2018 (01/05/2018), et kaasata kogu periood.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Taotletud summa | Praegune saldo (01. jaanuari 2019 seisuga) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Praegune saldo (22) = viitvõla summa (5 × 6) – taotluse summa (8)

#### <a name="monthly-plan"></a>Kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Lisandumised töödeldakse 1. mail 2018 (01/05/2018), et kaasata kogu periood.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Taotletud summa | Praegune saldo (01. jaanuari 2019 seisuga) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Praegune saldo (7) = viitvõla summa (5 × 3) – taotluse summa (8)

### <a name="forecasted-balance"></a>Prognoositav saldo

See *eelarvesaldo* on tulevasel kuupäeval saadaolev puhkuse kogus. Viitvõlgade ja ülekandmise korrigeerimised on prognoositud selleks kuupäevaks.

Rakendus Human Resources kasutab järgmist valemit:

Esmaspäeva prognoositud saldo = praegune saldo – taotlused + viitvõlad – ülekandmise korrigeerimine

### <a name="forecasted-balance-examples"></a>Prognoositud saldo näited

#### <a name="annual-plan"></a>Aastaplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Aastane            | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Lisandumised töödeldakse 15. veebruaril 2019 (15/02/2019), et kaasata kogu periood.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Praegune saldo | Prognoositud saldo (15. veebruari 2019 seisuga) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Prognoositud saldo (40) = juurdekasvu summa (20) – praegune saldo (40) – ülekandmise korrigeerimine (20)

#### <a name="semimonthly-plan"></a>Poole kuu plaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Lisandumised töödeldakse 15. veebruaril 2019 (15/02/2019), et kaasata kogu periood.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Praegune saldo | Prognoositud saldo (15. veebruari 2019 seisuga) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Prognoositud saldo (35) = juurdekasvu summa (5 × 3) + praegune saldo (40) – ülekandmise korrigeerimine (20)

#### <a name="monthly-plan"></a>Kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Lisandumised töödeldakse 15. veebruaril 2019 (15/02/2019), et kaasata kogu periood.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Praegune saldo | Prognoositud saldo (15. veebruari 2019 seisuga) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Prognoositud saldo (30) = juurdekasvu summa (10 × 1) – praegune saldo (40) – ülekandmise korrigeerimine (20)

### <a name="proration-balance-examples"></a>Proportsionaalse arvestuse saldo näited

#### <a name="prorated-monthly-plan"></a>Proportsionaalse arvestuse kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kord kuus           | Plaanitav alguskuupäev      |

**Tulemused**

| Töötaja            | Töötatud kuud | Registreerimise kuupäev | Alguskuupäev | Juurdekasvu summa | Viitvõlgade protsess | Saldo |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Täieliku arvestuse kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kord kuus           | Plaanitav alguskuupäev      |

**Tulemused**

| Töötaja            | Töötatud kuud | Registreerimise kuupäev | Alguskuupäev | Juurdekasvu summa | Viitvõlgade protsess | Saldo |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Arvestuse puudumise kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kord kuus           | Plaanitav alguskuupäev      |

**Tulemused**

| Töötaja            | Töötatud kuud | Registreerimise kuupäev | Alguskuupäev | Juurdekasvu summa | Viitvõlgade protsess | Saldo |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkuste ja puudumiste tüüpide konfigureerimine](hr-leave-and-absence-types.md)
- [Puhkuse ja puudumise plaanide koondamine](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]