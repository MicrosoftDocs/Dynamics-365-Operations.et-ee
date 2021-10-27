---
title: Elektroonilise aruandluse (ER) laiendatud vormingu otsing
description: See teema kirjeldab, kuidas ER-vormingus viidet saab seadistada ER vormingu otsingus, kui nõutud vorming on talletatud globaalses hoidlas.
author: NickSelin
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 395282eb267e7e356fca6087f99c6f193741ac9d
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605153"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Luba kasutajatel häälestada ER-vormingu viidet vormingu päringule globaalsest hoidlast

[!include [banner](../includes/banner.md)]

Saate kasutada [elektroonilise aruandluse](general-electronic-reporting.md) (ER) raamistikku, et konfigureerida [vorminguid](general-electronic-reporting.md#FormatComponentOutbound) väljaminevatele dokumentidele vastavalt erinevate riikide/piirkondade juriidilistele nõudmistele. Saate kasutada ka ER raamistikku, et konfigureerida [vorminguid](general-electronic-reporting.md#FormatComponentInbound) sissetulevate dokumentide sõelumiseks ja kasutada nende dokumentide teavet, et lisada või värskendada rakenduse andmeid. Kõiki neid vorminguid saab kasutada teie rakenduse Dynamics 365 Finance eksemplaris sissetuleva või väljamineva äridokumendi käsitlemiseks teatud äriprotsessi osana.

Tavaliselt peate määrama, millist ER-vormingut peab teatud äriprotsessis kasutama. Selleks valige üks ER vorming otsinguväljal, mis on konfigureeritud äriprotsessi kohaste parameetrite osana. Neid otsingu välju rakendatakse tavaliselt, kasutades ER raamistiku vastavat API-d. Lisateavet vt teemast [ER raamistiku API-kood, et kuvada vormingu vastendamise otsing](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Näiteks, kui konfigureerite [väliskaubanduse parameetreid](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters), peate seadistama viited konkreetsetele ER vormingutele, mida kasutatakse Intrastat-deklaratsiooni ja Intrastat-deklaratsiooni kontrolliaruande loomiseks. Järgmised pildid näitavad, kuidas ER vormingu otsinguväli välja näeb **Väliskaubanduse parameetrite** lehel.

Kui praegune Finance’i eksemplar ei sisalda Intrastati äriprotsessiga seotud ER-i vorminguid, on see otsinguväli tühi.

[![Väliskaubanduse parameetrite leht, tühi aruandevormingu vastendamise väli.](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Kui praegune Finance eksemplar sisaldab Intrastati äriprotsessiga seotud ER vorminguid, pakub otsinguväli ER vorminguid.

[![Väliskaubanduse parameetrite leht, valikutega aruandevormingu vastendamise väli.](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

See otsing pakub ainult praegusesse Finance eksemplari juba imporditud ER vorminguid. Et [importida](./tasks/er-import-configuration-lifecycle-services.md) ER lahendusi praegusesse Finance eksemplari, teil on vaja luba käivitada vastav ER raamistiku funktsioon, mis toetab ER vorminguid sisaldavate ER lahenduste [elutsüklit](general-electronic-reporting-manage-configuration-lifecycle.md).

Alates Finance versioonist 10.0.9 (aprill 2020 väljalase), ER vormingu otsing, mida rakendatakse ER raamistiku API abil, on laiendatud. Saate siiski valida olemasolevad ER vormingud, mis on kiirkaardil **Vormingu konfiguratsiooni valimine**. Lisaks pakub laiendatud otsing uut võimalust otsida globaalset hoidlat (GR), et leida kindlaid ER-i vorminguid. Kõiki GR ER formaate pakutakse kiirkaardil **Globaalsest hoidlast importimine**.

[![Väliskaubanduse parameetrite leht, importimine globaalsest hoidla kiirkaardist.](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Sarnaselt kiirkaardile **Vormingu konfiguratsiooni valimine**, näitab kiirkaart **Globaalsest hoidlast importimine** ainult ER vorminguid, mis on kohaldatavad äriprotsessile, mille puhul on sellel otsinguväljal valitud ER vorming. Selles näites Intrastati deklaratsiooni loomine. ER vorming on kohaldatav ettevõttele, kuhu kasutaja on praegu sisse logitud, sõltuvalt ettevõtte riigi kontekstist.

ER-vormingu valimisel kiirkaardil **Globaalsest hoidlast importimine** imporditakse valitud ER-vormingu [konfiguratsioon](general-electronic-reporting.md#Configuration) GR-lt praegusesse Finance eksemplari.

[![Väliskaubanduse parameetrite leht, töötlemise toimingu märkus.](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Kui import on edukalt lõpule viidud, talletatakse sellel otsinguväljal viide imporditud ER vormingule. Kui avate esmakordselt GR-i, tuleb teil järgida antud linki, et registreeruda [regulatiivsete konfiguratsiooniteenuse](https://aka.ms/rcs) (RCS) jaoks, mida kasutatakse juurdepääsu haldamiseks GR-i salvestusruumi.

[![Väliskaubanduse parameetrite leht, link RCS-ile registreerumiseks.](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Vaikimisi esindab kiirkaart **Globaalsest hoidlast importimine** ajutise salvestusruumi ER vormingute loendit, mis luuakse automaatselt jõudluse täiustuste GR sisu alusel. See juhtub siis, kui kiirkaart **Globaalsest hoidlast importimine** avatakse esimest korda, mis võib kesta mitu sekundit.

Kui te ei näe nõutud ER vormingut kiirkaardil **Globaalsest hoidlast importimine**, kuid olete kindel, et see ER vorming on salvestatud GR-is, valige suvand **Sünkroonimine**. See suvand värskendab ajutise salvestusruumi ja sünkroonib selle GR-i praeguse sisuga.

## <a name="feature-activation"></a>Funktsiooni aktiveerimine

Selle funktsiooni saadavust kontrollib **ER vormingu konfiguratsioonide laiendatud otsing, mis võimaldab pärida globaalsest hoidlast** **Funktsioonide halduses**. Funktsioon on vaikimisi lubatud.

[![Funktsioonihalduse leht.](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Turbemeetmed

**Konfiguratsioonihoidlate haldamise** (**ERMaintainSolutionRepositories**) privileeg kontrollib kasutaja juurdepääsu GR-ile, kes avab ER vormingu otsingu lubatud kiirkaardiga **Globaalsest hoidlast importimine**. Et lubada kasutajatel juurde pääseda GR sisule ER vormingu otsingust, peate muutma turvasätteid, andes **ERMaintainSolutionRepositories** kasutajatele privileegi kas otse või kasutades juba määratud rolle ja kohustusi.

Järgmine pilt näitab, kuidas saab seda privileegi anda kasutajatele, kellele on määratud **Raamatupidaja** roll. See roll võimaldab kasutajatel konfigureerida väliskaubanduse parameetreid ja seadistada viiteid ER-i vormingutele väljadel **Failivormingu vastendamine** ja **Aruande vormingu vastendamine** lehel **Väliskaubanduse parameetrid**.

[![Turvakonfiguratsiooni leht.](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Kitsendused

Juurdepääs GR-ile ER vormingu otsingus on praegu toetatud ainult väljaminevate dokumentide loomiseks kasutatavate ER-vormingute valimiseks.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Miks ma ei pääse juurde globaalsele hoidlale ER-vormingu otsingust?

Kui teil on lubatud funktsioon **ER vormingu konfiguratsioonide laiendatud otsing, mis võimaldavad teha päringuid globaalsest hoidlast** **Funktsioonide halduse** lehel, kuid kasutajad ei näe ER vorminguid kiirkaardil **Globaalsest hoidlast importimine** ja **Sünkroonimise** suvand on nähtav, kuid keelatud, veenduge, et **Konfiguratsiooni hoidlate haldamise** (**ERMaintainSolutionRepositories**) privileeg on kasutajale antud. Selle privileegi saamiseks võtke ühendust oma süsteemiadministraatoriga.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) raamistiku API](er-apis-app73.md)
- [Elektroonilise aruandluse (ER) konfiguratsioonide elutsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
