---
title: Laiendatud sisselogimise võimaluse häälestamine ja kasutamine
description: See artikkel kirjeldab, kuidas seadistada Microsoft Dynamics 365 Commerce ja kasutada müügikoha rakenduse laiendatud sisselogimisvõimalusi.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e27e8d94adccc46559089928b0481442306567ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884307"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Laiendatud sisselogimise võimaluse häälestamine ja kasutamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada Microsoft Dynamics 365 Commerce ja kasutada müügikoha rakenduse laiendatud sisselogimisvõimalusi.

Cloud POS-i (CPOS) ja Modern POS-i (MPOS) pakute laiendatud sisselogimise võimalust, mis võimaldab kaupluse töötajatel kassa rakendusse sisse logida, skannides vöötkoodi või tõmmates kaardi magnetribalugeja (MSR) abil.

## <a name="set-up-extended-logon"></a>Seadista laiendatud sisselogimine

Kaupluse kassaregistrite laiendatud sisselogimise häälestamiseks järgige neid samme.

1. Minge commerce headquartersi jaemüügi ja ärikanali häälestamise **kassa \> häälestuse \> kassaprofiilide \> funktsiooniprofiilidele \>**. 
2. Valige vasakul navigeerimispaanil kauplusega seostatud funktsiooniprofiil.
3. Seadke funktsiooni **kiirkaardi** jaotises Täiendavad **sisselogimise autentimise suvandid** väärtusele Jah **või** **Ei vastavalt vajadusele**.

    - **Personali vöötkoodi sisselogimine** – häälestage see valik valikule **Jah**, kui soovite töötajatel kassasse sisse logida vöötkoodi skannides. 
    - **Personali vöötkoodiga sisselogimisel** on nõutav parool – **määrake see valik väärtusele Jah**, kui soovite töötajatel sisestada kassasse sisselogimisel parooli vöötkoodi skannides.
    - **Personali kaardi sisselogimine** – määrake selle suvandi väärtuseks **Jah**, kui soovite, et teie töötajad kaardi tõstdes kassasse sisse logiks.
    - **Personali kaardiga sisselogimisel** on nõutav parool – **määrake** selle suvandi väärtuseks Jah, kui soovite, et teie töötajad sisestaks kassasse sisse logides parooli kaardi tõstmise abil.

Vöötkood või kaart on seotud mandaatidega, mille saab töötajale määrata. Mandaatide arv peab olema vähemalt kuus tähemärki. Esimest viit tähemärki sisaldav string peab olema kordumatu ja *seda peetakse töötaja otsimiseks mandaadi ID-ks*. Ülejäänud märke kasutatakse turvalisuse kinnitamiseks. Näiteks on teil kaks kaarti, millest ühel on mandaat 12345DTAGEMDEYTDW ja ühe kaardiga 12345EWUTBDTAGEMH. Kuna neil kahel kaardid on sama mandaadi ID-ga 12345, ei saa neid mõlemaid töötajatele edukalt määrata.

## <a name="assign-extended-logon"></a>Määra laiendatud sisselogimine

Vaikimisi saavad töötajatele laiendatud sisselogimist määrata ainult juhid. Laiendatud sisselogimise määramiseks avage kassas valik **Laiendatud sisselogimine**. Seejärel otsige töötajat, sisestades otsinguväljale tema operaatori ID. Valige töötaja ja klõpsake seejärel nuppu **Määra**. Järgmisel leheküljel tehke töötajale laiendatud sisselogimise määramiseks kaaarditõmme või ‑skann. Kui kaarditõmme või ‑skann on edukalt loetud, ilmub nupp **OK**. Töötajale laiendatud sisselogimise salvestamiseks klõpsake nuppu **OK**.

## <a name="delete-extended-logon"></a>Kustuta laiendatud sisselogimine

Töötajale määratud laiendatud sisselogimise kustutamiseks otsige töötajat toimingu **Laiendatud sisselogimine** abil. Valige töötaja ja klõpsake seejärel nuppu **Eemalda määrang**. Kõik töötajaga seostatud laiendatud sisselogimise identimisteave eemaldatakse.

## <a name="use-extended-logon"></a>Kasuta laiendatud sisselogimist

Kui laiendatud sisselogimine on konfigureeritud ja töötajale on määratud vöötkood või magnetriba, peab töötaja oma kaarti tõmmake või skannima, kuni müügikoha sisselogimisleht kuvatakse. Kui parool on nõutav ka enne sisselogimise jätkamist, palutakse töötajal sisestada oma parool.

## <a name="extend-extended-logon"></a>Pikenda laiendatud sisselogimist

Laiendatud sisselogimise võimaluse boksist väljas rakendamine nõuab, et mandaatide pikkus oleks vähemalt kuus tähemärki ja esimesed viis tähemärki (mandaadi ID) on kordumatud. See oli algselt mõeldud näidisna, mille arendajad saavad kohandada konkreetse rakenduse nõuetele. (Näiteks saab seda kohandada, et toetada rohkem märke või kasutada erinevaid turbekontrolli reegleid.) Lisateavet laiendatud sisselogimise laiendite [koostamise kohta vt MPOS-i ja Pilve kassa laiendatud sisselogimisfunktsiooni laiendamine](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Sisselogimisteenust saab laiendada ka täiendavate laiendatud sisselogimisseadmete (nt palmskannerite) toetamiseks. Lisateavet vt kassa laiendatavuse [dokumentatsioonist](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
