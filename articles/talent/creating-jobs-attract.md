---
title: Attractis töö loomine
description: Selles teemas kirjeldatakse Attarcti töö elemente. Lisaks selgitatakse, kuidas tööd luua.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9dcdbcea995285c879f91c0bff435103865cc10f
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832927"
---
# <a name="create-a-job-in-attract"></a>Attractis töö loomine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse töö elemente rakenduses Microsoft Dynamics 365 Talent: Attract. Lisaks selgitatakse, kuidas tööd luua.

## <a name="job-creation"></a>Töö loomine

Töid saavad luua administraatorid, värbajad ja personalijuhid. Töö loomisel palutakse teil valida oma roll protsessis: personalijuht või värbaja. Kui olete rolli valinud, palutakse teil valida protsessi mall. Kui valite **Jäta vahele**, kasutatakse vaikemalli. Protsessimallide kohta leiate lisateavet artiklist [Protsessimalli loomine Attractis](./process-templates-attract.md).

Attracti tööl on töö üksikasjad, värbamistöörühm, värbamisprotsess, töösisestused ja analüütika.

## <a name="job-details"></a>Töö üksikasjad

Vahekaart **Töö üksikasjad** sisaldab üksikasju töökohustuste ja atribuutide kohta. Ametinimetuse, töö kirjelduse ja töö asukoha väljad on nõutavad. Teised väljad pole kohustuslikud.

Välja **Vabade kohtade arv** vaikeväärtuseks **1**. Kuid te saate selle väärtust muuta. Kui tööle on pakkumine koostatud, vähendatakse välja **Vabade kohtade arv** väärtust.

Kui halduskeskuses on ametikoha haldamine sisse lülitatud, on saadaval otsing **Värskenda ametikohti**. See otsing loeb teenuse Common Data Service üksust JobPosition ja annab vastuseks loendi ametikohtadest, mida selle töö puhul saab valida. Kui valitud ametikohtade arv ületab vabade ametikohtade arvu, kuvatakse hoiatus. Samuti kuvatakse hoiatus, kui ametikohta kasutatakse mitme tööga.

> [!NOTE]
> Ametikoha haldus on saadaval tervikliku värbamise lisandmooduli korral.

Olenevalt värbamisprotsessi pakkumise tegevuse sätetest, saab ametikoha numbrit pakkumises kasutada kaks korda. Lisateavet vaadake jaotisest [Värbamisprotsessi toimingud](./activities-attract.md).

Attract sisaldav vaikimisi **Oskuste** komplekti. Need oskused kuvatakse trükkimisel soovitustena. Saate oskusi juurde lisada, sisestades uue oskuse teksti väljale ja vajutades sisestusklahvi.

Attract sisaldav vaikimisi **Tööfunktsioonide** komplekti. Saate kuni kolm tööfunktsiooni juurde lisada, sisestades uue tööfunktsiooni väljale ja vajutades sisestusklahvi.

Attract sisaldav vaikimisi **Ettevõtte valdkondade** komplekti. Saate kuni kolm ettevõtte valdkonda juurde lisada, sisestades uue ettevõtte valdkonna väljale ja vajutades sisestusklahvi.

## <a name="hiring-team"></a>Värbamistöörühm

Vahekaart **Värbamistöörühm** sisaldab tööga seotud isikute loendit. Kasutajate lisamisel värbamistöörühma peab neile määrama rolli värbamistöörühmas. Roll määrab, millistele andmetele kasutajatel juurdepääs on ja milliseid teavitusi nad saavad. Rollid, mida saab valida, on **Värbaja**, **Personalijuht**, **Delegaat** ja **Intervjueerija**. Lisainfot rolli privileegide kohta leiate dokumendist "Rollihaldus". Värbajad ja personalijuhid võivad määrata ühe või rohkem delegaate nende nimel töötama. Lisainfot delegaatide kohta leiate artiklist [Turvalisus ja rollihaldus Attractis](./security-attract.md).

Värbamistöörühma saab pärast töö aktiveerimist värskendada.

