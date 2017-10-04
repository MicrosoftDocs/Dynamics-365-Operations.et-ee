---
title: Palga algsaldode sisestamine
description: "Selles teemas kirjeldatakse tulukoodide, mahaarvamiste, soodustuste ja maksude algsaldode sisestamist. See teave on partneritele väärtuslik andmete migreerimiseks või üleviimiseks uue palgajuurutuse korral teisest süsteemist."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: d9e3018eb7b6c20cfd5e23a10d15e230009196de
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="enter-payroll-beginning-balances"></a>Palga algsaldode sisestamine

[!include[banner](../../includes/banner.md)]

Selles teemas kirjeldatakse tulukoodide, mahaarvamiste, soodustuste ja maksude algsaldode sisestamist. See teave väärtuslik partneritele, kes viivad uue palgajuurutuse jaoks teisest süsteemist andmeid üle. Palgasaldode sisestamiseks valmistumisel kontrollime järgmisi andmeid.

> * Töötajakirjed on sisestatud ja süsteemis saadaval
> * Järgmised andmed on seadistatud ja töötajatele määratud.

> > * Palgatsüklid ja makseperioodid
> > * Tulukoodid
> > * Maksud
> > * Soodustused ja mahaarvamised

> * Ettevõte oleks pidanud valima kuupäeva, millele saab määrata palga algsaldosid.

> * Andmeid koguti kõigi tulude, soodustuste/mahaarvamiste, soodustuse panuste, töötaja maksude ja tööandja maksude ning nende summad pärandsüsteemist jooksva aasta kohta.

Kui plaanite algsaldode sisestamist, siis mõelge, kui üksikasjalikud andmed olema peavad. Enamik ettevõtteid sisestab jooksva aasta kohta ühe konsolideeritud summa. Kuid kui on vaja täpsemaid andmeid, saab saldod sisestada kvartalivahemikena. Vajaliku üksikasjataseme põhjal määratakse, mitu käsitsi palgaväljavõtet tuleb igale töötajale luua. Ühe jooksva aasta summa puhul on iga töötaja jaoks vaja ainult ühte käsitsi väljavõtet. Selleks kasutage jooksva aasta summasid eelmise süsteemi lõplikust palgaväljavõttest uude palgasüsteemi sisestatava summana.

Järgmises näites näidatakse, kuidas sisestada töötaja palga algsaldosid, sh tulukoode, soodustusi/mahaarvamisi ja makse. Tõsielulise näite puhul oleks teil iga tulukoodi jaoks reaüksus, soodustuse mahaarvamine, soodustuse panus, töötaja maks ja tööandja maks ja sisestatav summa oleks jooksva aasta summa. Kasutades seda koodide ja summade loendit, järgige juhiseid käsitsi tulu- ja palgaväljavõtte loomiseks, nii et arvestus oleks keelatud, et tuua algsaldod palga jaoks üle.  Arvestus tuleb keelata, kuna seda algsaldo palgaväljavõtet ei ole vaja pearaamatusse sisestada. See tehti pärandsüsteemis ja see tuleb uude süsteemi üle, kui määrate pearaamatus algsaldod.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Palga algsaldodes kasutatavate tulukoodide seadistamine
Palga algsaldode sisestamisel veenduge, et kasutatavad tulukoodide konfigureerimisel oleks valik Luba tuluväljavõtte määrade muutmine lubatud. See võimaldab summat pärandsüsteemist käsitsi sisestada. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Töötajale tuluväljavõtte koostamine algsaldo jaoks
See etapp loob käsitsi tuluväljavõtte iga töötaja jaoks pärandsüsteemi viimase palgaperioodi kohta, mis loob tuluväljavõtte read uues palgasüsteemis. Sisestage üks rida tulukoodi kohta ning jooksva aasta summa ja tunnid. Näidisetapid on järgmised.

1. Avage leht **Kõik tuluväljavõtted** ja klõpsake nuppu **Uus**.  

Sisestage järgnev. 

| Väli      | Väärtus                 |
|------------|-----------------------|
| Töötaja     | Michael Redmond       |
| Palgatsükkel  | sm                    |
| Makseperiood | 6/16/2017 - 6/30/2017 |

2. Sisestage vahekaardile **Tuluväljavõtte rida** järgmised andmed.

Rida 1: vahekaart **Tuluväljavõtte rida**

| Väli            | Väärtus       |
|------------------|-------------|
| Tulukood    | Regulaarne palk |
| Kogus         | 1,00        |
| Rage             | 30 000      |
| Rea üksikasjade vahekaart |             |
| Käsitsi           | (märgitud)    |

Rida 2: vahekaart **Tuluväljavõtte rida**

| Väli            | Väärtus    |
|------------------|----------|
| Tulukood    | Preemia    |
| Kogus         | 1.0000   |
| Kurss             | 4250.00  |
| Rea üksikasjade vahekaart |          |
| Käsitsi           | (märgitud) |

Rida 3: vahekaart **Tuluväljavõtte rida**

| Väli           | Väärtus      |
|-----------------|------------|
| Tulukood   | Komisjonitasu |
| Kogus        | 1.0000     |
| Kurss            | !,299.00   |
| Kurss            | 1,299.00   |
| Rea üksikasjade vahekaart |            |
| Käsitsi          | (märgitud)   |

