---
title: Hoolduse kontrollnimekirjad
description: Selles teemas tutvustatakse hoolduse kontrollnimekirju varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1091af424f84265ffa7983fca8ddc3f66138a5cd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426078"
---
# <a name="maintenance-checklists"></a>Hoolduse kontrollnimekirjad

[!include [banner](../../includes/banner.md)]



Hoolduse kontrollnimekirjad on loodud hooldustööde tüüpide järgi. Täidate hoolduse kontrollnimekirjad töökäsu täitmise osana. Lisateabe saamiseks hooldustööde tüüpide hooldustööde kontrollnimekirjade seadistamise kohta lehel **Hooldustöö tüübi vaikesuvandid**, vt teemat [Hooldustööde tüüpide kategooriad ja hooldustööde tüübid, hooldustööde tüüpide variandid, hooldustööde vahetused ja hooldustööde kontrollnimekirjad](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Kui töötate hooldustööde kontrollnimekirjadega töökäsu alusel, saate täita eelnevalt määratletud hooldustööde kontrollnimekirjad, mis on seotud hooldustööde tüüpidega. Saate lisada ka rohkem hoolduse kontrollnimekirju.


## <a name="fill-in-a-maintenance-checklist"></a>Hoolduse kontrollnimekirja täitmine

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk ja seejärel tehke tegumiriba vahekaardi **Töökäsk** jaotises **Read Lines** valik **Hoolduse kontrollnimekiri**.

3. **Töökäsu hooldustööde kontrollnimekirjas** kuvatakse kõikide töökäsu tööde kontrollnimekirjad. Kui töökäsu töödel on erinevad hooldustöö tüübid, võivad hooldustööde kontrollnimekirjad olla igal töökäsu töö jaoks erinevad. Valige seotud hooldustööde kontrollnimekirjaga töötamiseks töökäsu töö. Valitud hoolduse kontrollnimekirja rida kuvatakse kiirkaardil **Rea üksikasjad**.

4. Täitke kõik hoolduse kontrollnimekirjade read ükshaaval järjestuses, milles neid kuvatakse. Lõpetate hoolduse kontrollnimekirja rea täites väljad vahekaardil **Rea üksikasjad**. Rea lõpetamiseks vajalik teave võib varieeruda olenevalt rea tüübist. Näiteks saate reale tüübiga **Tekst** lisada märkuse, mis selgitab kontrolli tulemust. Reale tüübiga **Mõõtmed** saate sisestada loenduri väärtuse, mille saite seadmest ja samuti saate vajadusel lisada märkuse. Allpool toodud hoolduse kontrollnimekirjade ridade rühmitamiseks kasutatakse pealkirjana tüüpi **Päis** hoolduse kontrollnimekirja rida. Te ei pea päist täitma. Nagu kõigi teiste hoolduse kontrollnimekirjade ridade jaoks, saate märkuse lisada ka reale tüübiga **Päis**.

5. Kui juhised on seotud hoolduse kontrollnimekirja reaga, on märgitud ruut **Juhised**. Lugege valitud hooldusnimekirja rea juhiseid kiirkaardi **Rea üksikasjad** väljalt **Juhised**.

6. Kui olete hoolduse kontrollnimekirja rea täitnud, märkige real ruut **Märgitud**, et märkida see lõpetatuks. Kui soovite hoolduse kontrollnimekirja reast loobuda, kuna see pole töökäsu töö jaoks asjakohane, märkige real ruut **N/A**. Kui hoolduse kontrollnimekirja real on märgitudruut **Kohustuslik**, peate märkima kas ruudu **Märgitud** või ruudu **N/A**.

>[!NOTE]
>Hoolduse kontrollnimekirja registreerimist saate värskendada ainult siis, kui töökäsk on [Aktiivses](../setup-for-work-orders/work-order-lifecycle-states.md) töötsükli olekus.  


## <a name="add-a-maintenance-checklist-line"></a>Lisage hoolduse kontrollnimekirja rida

Hoolduse kontrollnimekirjad luuakse hooldustöö tüübi vaikesätte määratlusest ja kantakse üle töökäsu tööks. Vajadusel saate lisada hooldustööde kontrollnimekirja read töökäsule. Käsitsi lisatud hoolduse kontrollnimekirja read saavad viite **Käsitsi**.

1. Valige lehel **Töökäsu hooldustöö kontrollnimekiri** töökäsu töö, millele soovite hoolduse kontrollnimekirja lisada.

2. Kiirkaardil **Hoolduse kontrollnimekirja read** valige hoolduse kontrollnimekirja rida. Uue rea lisamiseks pärast valitud rida, vajutage **Allanoole** klahvi. Järjestuse järgmine number sisestatakse automaatselt väljale **Rea number**. Uue rea lisamiseks enne valitud rida valige **Lisa rida.** 

3. Sisestage väljale **Nimi** hoolduse kontrollnimekirja rea nimi.

4. Väljal **Tüüp** valige hoolduse kontrollnimekirja rea tüüp. Kiirkaart **Rea üksikasjad** sisaldab iga hoolduse kontrollimekirja tüübiga seotud välju.
    - **Tekst** – kasutage seda tüüpi, et lisada hoolduse kontrollnimekirja rida, millel on tekst, mis kirjeldab, mida tuleb teha. Kasutage seda hoolduse kontrollnimekirja tüüpi näiteks siis, kui soovite, et töötaja midagi kontrolliks või üle vaataks, kuid te ei oota konkreetset (mõõdetavat) tulemust. Pärast selle tüübi valmist sisestage kiirkaardi **Ridade üksikasjad** väljale **Juhised** tekst, mis kirjeldab, mida tuleb teha.
    - **Päis** – seda tüüpi hoolduse kontrollnimekirjade rida kasutatakse selle all kuvatavate hoolduse kontrollnimekirja ridade rühmitamiseks. See tüüp on kasulik, kui teil on mitu hoolduse kontrollnimekirja rida, mida saab jagada konkreetseteks tööaladeks. Pärast selle tüübi valimist sisestage väljale **Nimi** kirjeldav nimi.
    - **Mall** – see tüüp pole rakendatav, kui lisate hooldustööde kontrollnimekirja rea töökäsku käsitsi.  
    - **Muutuja** – kasutage seda tüüpi vahemiku võimaliku tulemuse määratlemiseks hoolduse kontrollnimekirja real. Lisateavet hoolduse kontrollnimekirjade muutujate seadistamise kohta vt teemast [hooldustööde tüüpide kategooriad ja hooldustööde tüübid, hooldustööde tüüpide variandid, hooldustööde vahetused ja hooldustööde kontrollnimekirjad](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Pärast selle tüübi valimist sisestage väljale **Nimi** muutuja kirjeldav nimi. Valige muutuja kiirkaardi **Rea üksikasjad** väljalt **Muutuja**. Väljale **Juhised** sisestage tekst, mis kirjeldab seda, mida tuleb teha.
    - **Mõõtmed** – kasutage seda tüüpi kindla mõõtmise kirjendamiseks hoolduse kontrollnimekirja real. Pärast selle tüübi valimist sisestage väljale **Nimi** mõõtme nimi. Valige sobivad väärtused kiirkaardi **Rea üksikasjad** väljadel **Loendur** ja **Ühik**. Väljale **Juhised** sisestage tekst, mis kirjeldab seda, mida tuleb teha.

5. Kui olete hoolduse kontrollnimekirja read käsitsi täitnud, täitke read, nagu on kirjeldatud eespool toodud jaotises **Hoolduse kontrollnimekirja täitmine**.

>[!NOTE]
>Lehel **Töökäsu hooldustöö kontrollnimekiri** ei saa kustutada hoolduse kontrollnimekirja ridu, mille viiteks on **Töö tüüp**. Kustutada saate ainult hoolduse kontrollnimekirja ridu, mille olete ise või on teised hooldustöötajad käsitsi loonud ja millel on viide **Käsitsi**.

Alljärgneval joonisel on esitatud hoolduse kontrollnimekirja näide.

![Joonis 1](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]