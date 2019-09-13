---
title: Hoolduse kontrollnimekirjad
description: Selles teemas tutvustatakse hoolduse kontrollnimekirju varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875615"
---
# <a name="maintenance-checklists"></a>Hoolduse kontrollnimekirjad


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Hoolduse kontrollnimekirjad on loodud hooldustööde tüüpide järgi ja neid kasutatakse töökäskude puhul. Hoolduse kontrollnimekirjade täitmine on osa töökäsu täitmisest. Lisateabe saamiseks vt jaotisest [Hooldustööde tüüpide kategooriad ja hooldustööde tüübid, hooldustööde tüüpide variandid, hooldustööde vahetused ja hooldustööde kontrollnimekirjad](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md), hooldustööde tüüpide hooldustööde kontrollnimekirjade seadistamise kohta vormis **Hooldustööde vaiketüübid**.

Kui töötate hooldustööde kontrollnimekirjadega töökäsu alusel, saate täita eelnevalt määratletud hooldustööde kontrollnimekirjad, mis on seotud hooldustööde tüüpidega. Samuti on võimalik lisada täiendavaid hoolduse kontrollnimekirju.

## <a name="fill-out-a-maintenance-checklist"></a>Hoolduse kontrollnimekirja täitmine

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk ja klõpsake **Hoolduse kontrollnimekiri**.

3. **Töökäsu hooldustööde kontrollnimekirjas** näete kõikide töökäsu tööde hoolduse kontrollnimekirju. Kui töökäsu töödel on erinevad hooldustöö tüübid, võivad hooldustööde kontrollnimekirjad olla igal töökäsu tööl erinevad. Valige seotud hooldustööde kontrollnimekirjaga töötamiseks töökäsu töö. Valitud hoolduse kontrollnimekirja rida kuvatakse vahekaardil **Rea üksikasjad**.

4. Täitke kõik hoolduse kontrollnimekirjade read ükshaaval järjestuses, milles neid kuvatakse. Allpool toodud hoolduse kontrollnimekirjade ridade rühmitamiseks kasutatakse pealkirjana päise tüüpi hoolduse kontrollnimekirja rida. Päist ei pea te täitma, kuid nagu kõigi hoolduse kontrollnimekirjade puhul, on võimalik lisada päisesse **Märkus**.

5. Kui juhised on seotud hoolduse kontrollnimekirja reaga, on märgitud ruut **Juhised**. Lugege valitud hooldusnimekirja rea juhiseid vahekaardilt **Rea üksikasjad** > jaotisest **Juhised**.

6. Hoolduse kontrollnimekirja rea täitmiseks vajalik teave võib varieeruda, sõltuvalt seotud hoolduse kontrollnimekirja tüübist. Lõpetate hoolduse kontrollnimekirja rea täites väljad vahekaardil **Rea üksikasjad**. Näiteks rea tüübile "tekst" lisate **Märkuse**, milles selgitatakse, mis oli selle kontrollnimekirja rea tulemus. "Mõõtmed" tüüpi reale lisate seadmel loetud **Loenduri väärtuse** ja vajadusel saate lisada ka **Märkuse**.

- Kui olete hooldusnimekirja rea täitnud, märkige real ruut **Märgitud**, et märkida see lõpetatuks. Kui soovite hooldusnimekirja reast loobuda, kuna see pole töökäsu töö jaoks asjakohane, märkige real ruut **N/A**. Kui hooldusnimekirja rida on märgitud kui **Kohustuslik**, peate selle märkima kas "Märgitud" või "N/A".  
- Hoolduse kontrollnimekirja registreerimist saate värskendada ainult siis, kui töökäsk on [Aktiivses](../setup-for-work-orders/work-order-lifecycle-states.md) töötsükli olekus.  


## <a name="add-a-maintenance-checklist-line"></a>Lisage hoolduse kontrollnimekirja rida

Hoolduse kontrollnimekirjad luuakse hooldustöö tüübi vaikesätte määratlusest ja kantakse üle töökäsu tööks. Vajadusel saate lisada hooldustööde kontrollnimekirja read töökäsule. Käsitsi lisatud hoolduse kontrollnimekirja read saavad viite "Käsitsi".

1. Loendis **Töökäsu hooldustöö kontrollnimekiri** valige töökäsu töö, millele soovite hoolduse kontrollnimekirja lisada.

2. Vahekaardil **Hoolduse kontrollnimekirja read**, valige hoolduse kontrollnimekirja rida ja vajutage klaviatuuril allanoole klahvi, kui soovite valitud hoolduse kontrollnimekirja rea järel uue rea sisestada. Järjestuse järgmine number sisestatakse automaatselt väljale **Rea number**. Samuti võite valida hooldusnimekirja rea ja klõpsata nuppu **Lisa rida**, kui soovite sisestada valitud hoolduse kontrollnimekirja rea kohale uue rea.

3. Sisestage väljale **Nimi** hoolduse kontrollnimekirja nimi.

4. Väljal **Tüüp** valige hoolduse kontrollnimekirja rea tüüp. Iga hoolduse kontrollnimekirja tüübi puhul kuvatakse seotud väljad vahekaardil **Rea üksikasjad**.  
  a. "Teksti" kasutatakse hoolduse kontrollnimekirja rea lisamiseks koos teksti kirjeldusega, mida teha. Kasutage seda hooldusnimekirja tüüpi, kui soovite, et töötaja midagi kontrolliks või üle vaataks, kuid te ei oota konkreetset (mõõdetavat) tulemust. Sisestage kirjeldus, mida teha jaotisesse **Juhised** vahekaardil **Rea üksikasjad**. b. Päist kasutatakse pealkirjana selle all asuvate hoolduse kontrollnimekirjade ridade rühmitamiseks. See on kasulik, kui teil on mitu hoolduse kontrollnimekirja rida, mida saab jagada konkreetseteks tööaladeks. Sisestage kirjeldav nimi väljale **Nimi**.  
  c. Mall pole rakendatav, kui lisate hooldustööde kontrollnimekirja rea töökäsku käsitsi.  
  p Muutujat kasutatakse vahemiku võimaliku tulemuse määratlemiseks hoolduse kontrollnimekirja real. Hoolduse kontrollnimekirjade muutujate seadistamist kirjeldatakse jaotistes [hooldustööde tüüpide kategooriad ja hooldustööde tüübid, hooldustööde tüüpide variandid, hooldustööde vahetused ja hooldustööde kontrollnimekirjad](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Sisestage nimi, et kirjeldada muutujat väljal **Nimi**. Valige muutuja väljal **Muutuja**. Sisestage kirjeldus, mida teha jaotisesse **Juhised** vahekaardil **Rea üksikasjad**.  
  e. Mõõtmine – rida kasutatakse konkreetse mõõtmise registreerimiseks. Sisestage mõõtmise nimi väljale **Nimi**. Vahekaardil **Rea üksikasjad** valige **Loendur** ja **Üksikasjad**. Lisage jaotisesse **Juhised** kirjeldus, mida teha.  

5. Kui olete hoolduse kontrollnimekirja read käsitsi lisanud, täitke read ülaltoodud jaotises kirjeldatud viisil.

>[!NOTE]
>Loendis **Töökäsu hooldustöö kontrollnimekiri** ei saa kustutada hoolduse kontrollnimekirja ridu viitega "Töö tüüp". Kustutada saate ainult hoolduse kontrollnimekirja ridu, millel on viide „Käsitsi”, mille olete ise või on teised hooldustöötajad käsitsi loonud.


![Joonis 1](media/14-work-orders.png)

