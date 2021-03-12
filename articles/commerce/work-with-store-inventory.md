---
title: Kaupluse varude haldamine
description: Selles teemas kirjeldatakse dokumenditüüpe, mida saate kasutada varude haldamiseks.
author: rubencdelgado
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 616fb8975543344657c00c419ce7279658694675
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989472"
---
# <a name="commerce-inventory-management"></a>Kaubanduse varude haldamine

[!include [banner](includes/banner.md)]

Kui töötate varudega rakenduses Microsoft Dynamics 365 Commerce ja kasutate mis tahes Commerce'i rakendusi, mis on ühendatud Commerce Scale Unit'iga (CSU), on oluline teada, et CSU tellimuse töötlemise loogika pakub piiratud tuge teatud varude dimensioonidele ja teatud varude üksuse tüüpidele. Commerce'i rakendused ei toeta täielikke kauba konfigureerimise võimalusi, mis on saadaval Dynamics 365 Supply Chain Managementi kauba konfigureerimise suvandite kaudu.

CSU-l töötavad Commerce'i rakendused ei toeta praegu järgmisi tootedimensioone ja kauba konfiguratsioone.

- Konfiguratsiooni tootedimensioon ja koosluse (BOM) kaubad (välja arvatud jaemüügi tootekogumid, mis kasutavad osasid BOM-raamistiku komponente)
- Tegeliku kaaluga kaubad
- Versiooni tootedimensiooni juhitud kaubad

CSU-l töötavad Commerce'i rakendused ei toeta praegu järgmisi jälgimisdimensioone.
- Omanikudimensioon

- Kassarakendus võib järgmiste dimensioonide puhul pakkuda piiratud tuge. Kassa võib lao või kaupluse seadistuse konfiguratsiooni põhjal mõne neist dimensioonidest varude kannetesse automaatselt vaikimisi lisada. Kassa ei toeta siiski dimensioone täielikult samal viisil, nagu neid toetatakse müügikande käsitsi sisestamisel Commerce'i peakontorisse. 