> [!NOTE]
> Iga tuluväljavõtte rea puhul vahekaardil **Rea üksikasjad** liuguri **Käsitsi** lükkamine valikule **Jah** on iga töötaja puhul palga algsaldode sisestamiseks oluline.

3. Klõpsake paanil **Tegevus** valikut **Tuluväljavõtte väljastamine** USA-FED-ER-FICA.

4. Klõpsake paanil **Tegevus** valikut **Palgaväljavõte** lehe **Palgaväljavõtete loomine** avamiseks ja seadistage järgmised valikud.

| Väli              | Väärtus     |
|--------------------|-----------|
| Maksekuupäev       | 6/30/2017 |
| Maksetsükli tüüp   | Käsitsi    |
| Keela raamatupidamine |   Jah     |

> [!NOTE] 
> See on saadaval ainult siis, kui makse käitamise tüüp on käsitsi ja kui kasutaja soovib maksetsükli arvestuse keelata.

Klõpsake nuppu **OK** ja sulgege **teabelogi**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Miks peab liugur Keela arvestus olema makseväljavõtete loomisel seatud valikule Jah?
Liuguri seadmine valikule **Jah** takistab makseväljavõtte levitamist ja sisestamist pearaamatusse. Pearaamatu summasid värskendati varem, kui sisestati kontosaldod pärandsüsteemist. Palgaarvestuse algsaldode sisestamine võimaldab luua aruanded, mis sisaldavad teavet varasematest aastatest, samuti tuvastada soodustuste piirangud ja maksuotstarbed.   

### <a name="c-create-pay-statements-for-employees"></a>C. Töötajatele palgaväljavõtete koostamine
Pärast algsaldodega palgaväljavõtete koostamist tuleb kontrollida, et palgaväljavõtted kajastaksid täpselt palgaandmeid. Soodustuste ja maksude teave tuleb samuti käsitsi uuendada, et see vastaks eelmises palgasüsteemis olevatele väärtustele. Pärast kontrollimist, et eelmise palgasüsteemi summad vastavad praeguste palgaväljavõtete summadele, tuleb palgaväljavõtted lõpetada.

1. Avage leht **Kõik palgaväljavõtted**.

2. Tõstke esile viimati Michael Redmondile koostatud palgaväljavõte

3. Klõpsake nuppu **Redigeeri** lehe **Palgaväljavõte** avamiseks.

4. Avage vahekaart **Soodustuse mahaarvamised** ja sisestage järgmine.

| Väli                           | Väärtus            |
|---------------------------------|------------------|
| Soodustus                         | Mahaarvatav summa |
| 401K | Osalus              | 3000.00          |
| Hambaravikindlustus | SubSp                  | 495.00           |
| Osak. kulutused ravikindlustusele | Osalus | 2500.00          |
| Visioon | SupSp                  | 500,00           |

5. Sisestage vahekaardile **Soodustuse panused** järgmine.

| Väli              | Väärtus               |
|--------------------|---------------------|
| Soodustus            | Panuse summa |
| 401K | Osalus | 3000,00             |
| Hambaravikindlustus | SubSp     | 495.00              |
| Visioon | SubSp     | 500,00              |

6. Sisestage vahekaardile **Maksude mahaarvamised** järgmine.

| Väli           | Väärtus            |
|-----------------|------------------|
| Maksukood        | Mahaarvatav summa |
| USA-FED-ER-FICA | 1600.00          |
| USA-FED-ER-MEDI | 825.75           |

7. Sisestage vahekaardile **Maksude panused** järgmine.

8. Klõpsake valikut **Arvuta**.
> [!IMPORTANT] 
> Kontrollige töötaja makseväljavõtete kogusummade vastavust pärandsüsteemi jooksva aasta summadele. Järgmises etapis võib olla vaja lõpetamisega oodata, et oleks võimalik kõiki palgaväljavõtteid üldiselt kontrollida. Kui palgaväljavõtted on kontrollitud, vaadake need läbi ja lõpetage need.

Sama protsessi saab teha vajaduse korral kvartalite kaupa iga aasta kõigi eelmiste kvartalite kohta. See on vajalik ainult juhul, kui kliendil on vaja andmeid kvartalite kaupa näha, pärandsüsteemi naasmata.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Kui teete töötaja algsaldode sisestamisel vea,
on võimalik kandeid tühistada ja uuesti sisestada. Kande tühistamiseks peate tegema lehel **Kõik palgaväljavõtted** järgmised toimingud.

1. Klõpsake valikut **Tühista**.

2. Klõpsake **Jah**, kui kuvatakse teade „Selle palgaväljavõtte tühistamisel luuakse tühistav palgaväljavõte selle palgaväljavõtte tasakaalustamiseks. Kumbagi palgaväljavõtet ei saa muuta. Kas soovite selle palgaväljavõtte tühistada?” . 

Kui olete palgaväljavõtte tühistanud, saate luua uue palgaväljavõtte töötaja jaoks varem loodud tuluväljavõtte põhjal. Korrigeerige kindlasti kõik tuluväljavõtte valed read, enne kui loote uue palgaväljavõtte, ja seejärel looge uued palgaväljavõtted õigete summadega. 
