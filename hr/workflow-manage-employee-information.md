---
title: "Töövoogude abil saate hallata töötajate teavitamise"
description: "See teema selgitab kasutamist inimressursi töövoo suudab hallata töötaja teavet. Näiteks saate töövoo seostada võimalik ja algas siis, kui töötajad muuta nende kinnitamise töövoo sätete konfigureerimine."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Töövoogude abil saate hallata töötajate teavitamise

See teema selgitab kasutamist inimressursi töövoo suudab hallata töötaja teavet. Näiteks saate töövoo seostada võimalik ja algas siis, kui töötajad muuta nende kinnitamise töövoo sätete konfigureerimine.

Töövoo võimega inimressursi annab personali tegevuse haldamise töövoogu. Lisaks mitmeid võimalusi on saadaval nii, et saate muuta tööprotsesse ja ühineda aruandluse hierarhia. Töövood on saadaval, et aidata hallata muudatusi mitme standardi tüüpi töötajateavet. Töövoo saab seostada võimalik. Siis, kui töötajad saavad töötaja kirje muutmiseks töövoo alustamist enne, kui uus teave salvestatakse kinnitust nõudva. Töövood on eelnevalt infot, mis aitavad teil tõhusalt hallata muudatusi ja hoida oma töötajate andmete täpne järgmisi:

-   ID-numbrid
-   Kursused
-   Haridus
-   Pilt
-   Laenatud üksused
-   Töökogemus
-   Projektikogemus
-   Oskused
-   Vastutavad positsioonid
-   Inimressursside meetmete
-   Kursusele registreerimine

Kui töötajad on palgatud, üle või lõpetada, saate lisada töövoo läbivaatamisprotsessi. Sel viisil saab muuta dokumendi või hagi seoses defineeritakse töövoo osa. Läbivaatamise protsessi lõppedes dokumendi või tegevus on lõpetatud ja töövoo avatakse samm lõpliku heakskiidu.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Töövoo seostada positsiooni hierarhia
Töövoo saab seostada hierarhia, mis konfigureerida. Näiteks, kui ametikoht on seotud maatriks andmete esitamise hierarhia, võis seadistada töövoog, mis suunab konkreetse projekti kulud projekti juhtiv töötaja, kes on seotud selle seisukoha manager asemel. Luua uue töövoo või muuta olemasoleva töövoo kohta ning **inimressursside töövoo** klõpsake valikul **uus**. Valige Töövoog töövoo designer alustamiseks loendis. Saate luua uue töövoo või muuta olemasoleva töövoo juhised projekteerija. Kui olemasoleva töövoo muutmiseks muudatused salvestatakse uue versioonina. Seetõttu siis saab alati tagasi minna eelmise versiooni kui pead.

## <a name="configure-a-human-resources-workflow"></a>Konfigureerige töövoog inimressursside
Põhilised töövoog, mis käivitatakse, kui töötajad taotleda oma isikukood muutmist konfigureerimiseks toimige järgmiselt.

1.  Kohta ning **inimressursside töövoogude** klõpsake valikul **uus**.
2.  Valige saadaolevate töövoogude loendist **identifitseerimisnumbrid**.
3.  Klõpsake **käivitada** alustada töövoo disainer ja seejärel sisestage oma kasutajanimi ja parool, kui küsitakse.
4.  Drag on **kinnitada registreerimise number** disainer lõuend töövoo elementide loendist element.
5.  Connect heakskiidu elemendi **alustada** ja **lõpuni**.
6.  Topeltklõpsake **kinnitamine elemendi**, ja seejärel paremklõpsake ja valige **atribuudid**.
7.  Tööjuhiste üksuse lisamiseks tehke järgmist
    1.  Valige **määramine**, ja seejärel valige **hierarhia** ülesande tüüp.
    2.  All on **hierarhia** valik, valige **seadistatav hierarhia**.
    3.  Stop tingimuse lisamine ja lehe sulgemiseks.

8.  Täitma täiendavaid juhiseid (hoiatusi pole veel peaks eksisteerima).
9.  Klõpsake käsku **Salvesta ja sule**. Aktiveerimine uue töövoo dialoog avaneb ning valige **aktiivseks muuta**.
10. Mine **töötajate**&gt;**positsioone**&gt;**paigutada hierarhia tüübid**.
11. Valige **maatriksi**.
12. Lisada ka **töötaja ID-koodi** loendisse töövoo.



