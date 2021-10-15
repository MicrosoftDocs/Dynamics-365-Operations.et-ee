---
title: Mobiilse seadme menüüelemendi seadistamine ostutellimuse lõpetamiseks
description: Selles teemas näidatakse, kuidas seadistada mobiiliseadme menüü-üksust.
author: Mirzaab
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d18b0ab1057dbccdd45a52a58f80ef9346e4459f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565148"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Mobiilse seadme menüüelemendi seadistamine ostutellimuse lõpetamiseks

[!include [banner](../../includes/banner.md)]

Selles teemas näidatakse, kuidas seadistada mobiiliseadme menüü-üksust. Selles näites kasutatakse seda menüü-üksust ostutellimuse tüüpi töö tegemiseks. Menüü-üksusega seostatud töö klass määrab, milline töö on kehtiv. Saate seda juhendit kasutada demoettevõtte USMF andmetega. Tavaliselt viib selle protseduuri läbi laojuhataja.


## <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine
1. Avage  **Mobiiliseadme menüü-üksused**, sisestades selle otsinguribasse.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Menüü-üksuse nimi**. Sisestage kordumatu väärtus. Näiteks võite sisestada `POMove`. Jätke väärtus meelde, teil on seda hiljem vaja.  
4. Sisestage väärtus väljale **Pealkiri**. See on pealkiri, mis kuvatakse mobiilses seadmes. Näiteks võite sisestada `PO Move`.  
5. Valige väljal **Režiim** suvand **Töö**.
6. Valige väärtus **Jah** väljal **Kasuta olemasolevat tööd**.
    - Seda mobiilse seadme menüüelementi kasutatakse olemasoleva töö tegemiseks. Seega tuleb määrata selle väärtuseks **Jah**.  
    - Väli **Kuva varude olek** määrab, kas vaba kaubavaru olek kuvatakse laotöötajale mobiiliseadmel.  
7. Tehke väljal **Suunaja** valik **Süsteemi rühmitamine**. Kui valite midagi väljalt **Suunaja**, kuvatakse selle lehe jaotises **Üldine** lisaväljad. Kuvatavad väljad sõltuvad sellest, mida valisite. Kui teete valiku **Süsteemi rühmitamine**, lisatakse kaks uut välja. Neid selgitatakse allpool.  
8. Valige väljalt **Süsteemi rühmitamine** väärtus **WorkPoolId**. Kui laotöötajad selle menüü-üksuse avavad, palutakse neil töökausta ID skannida. Kõik selle töökausta ID-ga töötellimused ja ühe sellele menüü-üksusele lisatud tööklassiga avatud töötellimuse read suunatakse kasutajale.  
9. Sisestage väärtus väljale **Süsteemi rühmitussilt**. See tekst kuvatakse mobiilsel seadmel kasutajale. Näiteks võite sisestada valiku **Töökaust**.  
10. Valige **Jah** väljal **Tühista litsentsiplaat paneku käigus**. See valik võimaldab laotöötajatel alistada sihtlitsentsiplaadi, kui kaubad paigutatakse litsentsiplaadiga juhitavasse asukohta.  
11. Valige **Jah** väljal **Grupi kõrvalepanek**.
    - Kui kõik asetamise read töötellimusel on sama asukohaga, saab kasutaja kõigi ridade kohta ühe kombineeritud asetamise juhise. 
    - Auditimalli ID: töö auditimall võimaldab määratleda, et menüü-üksuse tööprotsess tuleks teise toimingu tegemiseks katkestada. Kui näiteks menüüelement käib sissetuleva töö kohta, võib auditimall nõuda, et töötaja kontrolliks temperatuuri. Hetk, millal protsess katkestatakse, tuleb määrata auditi mallis, ja see võib olla näiteks siis, kui tööd alustatakse või lõpetatakse või kui selle olek muutub.  
12. Laiendage jaotist **Tööklassid**.
13. Valige suvand **Uus**.
14. Sisestage väljale **Tööklassi ID** sõna `Purchase`. Töökaust piirab tööd, mille jaoks seda menüüelementi võib kasutada. Praegusel juhul kasutatakse seda avatud töötellimuse ridade jaoks, millel on ostutöö klassi ID.  
15. Valige käsk **Salvesta**.

## <a name="set-up-work-confirmation"></a>Töö kinnituse häälestamine
1. Valige **Töö kinnituse häälestus**.
2. Tehke väljal **Töö tüüp** valik **Komplekteeri**.
3. Märkige ruut **Automaatkinnitus.** Tööjuhis töö tüübiga Komplekteeri kinnitatakse automaatselt. Seda juhist ei kuvata kasutajale.  
4. Valige suvand **Uus**.
5. Valige väljal **Töö tüüp** suvand Pane.
6. Märkige ruut **Asukoha kinnitus**. Laotöötajal palutakse teha asukohast kinnitusskann, kui kaup on paigutatud.  
7. Valige käsk **Salvesta**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Menüü-üksuse lisamine mobiilse seadme menüüsse
1. Avage menüü  **Mobiiliseade**, sisestades selle otsinguribasse.
2. Valige suvand **Redigeeri**.
3. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtreerida välja **Nimi** väärtuse „**sissetulev**” järgi. Soovite leida menüüd, mida kasutate sissetulevate menüü-üksuste puhul. USMF-is on selle nimetus **Sissetulev**.  
4. Valige puul **väärtus**.
5. Klõpsake paremale suunatud noolt.
6. Valige käsk **Salvesta**.
7. Sulgege leht.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]