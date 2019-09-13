---
title: Eelistatud hooldustöötajate seadistus
description: Selles teemas selgitatakse, kuidas sätestada eelistatud hooldustöötajaid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887407"
---
# <a name="preferred-maintenance-workers"></a>Eelistatud hooldustöötajad

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Saate töötellimuse planeerimisel eelistada, millised hooldustöölised on määratud töötellimuste läbiviimiseks. Selle funktsiooni kasutamine on valikuline, kuid see aitab teil töö läbiviimiseks valida kõige kvalifitseerituma hooldustöötaja tema oskuste ja pädevuste alusel. Seetõttu kasutatakse töötellimuse planeerimisel **eelistatud hooldustöötaja** seadistust, et määrata, kas kindel hooldustöötaja või töötajate grupp tuleks töötellimuse jaoks planeerida. Planeeritakse ainult hooldustöötajaid, kes on saadaval planeerimise ajal. Kui eelistatud hooldustöötaja häälestus ühtib planeerimisel töötellimusega, kuid hooldustöötaja on määratud teistele töödele, planeeritakse töötellimus teisele, saadaolevale hooldustöötajale.

Enne kui saate sätestada eelistatud hooldustöötajaid, peate esiteks sätestama hooldustöötajad ja töötajate rühmad, mis peaksid valikuks saadaval olema. Hooldustöötajate ja töötajate gruppide sätestamise kirjeldust vaadake teemast [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Eelistatud hooldustöötajate sätestamine

Eelistatud hooldustöötaja või töötajate grupp võib olla seotud konkreetse

- kaubandus  
- Hooldustöö  tüübi variant  
- Hooldustöö tüüp  
- Hooldustöö tüübi kategooria  
- vara  
- Vara tüüp  

Või nende valikute kombinatsioon. Mida rohkem valikuid te sama kirje jaoks teete, seda täpsem on teie seadistus.

1. Klõpsake **Varahaldus** > **Seadistus** > **Töötajad** > **Eelistatud hooldustöötajad**.

2. Klõpsake uue kirje loomiseks suvandit **Uus**.

3. Alustage, luues "vaikimisi" hooldustöötaja või töötajate grupi seadistuse, millel puuduvad valikud ülaltoodud täpploendi väljadel. See tähendab, et teete ainult valiku **Eelistatud hooldustöötajate grupi** väljal või **Eelistatud hooldustöötaja** väljal. Alltoodud joonisel näete näidet esimesest kirjest, milles on valitud eelistatud hooldustöötajate grupiks "Taotlused".

>[!NOTE]
>Vaikimisi häälestust kasutatakse töökäsu planeerimisel siis, kui teine spetsiifilisem kombinatsioon ei vasta töökäsu planeerimisel töökäsu sisule.

4. Uue kirje loomiseks korrake 2. etappi. Tehke nõutavad valikud sõltuvalt eelistatud töötaja või töötajate grupi üksikasjalikust tasemest. *Näide:* alltoodud joonisel on kuuendas kirjes hooldustöötaja Shawn Richardson valitud eelistatud töötajaks. Ta valitakse automaatselt töötellimuse planeerimisel, mis sisaldab vara "CH-BP1-03-02 ja hooldustöö tüüp "Oskuste hindamine", kui ta on planeeritud ajal saadaval.

>[!NOTE]
>Üldiselt, kui töötellimuse planeerimisel valitakse eelistatud hooldustöötaja, läbib Varahaldus kõik **eelistatud hooldustöötajate** kirjed, et kontrollida võimalikku vastet, kontrollides alati kõige spetsiifilisemat kombinatsiooni esimesena. Kui vastet ei leita, kasutatakse "vaikimisi" kirjet, mille valikuks on kas **Eelistatud hooldustöötajate grupi** väli või **Eelistatud hooldustöötaja** väli.


![Joonis 1](media/02-work-order-scheduling.png)

Saate seadistada ka vastutavad hooldustöötajad, keda saab valida hoolduse taotluse või töötellimuse loomisel. **Kõigi töötellimuste** ja **Kõigi hooldusnõuete** korral saate valikut vajadusel redigeerida. Lisateabe saamiseks vaadake [Vastutavad hooldustöötajad](../setup-for-maintenance-requests/responsible-workers.md).

Töötellimuse planeerimisel arvutatakse erinevad punktisummad, et määrata, millised töötajad peaksid läbi viima töötellimusega seotud tööd (need punktisummad seadistatakse **Varahalduse parameetrite** > **Töötellimuse planeerimise** lingil). Kui kaks või rohkem eelistatud hooldustöötajat või vastutavat hooldustöötajat saavad töötellimuse planeerimisel sama punktisumma, valitakse juhuslikult üks töötaja. Vastasel juhul on alati kõige kõrgema punktisummaga töötaja see, kes määratakse töötellimuse läbiviimiseks.

