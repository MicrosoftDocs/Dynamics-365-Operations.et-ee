---
title: Töövoogude kasutamine töövõtja teabe haldamiseks
description: Selles teemas selgitatakse, kuidas saate töövooge kasutada töötaja teabe haldamiseks.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d80ed49a4f423179997ac35562284a4e28af803f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068081"
---
# <a name="use-workflows-to-manage-employee-information"></a>Töövoogude kasutamine töövõtja teabe haldamiseks


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema selgitab, kuidas saate töötaja teabe haldamiseks kasutada inimressursside töövoo võimalust. Näiteks saate seostada töövoo positsiooniga ja konfigureerida kinnitamise töövoo, mis käivitatakse, kui töötajad muudavad oma kirjet.

Inimressursside töövoo võimalus annab hulgaliselt töövoogusid inimressursside tegevuste haldamiseks. Lisaks on saadaval mitmed valikud, et saaksite muuta spetsiifilisi töövoogusid ja seostada neid aruandlushierarhiaga. Töövood on saadaval, et aidata hallata mitut tüüpi töötajateabe muudatusi. Saate seostada töövoo positsiooniga. Kui töötajad muudavad seejärel oma töötaja kirjet, käivitatakse töövoog, mis nõuab enne uue teabe salvestamist kinnitust. Töövood on eelmääratletud järgmist tüüpi teabe jaoks, mis aitab teil muudatusi tõhusalt hallata ja töötajate andmeid täpsena hoida.

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

Töötajate palkamisel, üleviimisel või nendega töösuhte lõpetamisel võib töövoog hõlmata ülevaatamise protsessi. Sel viisil saab dokumenti muuta või toimingu tingimusi määratleda töövoo osana. Ülevaatamisprotsessi lõpuleviimisel viiakse dokument või tegevus lõpule ja töövoog liigub lõplikku kinnitamisetappi.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Töövoo seostamine positsioonihierarhiaga
Saate seostada töövoo mis tahes konfigureeritava hierarhiaga. Näiteks kui positsioon on seotud maatriksi aruandluse hierarhiaga, võite konfigureerida töövoo, mis suunab spetsiifilise projekti kulud selle positsiooniga seotud töötaja juhataja asemel projekti müügivihjele. Uue töövoo loomiseks või olemasoleva töövoo muutmiseks **valige lehel Inimressursside töövoog** suvand **Uus**. Töövoo kujundaja avamiseks valige loendist töövoog. Saate kasutada kujundajat uue töövoo loomiseks või etappide muutmiseks olemasolevas töövoos. Olemasoleva töövoo muutmisel salvestatakse teie muudatused uude versiooni. Lisaks saate vajaduse korral minna tagasi eelmisesse versiooni.

## <a name="configure-a-human-resources-workflow"></a>Inimressursside töövoo konfigureerimine
Konfigureerimaks põhitöövoogu, mis käivitatakse siis, kui töötajad nõuavad nende isikukoodi muutmist, järgige neid juhiseid.

1.  **Valige lehel Inimressursside töövood** suvand **Uus**.
2.  Saadaolevate töövoogude loendis valige **ID-koodid**.
3.  Töövookujundaja avamiseks valige **Käivita** ja sisestage küsimisel oma kasutajanimi ja parool.
4.  Lohistage element **Kinnituse ID-number** töövoo elementide loendist kujundaja lõuendile.
5.  Ühendage kinnituse element valikuga **Algus** ja **Valmis**.
6.  Topeltpuudutage (või topeltklõpsake) **Kinnitage element**, valige ja hoidke all (või paremklõpsake) ja seejärel valige **Atribuudid**.
7.  Järgige tööüksuse juhiste lisamiseks neid juhiseid.

    1.  Valige **Määramine** ja seejärel valige määramistüübi valikus **Hierarhia**.
    2.  Valikus **Hierarhia** valige **Konfigureeritav hierarhia**.
    3.  Lisage peatamistingimus ja sulgege leht.

8.  Täitke mis tahes täiendavad juhised (täiendavaid hoiatusi ei tohiks olla).
9.  Valige **Salvesta ja sule**. Aktiveerige uus töövoog, kui dialoogiboks avaneb, ja valige **Muuda aktiivseks**.
10. Valige **Inimressurssid** &gt; **Ametikohad** &gt; **Positsiooni hierarhiatüübid**.
11. Valige suvand **Maatriks**.
12. Lisage loendisse töövoog **Töötaja ID-kood**.

## <a name="additional-resources"></a>Lisaressursid

[Aadressimuudatuste vaatamine ja haldamine](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
