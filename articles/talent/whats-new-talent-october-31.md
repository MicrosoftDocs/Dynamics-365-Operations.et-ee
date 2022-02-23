---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (31. oktoober 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
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
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460938"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (31. oktoober 2018)

**Järk 8.1.2031**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.

## <a name="create-links-from-talent-to-finance"></a>Linkide loomine Talentist Finance’i
See uus navigeerimisfunktsioon võimaldab teil linkida Talentist Finance’i, pakkudes teile otsest navigeerimist Finance’i lehtedele. Kui lingid on konfigureeritud, saate määratleda lingi nime ja grupi, kus link peaks rakenduses Talent asuma ja sihtlehe, mis peaks Finance’is avanema.

#### <a name="coming-soon"></a>Peagi tulekul
Tulevikus lisatakse välja kontekst, et võimaldada otsest navigeerimist Finance’i vastavatele kirjetele. Näiteks saate kasutada **Lingi väljale**, et pakkuda konteksti, navigeerimaks otse konkreetse töövõtja või asukoha juurde rakenduses Finance.

### <a name="configure-target-systems"></a>Sihtsüsteemide konfigureerimine

Rakenduse Talent süsteemiadministraatoris saate määratleda lingid, mis ilmnevad läbi Süsteemiadministraatori tööruumi. Konfiguratsiooni osaks on Finance’i keskkonnad, kuhu soovite kui lingi "sihtkohta" navigeerida. Saate seda teha, andes sihtsüsteemile nime ja Finance’i keskkonna URL-i. Siin on näide antavast Finance’i URL-ist: https://devax00124aos.cloud.test.dynamics.com/. Pärast oma sihtsüsteemi konfigureerimist saate määratleda oma lingid.

### <a name="configure-links"></a>Konfigureeri lingid

Iga loodud lingi kohta määratletakse järgmine teave.

- Link – lingi nimi, mida kasutatakse ainult tuvastamiseks.

- Lingi lubamine – seatud olekusse **Jah**, kui soovite linki Talenti kasutajatele kuvada.

- Kuvatav nimi – määratlege nimi, mis ilmub lingina Finance’is. Need andmed ei ole praegu tõlgitud.

- Lingi ilmutamise vorm – valige, missugusel lehel soovite linki kuvada.

- Grupp – grupid ei ole kohustuslikud, kuid kui soovite linke gruppide abil korraldada, valige olemasolev grupp või looge uus, kasutades **Grupi** välja.

- Sihtsüsteem – valige sihtsüsteem, mis loodi, kasutades **Sihtsüsteemi konfigureerimise** suvandit. See saab olema Finance’i keskkond, mida kasutatakse lingiga navigeerides.

- Kasuta kasutaja praegust ettevõtet – valige **Jah**, kui soovite Finance’i navigeerimisel kasutada kasutaja praeguse ettevõtte konteksti. Kui valitakse **Ei**, saate valida ettevõtte, mida tuleks kasutada.

- Sihtmenüü käsk – sisestage Finance’i menüükäsk, mida link peab navigeerimisel kasutama. Otse navigeeritavad menüü-üksused ei ole saadaval. Nõutava menüü-üksuse leidmiseks avage Finance ja avage navigeerimise sihtlehekülg. Kopeerige menüü-üksus URL-ist. Kui soovite näiteks, et link viiks teid töövõtjate loendisse Finance and Operations rakenduses, sisestage väärtus, mis kuvatakse URL-is pärast "&mi"-d. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Töövõtja loendi lehele navigeerimise menüü-üksus on selles näites: HcmWorkerListPage_Employees.

- Andmeallika link – valige andmeallikas, millele link viitab. Saadaval on kõige tavalisemad allikad nagu **Töötaja** ja **Ametikoht**.

- Link väljale (tuleb varsti) – see välja valik võimaldab otsest navigeerimist üksikult kirjelt rakenduses Talent, üksikule kirjele rakenduses Finance.

### <a name="access-to-links"></a>Juurdepääs linkidele

Süsteemiadministraatorid näevad vastloodud linke määratletud lehtedel isegi siis, kui **Lingi lubamise** suvandiks on määratud **Ei**. Seda saab kasutada linkide kontrollimiseks enne nende ilmutamist teistele töövõtjatele. Kõik teised rollid näevad vaid konfigureeritud linke pärast seda, kui valiku **Lingi lubamise** suvandiks on määratud **Jah**. Töövõtjatel, kellel on juurdepääs lehekülgedele, kuhu lingid on ilmutatud, on juurdepääs ka linkidele.

Kasutajatele võib ka rakenduses Finance määratleda turvaõigused, et pääseda ligi lehekülgedele Finance and Operations rakenduses. Kui õiguseid ei ole, kuvatakse lingi kasutamisel turva dialoogiboks.


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
