---
title: Töövoogude kasutamine töövõtja teabe haldamiseks
description: See artikkel selgitab, kuidas saate töötaja teabe haldamiseks kasutada inimressursside töövoo võimalust. Näiteks saate seostada töövoo positsiooniga ja konfigureerida kinnitamise töövoo, mis käivitatakse, kui töötajad muudavad oma kirjet.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aba7627877cd9b79dce5930e528f892e2d80baac
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058748"
---
# <a name="use-workflows-to-manage-employee-information"></a>Töövoogude kasutamine töövõtja teabe haldamiseks

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab, kuidas saate töötaja teabe haldamiseks kasutada inimressursside töövoo võimalust. Näiteks saate seostada töövoo positsiooniga ja konfigureerida kinnitamise töövoo, mis käivitatakse, kui töötajad muudavad oma kirjet.

Inimressursside töövoo võimalus annab hulgaliselt töövoogusid inimressursside tegevuste haldamiseks. Lisaks on saadaval mitmed valikud, et saaksite muuta spetsiifilisi töövoogusid ja seostada neid aruandlushierarhiaga. Töövood on saadaval, et hallata muudatusi mitmele töötajateabe standardsele tüübile. Saate seostada töövoo positsiooniga. Kui töötajad muudavad seejärel oma töötaja kirjet, käivitatakse töövoog, mis nõuab enne uue teabe salvestamist kinnitust. Töövood määratletakse eelnevalt järgmiste teabetüüpide puhul, et aidata teil tõhusalt muudatusi hallata ja töötajate andmete täpsust säilitada.

-   ID-numbrid
-   Kursused
-   Haridus
-   Pilt
-   Laenatud üksused
-   Töökogemus
-   Projektikogemus
-   Oskused
-   Vastutavad positsioonid
-   Inimressursside tegevused
-   Kursusele registreerimine

Töötajate palkamisel, üleviimisel või nendega töösuhte lõpetamisel võib töövoog hõlmata ülevaatamise protsessi. Sellisel viisil saab dokumenti parandada või tegevuse tingimusi määratleda osana töövoost. Ülevaatamisprotsessi lõpuleviimisel viiakse dokument või tegevus lõpule ja töövoog liigub lõplikku kinnitamisetappi.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Töövoo seostamine positsioonihierarhiaga
Saate seostada töövoo mis tahes konfigureeritava hierarhiaga. Näiteks kui positsioon on seotud maatriksi aruandluse hierarhiaga, võite konfigureerida töövoo, mis suunab spetsiifilise projekti kulud selle positsiooniga seotud töötaja juhataja asemel projekti müügivihjele. Uue töövoo loomiseks või olemasoleva töövoo muutmiseks klõpsake lehel **Inimressursside töövood** nuppu **Uus**. Töövoo kujundaja käivitamiseks valige loendis töövoog. Saate kasutada kujundajat uue töövoo loomiseks või etappide muutmiseks olemasolevas töövoos. Olemasoleva töövoo muutmisel salvestatakse teie muudatused uude versiooni. Lisaks saate vajaduse korral minna tagasi eelmisesse versiooni.

## <a name="configure-a-human-resources-workflow"></a>Inimressursside töövoo konfigureerimine
Konfigureerimaks põhitöövoogu, mis käivitatakse siis, kui töötajad nõuavad nende isikukoodi muutmist, järgige neid juhiseid.

1.  Lehel **Inimressursside töövood** klõpsake nuppu **Uus**.
2.  Saadaolevate töövoogude loendis valige **ID-koodid**.
3.  Klõpsake nuppu **Käivita**, et käivitada töövoo kujundaja ja sisestada seejärel vastava viiba kuvamisel oma kasutajanime ja parooli.
4.  Lohistage element **Kinnituse ID-number** töövoo elementide loendist kujundaja lõuendile.
5.  Ühendage kinnituse element valikuga **Algus** ja **Valmis**.
6.  Topeltklõpsake nuppu **Kinnita element** ning seejärel paremklõpsake ja valige suvand **Atribuudid**.
7.  Järgige tööüksuse juhiste lisamiseks neid juhiseid.
    1.  Valige **Määramine** ja seejärel valige määramistüübi valikus **Hierarhia**.
    2.  Valikus **Hierarhia** valige **Konfigureeritav hierarhia**.
    3.  Lisage peatamistingimus ja sulgege leht.

8.  Täitke mis tahes täiendavad juhised (täiendavaid hoiatusi ei tohiks olla).
9.  Klõpsake käsku **Salvesta ja sule**. Aktiveerige uus töövoog, kui dialoogiboks avaneb, ja valige **Muuda aktiivseks**.
10. Valige **Inimressurssid** &gt; **Ametikohad** &gt; **Positsiooni hierarhiatüübid**.
11. Valige suvand **Maatriks**.
12. Lisage loendisse töövoog **Töötaja ID-kood**.

## <a name="additional-resources"></a>Lisaressursid

[Aadressimuudatuste vaatamine ja haldamine](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]