## <a name="process"></a>Töötlemine

Värbamisprotsessi vaiketeave põhineb töö loomisel valitud protsessimallil. Kui sel ajal kindlat malli ei valitud, kasutatakse vaikemalli. Kui määratlete värbamisprotsessi, saate lisada või eemaldada erinevaid etappe, välja arvatud potentsiaalselt sobiva kandidaadi, avalduse ja pakkumise etappe. Kuigi potentsiaalselt sobiva kandidaadi etappi ei saa eemaldada, võib selle välja lülitada. Igas etapis saate lisada või eemaldada ühe või mitu eelmääratletud tegevust.

Lisateavet toimingute kohta, mida saab värbamisprotsessis lisada, vaadake jaotisest [Värbamisprotsessi toimingud](./activities-attract.md).

> [!NOTE]
> Värbamisprotsessi saab pärast töö aktiveerimist värskendada.

## <a name="postings"></a>Sisestamised

Pärast töö aktiveerimist saab selle sisestada. Ainult värbajad ja administraatorid saavad töid sisestada. Töö saab sisestada kas rakendusse Talent Careers (Dynamics 365 Talent karjäärisait) või LinkedIni. Attracti meeskond töötab pidevalt töökuulutuste vahendajatega koostöös. See loend laieneb aja jooksul. Töö sisestamisel ainult sisesena vajavad kandidaadid töö vaatamiseks ja sellele kandideerimiseks AAD kontot. Kui töö on loetletud avalikuna, saavad kandidaadid töid vaadata ja neile kandideerida kõiki autentimissuvandeid kasutades. 

Töökuulutuste kohta lisateabe saamiseks vaadake jaotist [Karjäärisaidi seadistamine rakenduses Microsoft Dynamics 365 Talent – Attract](career-site.md).

> [!NOTE]
> Töösisestuste funktsionaalsus on saadaval ainult tervikliku värbamise lisandmooduliga Attractile.

## <a name="activate"></a>Aktiveeri

Pärast seda, kui töö on aktiveeritud, saab sellele potentsiaalselt sobivaid kandidaate ja kandidaate lisada. Tööle potentsiaalselt sobivate kandidaatide lisamise valik on määratud värbamisprotsessi potentsiaalselt sobiva kandidaadi tegevuses.

> [!NOTE]
> Värbamisprotsessi saab pärast töö aktiveerimist värskendada.

## <a name="prospects-and-applicants"></a>Potentsiaalselt sobivad kandidaadid ja kandidaadid

