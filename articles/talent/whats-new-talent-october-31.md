---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (31. oktoober 2018)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talent Core HR-i uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517830"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (31. oktoober 2018)

[!include [banner](includes/banner.md)]

**Järk 8.1.2031**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Linkide loomine Talentist Finance and Operationsini
See uus navigeerimisfunktsioon võimaldab teil linkida Talentist Finance Operationsini, pakkudes teile otsest navigeerimist Finance and Operations lehtedel. Kui lingid on konfigureeritud, saate määratleda lingi nime ja grupi, kus link peaks rakenduses Talent asuma ja sihtlehe, mis peaks Finance and Operationsiga avanema.

#### <a name="coming-soon"></a>Peagi tulekul
Tulevikus lisatakse välja kontekst, et võimaldada otsest navigeerimist Finance and Operations vastavatele kirjetele. Näiteks saate kasutada **Lingi väljale**, et pakkuda konteksti, navigeerimaks otse konkreetse töövõtja või asukoha juurde Finance and Operationsis.

### <a name="configure-target-systems"></a>Sihtsüsteemide konfigureerimine

Rakenduse Talent süsteemiadministraatoris saate määratleda lingid, mis ilmnevad läbi Süsteemiadministraatori tööruumi. Konfiguratsiooni osaks on Finance and Operationsi keskkonnad, kuhu soovite kui lingi "sihtkohta" navigeerida. Saate seda teha, andes sihtsüsteemile nime ja Finance and Operationsi keskkonna URL-i. Siin on näide antavast Finance and Operationsi URL-ist: https://devax00124aos.cloud.test.dynamics.com/. Pärast oma sihtsüsteemi konfigureerimist saate määratleda oma lingid.

### <a name="configure-links"></a>Konfigureeri lingid

Iga loodud lingi kohta määratletakse järgmine teave.

- Link – lingi nimi, mida kasutatakse ainult tuvastamiseks.

- Lingi lubamine – seatud olekusse **Jah**, kui soovite linki Talenti kasutajatele kuvada.

- Kuvatav nimi – määratlege nimi, mis ilmub lingina Finance and Operationsis. Need andmed ei ole praegu tõlgitud.

- Lingi ilmutamise vorm – valige, missugusel lehel soovite linki kuvada.

- Grupp – grupid ei ole kohustuslikud, kuid kui soovite linke gruppide abil korraldada, valige olemasolev grupp või looge uus, kasutades **Grupi** välja.

- Sihtsüsteem – valige sihtsüsteem, mis loodi, kasutades **Sihtsüsteemi konfigureerimise** suvandit. See saab olema Finance and Operationsi keskkond, mida kasutatakse lingiga navigeerides.

- Kasuta kasutaja praegust ettevõtet – valige **Jah**, kui soovite Finance and Operationsi navigeerimiesl kasutada kasutaja praeguse ettevõtte konteksti. Kui valitakse **Ei**, saate valida ettevõtte, mida tuleks kasutada.

- Sihtmenüü käsk – sisestage Finance and Operationsi menüükäsk, mida link peab navigeerimisel kasutama. Otse navigeeritavad menüü-üksused ei ole saadaval. Nõutava menüü-üksuse leidmiseks avage Finance and Operations ja avage navigeerimise sihtlehekülg. Kopeerige menüü-üksus URL-ist. Kui soovite näiteks, et link viiks teid töövõtjate loendisse Finance ja Operationsis, sisestage väärtus, mis kuvatakse URL-is pärast "&mi"-d. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Töövõtja loendi lehele navigeerimise menüü-üksus on selles näites: HcmWorkerListPage_Employees.

- Andmeallika link – valige andmeallikas, millele link viitab. Saadaval on kõige tavalisemad allikad nagu **Töötaja** ja **Ametikoht**.

- Link väljale (tuleb varsti) – see välja valik võimaldab otsest navigeerimist üksikult kirjelt rakenduses Talent, üksikule kirjele rakenduses Finance and Operations.

### <a name="access-to-links"></a>Juurdepääs linkidele

Süsteemiadministraatorid näevad vastloodud linke määratletud lehtedel isegi siis, kui **Lingi lubamise** suvandiks on määratud **Ei**. Seda saab kasutada linkide kontrollimiseks enne nende ilmutamist teistele töövõtjatele. Kõik teised rollid näevad vaid konfigureeritud linke pärast seda, kui valiku **Lingi lubamise** suvandiks on määratud **Jah**. Töövõtjatel, kellel on juurdepääs lehekülgedele, kuhu lingid on ilmutatud, on juurdepääs ka linkidele.

Kasutajatele võib ka rakenduses Finance and Operations määratleda turvaõigused, et pääseda ligi lehekülgedele Finance and Operationsis. Kui õiguseid ei ole, kuvatakse lingi kasutamisel turva dialoogiboks.


## <a name="other-changesfixes"></a>Muud muudatused/parandused

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Uuele töövõtjale ei saa määrata ametikohti, mille alguskuupäev on tulevikus

Nüüd on võimalik määrata töövõtja ametikohale, mille alguskuupäev on tulevikus. Valida saab ametikohti, mille alguskuupäevad on tulevikus ja töövõtja määramine viiakse lõpule salvestamisel või töövoo lõpetamisel (kui töövoog on lubatud).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Uut töötajad ei saa olemasolevale ametikohale määrata

Nüüd saab uusi töötajaid määrata olemasolevatele ametikohtadele.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Staaži kuupäev / kontori asukoht kaovad, kui töösuhte alguskuupäev on minevikus ja kirje salvestatakse

Parandatud on **Staaži kuupäeva** ja **Kontori asukoha** nähtavust endiste töötajate muudatuste salvestamisel.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Ei saa sisestada andmeid tulevikus olevate töösuhete jaoks töötaja lehel

Tööhõiveandmed on tulevikus olevate töösuhete jaoks põhilisel töötaja lehel keelatud. Tööhõiveandmeid saab sisestada **Kuupäevahalduri** lehekülgedelt. Tulevastes väljaannetes tehakse lisamuudatusi, et võimaldada tööhõiveandmete sisestamine töövoo protsessi ajal.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Lisage ValidFrom ja ValidTo HcmPersonalContactPersonEntity

Andmehalduse raamistiku (DMF) üksus HcmPersonalContactPersonEntity on uuendatud ning sisaldab "kehtiv alates" ja "kehtiv kuni" kuupäevasid, et võimaldada teatud intgratsioonistsenaariumite soodustusi. 

## <a name="known-issue"></a>Teadaolev probleem
- **Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid. 
- **Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud. Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud. (See probleem lahendatakse järgmisel platvormivärskendusel.)
