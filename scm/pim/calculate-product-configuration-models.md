---
title: Toote konfiguratsioonimudelite arvutuste KKK
description: Selles artiklis kirjeldatakse tootekonfiguratsiooni mudelite arvutusi ja selgitatakse arvutuste kasutamist koos piirangutega.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f13d03e5d1a26a5c87d71732b692537be94bdfb8
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Toote konfiguratsioonimudelite arvutuste KKK

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse tootekonfiguratsiooni mudelite arvutusi ja selgitatakse arvutuste kasutamist koos piirangutega.

Arvutusi saab kasutada aritmeetiliste või loogiliste operatsioonide puhul. Need täiendavad avaldise piiranguid toote konfiguratsioonimudelites. Saate määratleda arvutused lehel **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** ja luua seejärel arvutuste jaoks avaldisi avaldiseredaktoris. Lisateabe saamiseks vt jaotist Arvutuste loomine.

## <a name="what-is-a-calculation"></a>Mis on arvutus?
Arvutus on toote konfiguratsioonimudelis kasutatav element. Arvutused täiendavad piiranguid, võimaldades teil kasutada kümnendarve väärtuste arvutamiseks toote konfigureerimisel. Lisaks on arvutuste puhul võimalik kasutada suuremat arvu tehtemärke kui piirangute puhul.  

Sarnaselt piirangule on arvutus seotud kindla komponendiga toote konfiguratsioonimudelis ja seda ei saa uuesti kasutada või teise komponendiga jagada. Üks oluline erinevus arvutuste ja piirangute vahel on see, et arvutused on imperatiivsed (ühesuunalised) ja piirangud on deklaratiivsed (kahesuunalised). Lisateavet piirangute kohta saate jaotisest [Avaldise piirangud ja tabeli piirangud](expression-constraints-table-constraints-product-configuration-models.md).  

Arvutus koosneb on sihtatribuudist ja arvutusavaldisest.

## <a name="what-is-a-target-attribute"></a>Mis on sihtatribuut?
Sihtatribuut on atribuut, mis võtab avaldises vastu arvutuse tulemuse.  

Järgmises valemis on sihtatribuut laudlina mõõt.  

**Avaldis:** If\[decimalAttribute1 &lt;= decimalAttribute2, tõene, väär\]  

**DecimalAttribute1** on tabeli pikkus ja **decimalAttribute2** on laudlina pikkus. Avaldis tagastab väärtuse **Tõene** sihtatribuudile, kui **decimalAttribute2** on suurem kui **decimalAttribute1** või sellega võrdne. Muidu tagastab avaldis väärtuse **Väär**. Seega on laudlina mõõt aktsepteeritav, kui laudlina pikkus on laua pikkusega sama või ületab laua pikkuse.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Milliseid atribuudi tüüpe saab sihtatribuutideks määrata?
Kõiki toote konfiguraatori puhul toetatud atribuuditüüpe saab määrata sihtatribuutideks, välja arvatud ilma fikseeritud loendita tekst.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Kas sihtatribuudi väärtus saab arvutuses sisendatribuutide väärtusi piirata?
Ei, sihtatribuudi väärtus ei saa sisendatribuutide väärtusi piirata, sest arvutused on ühesuunalised. Seetõttu määratakse sihtatribuudi väärtus sisendatribuudi väärtuse muudatuste alusel, kuid muudatus sihtatribuudi väärtuses ei mõjuta sisendatribuutide väärtust. See käitumine erineb piirangute käitumisest. Piirangud ilmnevad mõlemasuunaliselt.

### <a name="example"></a>Näide

Järgmises avaldises on arvutuse sihtväärtus toitejuhtme pikkus ja sisendväärtus on värv.  

**Avaldis:** \[If Color == "Roheline", 1,5, 1,0\]  

Kauba konfigureerimisel määratakse toitejuhtme pikkuseks **1,5**, kui määrate värviatribuudiks **Roheline**. Kui määrate mõne muu värvi, määratakse pikkuseks **1**. Kuid kuna arvutused on ühesuunalised, ei määra arvutus värviatribuudi väärtuseks **Roheline**, kui määrate pikkuseks **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Mis juhtub, kui arvutusel on täisarvu tüüpi sihtatribuut, kuid arvutus loob kümnendarvu?
Kui sihtatribuut on täisarvu tüüpi, kuid arvutus loob kümnendarvu, tagastatakse ainult arvutuse täisarvuline osa. Kümnendosa eemaldatakse ja tulemust ei ümardata. Näiteks arvu 12,70 tulemusena kuvatakse 12.

## <a name="when-do-calculations-occur"></a>Millal arvutused toimuvad?
Arvutused toimuvad, kui on esitatud kõigi sisendatribuutide väärtus.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Kas saan sihtatribuudile arvutatud väärtuse üle kirjutada?
Saate sihtatribuudile arvutatud väärtuse üle kirjutada, kui sihtatribuut pole määratud peidetuks või kirjutuskaitstuks.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Kuidas määrata sihtatribuut peidetuks või kirjutuskaitstuks?
Atribuudi määramiseks peidetuks või kirjutuskaitstuks tehke järgmist.

1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Toote konfiguratsioonimudelid**.
2.  Valige toote konfiguratsioonimudel ja klõpsake seejärel tegevuspaanil suvandit **Redigeeri**.
3.  Valige lehel **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** sihtatribuudina kasutatav atribuut.
4.  Valige kiirkaardil **Atribuudid** suvand **Peidetud** või **Kirjutuskaitstud**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Kas arvutus saab minu määratud väärtused üle kirjutada?
Nr Kasutatakse toote konfigureerimisel määratud väärtusi. Arvutus, mis toimub, kui muudetakse arvutuse sisendväärtusi, ei saa konkreetse atribuudi kohta esitatud väärtusi üle kirjutada.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Mis juhtub, kui eemaldan arvutusest sisendväärtuse?
Sisendväärtuse eemaldamisel arvutusest eemaldatakse ka sihtatribuudi väärtus.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Miks saan tõrketeate, mis ütleb, et minu mudelis on vastuolu?
See teade kuvatakse, kui arvutuses on viga või kui ühes või mitmes piirangus on vastuolu. Lisateavet piirangutes olevate vastuolude kohta saate jaotisest [Avaldise piirangud ja tabeli piirangud](expression-constraints-table-constraints-product-configuration-models.md). Siin on mõned olukorrad, kus arvutustes võib ilmneda vigu.

-   Väärtus on jagatud nulliga (0).
-   Kahe järgmise elemendi vahel on konflikt:
    -   väärtused, mis on atribuudi puhul saadaval ja piiranguga piiratud;
    -   arvutusega loodud väärtus.
-   Arvutusega saadud väärtused on väljaspool atribuudi domeeni. Näiteks on täisarv vahemikus \[1.. 10\], mis on arvutatud nulliks.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Miks saan tõrketeate, kuigi minu tootemudeli kinnitamine õnnestus?
Arvutusi ei kaasata kinnitamisse. Vigade leidmiseks arvutustes peab konfiguratsioonimudelit testima. Toote konfiguratsioonimudeli testimiseks järgige neid juhiseid.

1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Toote konfiguratsioonimudelid**.
2.  Valige toote konfiguratsioonimudel ja klõpsake seejärel tegevuspaanil grupis **Käita** suvandit **Katse**.