Võimalus lisada tööle värbamisprotsessis väljavaateid on seatud jaotises [Värbamisprotsessi toimingud](./activities-attract.md#prospect-activity). See valik peaks olema enne töö aktiveerimist määratud.. Pärast seda, kui töö on aktiveeritud, saab sellele potentsiaalselt sobivaid kandidaate ja kandidaate lisada.

## <a name="approvals"></a>Kinnitused

Attracti töid saab kinnitamiseks esitada. Kõik tööd ei vaja kinnitamist. Nõue määratakse malli tasandilt. Vaikimisi on mallil kinnitused välja lülitatud. Kinnituste seadistamiseks minge protsessimallile ja määrake väli **Kinnitamine** vaikeväärtuseks. Siis valige tööd luues see mall.

Pärast töö salvestamist saab selle kinnitamiseks esitada. Järgnev tabel loetleb kinnitamist kasutava dokumendi olekut.

| Olek   | Riik                                                               |
|----------|---------------------------------------------------------------------|
| Mustand    | Töö on salvestatud, kuid see pole töövoogu esitatud. |
| Ootel  | Töö on edastatud kinnitajatele.                            |
| Kinnitatud | Töö on kinnitatud, kuid see ei ole aktiveeritud.            |
| Tagasi lükatud | Töö on tagasi lükatud ja seda ei saa aktiveerida.               |
| Aktiivne   | Töö on kinnitatud ja aktiveeritud.                            |

Tööde loendis, saate filtreerida tööde olekuid.

Kinnitusi saab saata ettevõttes mis tahes Microsoft Azure Active Directory (Azure AD) kasutajale. Kinnitused saadakse paralleelselt kõigile inimestele, kes on kinnitajate loendis. Kõik kinnitajad peavad töö heaks kiitma, enne kui see saab edasi liikuda. Kui üks kinnitaja lükkab töö tagasi, kuvatakse töö olekuna **Tagasi lükatud**. Pärast töö kinnitamist saab selle aktiveerida.

Kui kasutaja redigeerib tööd, kui see on kinnitatud, kuid mitte aktiveeritud, lähtestatakse töö olekule **Mustand** ja töö tuleb uuesti kinnitamiseks esitada. Kui kinnitatud töö on aktiveeritud, ei saa seda enam redigeerida.

Kinnitajatena loetletud inimesed saavad Attracti teatise ja meili, mis annab teada, et neil on üksus kinnitamiseks.  Meilis saavad kinnitajad klõpsata linki töö avamiseks, üksikasjade ülevaatamiseks ja kas kinnitamiseks või tagasilükkamiseks. Kui töö olekuks on seatud **Kinnitatud** või **Tagasi lükatud**, teavitatakse esitajat Attractis ja talle saadetakse meil. Samuti saavad kinnitajad meeldetuletusmeili, kui nad pole kinnitustaotlusele 24 tunni jooksul vastanud.

> [!NOTE]
> saate luua kinnitusmeilide jaoks kohandatud meilimalle. Lisateabe saamiseks vt teemat [Meilimallide loomine ja haldamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Töö loomine

Töö loomiseks toimige järgmiselt.

1. Minge valikusse **Tööd**.
2. Valige suvand **Uus**.
3. Sisestage töö nimetus väljale **Töö nimetus**. Sisestage oma roll väljale **Roll**.
4. Valige mall väljal **Mall**. Teise võimalusena valige **Jäta vahele**. Kui valite **Jäta vahele**, kasutatakse vaikemalliks märgitud malli.

    Kui dokumendi peab läbima kinnitusprotsessi, valige mall mille väli **Kinnitusprotsess** on määratud **Vaikimisi** peale.

5. Sisestage töö üksikasjad vahekaardile **Üksikasjad**. Väljad **Pealkiri**, **Töö kirjeldus** ja **Asukoht** on nõutavad.
6. Valige **Salvesta**.
7. Lisage vahekaardile **Värbamistöörühm** personalijuht, värbaja või intervjueerija.
8. Valige **Salvesta**.
9. Vajadusel lisage etappe vahekaardile **Protsess** või eemaldage sealt etappe.

    - Etapi lisamiseks valige **+ Uus etapp**.
    - Etapi eemaldamiseks hoidke kursorit eemaldatava etapi kohal ja valige seejärel ilmunud prügikastinupp.

        > [!NOTE]
        > Potentsiaalselt sobiva kandidaadi, avalduse ja pakkumise etappe ei saa eemaldada.

10. Vajadusel lisage või eemaldage tegevusi.

    - Tegevuse lisamiseks lohistage see paremal asuvast loendist otse sobivasse etappi. Teise võimalusena topeltklõpsake tegevusel ja valige etapp, kuhu see lisada.
    - Tegevuse eemaldamiseks laiendage tegevust ja seejärel valige prügikasti nupp tegevuse päises.

11. Valige **Salvesta**.
12. Kui valisite kinnitusprotsessi kasutamise, toimige järgmiselt.

    1. Valige suvand **+ Lisa kinnitaja** ja sisestage kasutaja, kellel on Azure AD konto. Saate lisada mitu kinnitajat.
    2. Valige **Saada kinnitajatele**.

    Töö väli **Töö olek** määratakse **Ootel** peale. Pärast välja **Töö olek** muutumist olekusse **Kinnitatud**, saab töö aktiveerida.

13. Töö aktiveerimiseks valige **Aktiveeri**.
14. Töö sisestamiseks avage **Töökuulutused**, ja seejärel valige Talent Careers saidi või LinkedIni all **Sisesta kohe**.
