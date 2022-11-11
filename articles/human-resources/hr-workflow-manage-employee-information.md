---
title: Töövoogude kasutamine töövõtja teabe haldamiseks
description: See artikkel selgitab, kuidas saate kasutada töövooge töötaja teabe haldamiseks.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750730"
---
# <a name="use-workflows-to-manage-employee-information"></a>Töövoogude kasutamine töövõtja teabe haldamiseks

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab, kuidas saate töötaja teabe haldamiseks kasutada inimressursside töövoo võimalust. Näiteks saate seostada töövoo positsiooniga ja konfigureerida kinnitamise töövoo, mis käivitatakse, kui töötajad muudavad oma kirjet.

Inimressursside töövoo võimalus annab hulgaliselt töövoogusid inimressursside tegevuste haldamiseks. Lisaks on saadaval mitmed valikud, et saaksite muuta spetsiifilisi töövoogusid ja seostada neid aruandlushierarhiaga. Töövood on saadaval, et aidata hallata erinevat tüüpi töötajateabe muudatusi. Saate seostada töövoo positsiooniga. Kui töötajad muudavad seejärel oma töötaja kirjet, käivitatakse töövoog, mis nõuab enne uue teabe salvestamist kinnitust. Töövood on eelmääratletud järgmiste teabetüüpide jaoks, mis aitavad tõhusalt muudatusi hallata ja töötajate andmeid täpsena hoida:

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

Töötajate palkamisel, üleviimisel või nendega töösuhte lõpetamisel võib töövoog hõlmata ülevaatamise protsessi. Sel viisil saab dokumendi üle vaadata või toimingu tingimusi töövoo osana määratleda. Ülevaatamisprotsessi lõpuleviimisel viiakse dokument või tegevus lõpule ja töövoog liigub lõplikku kinnitamisetappi.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Töövoo seostamine positsioonihierarhiaga

Töövoo saate seostada mis tahes konfigureeritud positsioonihierarhiaga. Töövoo marsruutimiseks kasutatakse kahte hierarhiatüüpi: juhtimis **- ja** **konfigureeritav**.

- Juhtimishierarhia **esindab** ettevõtte või organisatsiooni aruandlusstruktuuri. Lisateavet selle hierarhiatüübi kohta vt aruandelt [positsioonile](hr-personnel-positions.md#reports-to-position).
- Konfigureeritav **hierarhia** tähistab maatriksit või kohandatud hierarhiat. Lisateavet selle hierarhia tüübi kohta vt teemast [Seosed](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Juhtimishierarhia näide

Te võite konfigureerida töövoogu nii, et kui töötaja esitab ostutaotluse uude arvutisse, suunatakse taotlus töötaja juhatajale ja jätte taseme juhatajale. Kui konfigureerite töövoo sammu, seadke välja **Määrangu tüüp väärtuseks** **Hierarhia**. Vahekaart **Hierarhia** tüüp muutub seejärel kättesaadavaks. Näiteks valige **juhtimishierarhia**.

### <a name="configurable-hierarchy-example"></a>Konfigureeritav hierarhia näide

Kui ametikoht on seotud maatriksi aruandlushierarhiaga, saate konfigureerida töövoo, mis marsruutib kindla projekti kulud töötaja juhataja asemel projekti müügivihjele. Sellisel juhul seadke välja Määramise **tüüp väärtuseks** **Hierarhia**. Seejärel valige vahekaardil **Hierarhia** tüüp konfigureeritav **hierarhia**. Kui töövoog on **häälestatud**, valige **töövoo** häälestuse lehel suvand Seosta hierarhia, et valida hierarhia, mida tuleks kasutada töövoo marsruutimiseks.

> [!IMPORTANT]
> Kui dokument, kanne või koondkirje esitatakse töövoo kinnitamiseks, kasutatakse edastaja esmast ametikohta määramaks, kelle juurde dokument suunatakse.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hierarhia säte töövoo parameetrites

1. Minge töövoo **parameetrite lehel** hierarhia protsessi **.**
2. Vaikimisi on valiku **Kasuta positsioonihierarhiat** väärtuseks seatud **Ei**. Sel juhul kasutab töövoog töötaja esmast positsiooni, kui see navigeerib hierarhias. Seadistage valik Jah **,** et muuta töövoog kasutama ametikoha ema, kui see navigeerib hierarhias.

### <a name="additional-example"></a>Täiendav näide 

Töötaja Grace Sturmanil on kaks ametikohta: nõustaja ja töötaja. Ajapikenduse peamine positsioon on I väljaminek. Kui ta uute töötajatega ei koolitus, on ta saadaval konsultatsioonitöö jaoks. Oma peamise positsiooni kaudu annab Grace aru Inimressursside direktorile, oma ametile. Selle aruande abil saab aruandeid teha siis, kui teie aruanne on tagasi salvestatud. Oma nõustaja ametikohal on Grace’il mitmeid punktiirseost, sõltuvalt projektist.

Ajapikenduse ettevõte loob töövoo protsessireeglid, mis põhinevad konfigureeritaval **hierarhial** (maatriksi/projektipõhised hierarhiad). See hierarhia kasutab Grace’i nõustaja positsiooni. **·** **Kui suvand Kasuta ametikoha hierarhiat on seatud valikule Ei**, kui dokument marsruuditakse Grace’ile kinnitamiseks, siis töövoog näitab tema esmast positsiooni (kuupäev), et määrata, kuhu dokument järgmisena suunatakse. Sel juhul suunatakse see esmalt Sisestusklahvi ja Seejärel Sisestusklahvi. Kui suvandi väärtuseks on **seatud Jah** **ja** töövoog kasutab konfigureeritavat hierarhiat, siis nigege ajapikenduse nõustaja positsiooni ja aruandlussuhe määravad, kuhu dokument järgmisena suunatakse.

### <a name="configure-a-human-resources-workflow"></a>Inimressursside töövoo konfigureerimine
Konfigureerimaks põhitöövoogu, mis käivitatakse siis, kui töötajad nõuavad nende isikukoodi muutmist, järgige neid juhiseid.

1.  **Leheküljel Inimressursside töövood** valige **Uus**.
2.  Saadaolevate töövoogude loendis valige **ID-koodid**.
3.  Töövookujundaja **avamiseks** klõpsake nuppu Käivita ning sisestage seejärel kasutajanimi ja parool.
4.  Teisaldage **kujundaja lõuendile** elemendi Kinnita ID-number töövoo elementide loendist.
5.  Ühendage kinnituse element valikuga **Algus** ja **Valmis**.
6.  Topeltklõpsake (või topeltklõpsake) Elementi **Kinnita**, valige ja hoidke all (või paremklõpsake) ja valige **atribuudid**.
7.  Järgige tööüksuse juhiste lisamiseks neid juhiseid.

    1.  Valige **Määramine** ja seejärel valige määramistüübi valikus **Hierarhia**.
    2.  Valikus **Hierarhia** valige **Konfigureeritav hierarhia**.
    3.  Lisage peatamistingimus ja sulgege leht.

8.  Täitke lisajuhised.
9.  Valige **Salvesta ja sule**. Aktiveerige uus töövoog, kui dialoogiboks avaneb, ja valige **Muuda aktiivseks**.
10. Valige **Inimressurssid** &gt; **Ametikohad** &gt; **Positsiooni hierarhiatüübid**.
11. Valige suvand **Maatriks**.
12. Lisage loendisse töövoog **Töötaja ID-kood**.

## <a name="additional-resources"></a>Lisaressursid

[Aadressimuudatuste vaatamine ja haldamine](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