- **Lao asukoht** – uute kassatoimingute [Sissetuleku toiming](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ja [Väljamineku toiming](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) kasutamisel saavad kasutajad valida lao varude asukoha kaupade vastuvõtmiseks või väljaminevate üleviimistellimuse kaupade lähetamiseks. Aegunud toimingu **Komplekteerimine ja vastuvõtmine** kasutamisel, on saadaval piiratud asukohahalduse tugi väljaminevate ükannete vastuvõtmiseks ja saatmiseks. See tugi on saadaval ainult juhul, kui kauba ja kaupluse lao puhul on sisse lülitatud suvand **Kasuta laohaldusprotsessi**. Varude asukohta ei saa praegu kasutada toiminguga **Laoinventuur** või **Otsing varudest**.

- **Litsentsiplaat** – litsentsiplaadid kohalduvad ainult siis, kui kauba ja kaupluse lao puhul on sisse lülitatud suvand **Kasuta laohaldusprotsessi**. Kui kassas võetakse varud kaupluse lattu vastu toimingu **Sissetuleku toiming** või **Komplekteerimine ja vastuvõtmine** abil, kus laohaldusprotsess on sisse lülitatud, ja kui kauba vastuvõtmiseks valitud asukoht on lingitud asukohaprofiiliga, mis nõuab litsentsiplaadi juhtelementi, rakendab kassarakendus vastuvõtvale reale süstemaatiliselt litsentsi. Kassa kasutajad ei saa litsentsiplaadi andmeid muuta ega hallata. Kui on nõutav litsentsiplaadi täielik haldamine, soovitame kauplusel kasutada [laorakendust](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) või kontoriklienti nende kaupade vastuvõtmise haldamiseks.

- **Seerianumber** – rakendus Kassa pakub piiratud tuge ühe seerianumbri registreerimise jaoks, mis registreeritakse kande müügireal kassas loodud tellimuste alusel ja sisaldavad järjestatud kaupu. Seda seerianumbrit ei kinnitata juba laos registreeritud seerianumbrite suhtes. Kui müügitellimus on loodud kõnekeskuse kanalis või on täidetud ettevõtte ressursiplaneerimise (ERP) kaudu ja mitu seerianumbrit on registreeritud ühel müügireal ERP-s täitmise protsessi käigus, siis neid seerianumbreid ei saa rakendada ega kinnitata, kui nende tellimuste puhul teostatakse kassas tagastust. Kui varud võetakse vastu toimingu **Sissetuleku toiming** abil, saavad kasutajad [vastuvõetud seerianumbrid registreerida või kinnitada](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).

- **Partii ID** - kassarakendus pakub väljavõtte sisestamisel piiratud tuge, kui müüakse partii kaudu juhitud kaupa, kuid kassa kasutajad ei saa määratleda partii ID-d, mis müüdi või komplekteeriti kassa rakendust kasutades.

- **Lao olek** – kaupade puhul, mis kasutavad laohalduse protsessi ja nõuavad lao olekut, ei saa oleku välja määrata ega muuta rakenduse Kassa kaudu. Kaupluse lao konfiguratsioonis määratletud lao vaikimisi olekut kasutatakse kaupade lattu vastuvõtmisel.

> [!NOTE]
> Kõik organisatsioonid peavad kaubakonfiguratsioone Commerce'i rakenduste kaudu arendus- või katsekeskkonnas katsetama, enne kui need tootmiskeskkondadesse juurutatakse. Testige kaupu, kasutades neid kassas regulaarsete sularaha- ja müügikannete tegemiseks ning looge klienditellimused (kui on kohaldatav) läbi kassa, kõnekeskuse või e-kaubanduse, et kontrollida, kas need on täielikult toetatud. Peaksite katsetama ka kassa täitmise ja varude protsesse (nt varude vastuvõtmise ja tellimuse täitmise toimingud) enne uute kaubakonfiguratsioonide juurutamist, veendumaks, et kassarakendus saab neid toetada. Katsetamine peab hõlmama täieliku väljavõtte/tellimuse sisestamise protsessi käitamist teie katsekeskkonnas ja kontrollimist, et nende kaupade loomisel ja sisestamisel Commerce'i peakontoris ei ilmneks ühtegi sisestamisprobleemi.
>
> Kui kaubad konfigureeritakse viisil, mida Commerce'i rakendused ei toeta ja sobivat testimist ei toimu, võivad ilmneda andmete tõrked, mida ei ole lihtne parandada või mida ei pruugi üldse olla võimalik parandada.

## <a name="purchase-orders"></a>Ostutellimused

Ostutellimused luuakse Commerce'i peakontoris. Kui ostutellimuse päisesse või ostutellimuse ridadele on kaasatud kaupluse ladu, saab tellimust vastu võtta kaupluses kassa toimigu [Sissetuleku toiming](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) abil. 

## <a name="transfer-orders"></a>Üleviimistellimused

Üleviimistellimusi saab luua Commerce'i peakontori kaudu või kassa toimingu [Sissetuleku toiming](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) või [Väljamineku toiming](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) abil. Saate kasutada kassa toimingut **Sissetuleku toiming** üleviimistellimuse taotluse loomiseks, et saata kaupa kauplusesse mõnest muust laost või kaupluse asukohast. Saate kasutada kassa toimingut **Väljamineku toiming** üleviimistellimuse taotluse loomiseks, et lähetada kaupa kauplusest mõnda muusse lattu või kaupluse asukohta. Pärast kaupluse üleviimistellimuse loomist saab see kauplus hallata üleviimistellimuse varude sissetulekut kassa toimingu **Sissetuleku toiming** abil. Kui kauplus lähetab varusid teise asukohta, kasutatakse selle kaupluse väljaminevate saadetiste protsessi haldamiseks kassa toimingut **Väljamineku toiming**.

## <a name="stock-counts"></a>Laoinventuurid

Laoinventuurid võivad olla plaanipärased või plaanivälised. Plaanitud laoinventuurid luuakse Commerce'i peakontori kaudu, luues dokumendi Inventuuritööleht, mis lingitakse kaupluse laoga. See tööleht määrab kaubad, mida tuleb loendada. Kauplus saab seejärel juurdepääsu eelmääratletud inventuuri töölehtedele ja toimib nende alusel, kasutades kassa toimingut **Laoinventuur**. Kaupluse kasutajad käivitavad planeerimata laoinventuuri, kuna see on vajalik kassa toimingu **Laoinventuur** kasutamisel. Erinevalt ajastatud laoinventuuridest puudub plaanimata laovarudel eelmääratletud kaupade loend. Mõlemat tüüpi laoinventuuri lõpetamisel kassas, kooskõlastatakse ja saadetakse see peakontorisse. Peakontoris tuleb seejärel kinnitada inventuur ja sisestada Commerce'i peakontorisse eraldi etapina.

## <a name="inventory-lookup"></a>Otsing varudest

Hetkel vaba olevat tootekogust mitme kaupluse ja lao kohta saab vaadata lehelt **Otsing varudest**. Lisaks jooksvale vabale kaubavarule saab tulevasi lubamiseks saadaval (ATP) koguseid vaadata iga kaupluse kohta. Valige kauplus, mille ATP koguseid soovite vaadata, ja seejärel valige **Kaupluse saadavuse kuvamine**. Lisateavet saadaolevate konfigureerimissuvandite kohta leiate teemast [Varude saadavuse arvutamine jaemüügikanalite jaoks](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).
