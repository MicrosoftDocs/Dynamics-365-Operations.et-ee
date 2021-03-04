---
title: Eelistatud hooldustöötajate seadistus
description: Selles teemas selgitatakse, kuidas sätestada eelistatud hooldustöötajaid varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426207"
---
# <a name="set-up-preferred-maintenance-workers"></a>Eelistatud hooldustöötajate seadistus

[!include [banner](../../includes/banner.md)]

 

Saate töötellimuse planeerimisel eelistada, milline hooldustööline või tööliste rühm on määratud töötellimuste läbiviimiseks. Selle funktsiooni kasutamine on valikuline, kuid see aitab teil töö läbiviimiseks valida kõige kvalifitseerituma hooldustöötaja tema oskuste ja pädevuste alusel. Planeeritakse ainult hooldustöötajaid, kes on saadaval planeerimise ajal. Kui eelistatud hooldustöötaja häälestus ühtib planeerimisel töötellimusega, kuid hooldustöötaja on määratud teistele töödele, planeeritakse töötellimus teisele, saadaolevale hooldustöötajale.

Enne eelistatud hooldustöötajate seadistamist peate esmalt seadistama hooldustöötajad ja töötajate rühmad. Hooldustöötajate ja töötajate rühmade sätestamise kirjeldust vaadake teemast [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Eelistatud hooldustöötajate sätestamine

Eelistatud hooldustöötaja või töötajate rühm võib olla seotud ühe või mitmega järgmistest.

- kaubandus  
- Hooldustöö  tüübi variant  
- Hooldustöö tüüp  
- Hooldustöö tüübi kategooria  
- vara  
- Vara tüüp  

Mida rohkem valikuid te sama kirje jaoks teete, seda täpsem on teie seadistus.

1. Klõpsake **Varahaldus** > **Seadistus** > **Töötajad** > **Eelistatud hooldustöötajad**.

2. Klõpsake uue kirje loomiseks suvandit **Uus**.

3. Alustage "vaikimisi" hooldustöötaja või töötajate rühma loomisega. See tähendab, et teete ainult valiku **Eelistatud hooldustöötajate grupi** väljal või **Eelistatud hooldustöötaja** väljal. Alltoodud kuvatõmmisel näete näidet esimesest kirjest, milles on "Taotlused" on valitud rühmaks **Eelistatud hooldustöötajate rühm**.

    [!NOTE] Vaikimisi häälestust kasutatakse töökäsu planeerimisel, kui teine spetsiifilisem kombinatsioon ei vasta töökäsu sisule.

4. Uue kirje loomiseks korrake 2. etappi. Tehke nõutavad valikud sõltuvalt eelistatud töötaja või töötajate grupi üksikasjalikust tasemest. 

    *Näide:* alltoodud kuvatõmmisel on kuuendas kirjes hooldustöötaja Shawn Richardson valitud eelistatud töötajaks. Ta valitakse automaatselt töötellimuse planeerimisel, mis sisaldab vara "CH-BP1-03-02 ja hooldustöö tüüp "Oskuste hindamine", kui ta on planeeritud ajal saadaval.

    [!NOTE] Üldiselt, kui töötellimuse planeerimisel valitakse eelistatud hooldustöötaja, läbib Varahaldus kõik **eelistatud hooldustöötajate** kirjed, et kontrollida võimalikku vastet, kontrollides alati kõige spetsiifilisemat kombinatsiooni esimesena. Kui vastet ei leita, kasutatakse "vaikimisi" kirjet, mille valikuks on kas **Eelistatud hooldustöötajate grupi** väli või **Eelistatud hooldustöötaja** väli.

![Joonis 1](media/02-work-order-scheduling.png)

Saate seadistada ka *vastutavad* hooldustöötajad, keda saab valida hoolduse taotluse või töökäsu loomisel. **Kõigi töökäskude** ja **Kõigi hooldusnõuete** korral saate valikut vajadusel redigeerida. Lisateabe saamiseks vaadake [Vastutavad hooldustöötajad](../setup-for-maintenance-requests/responsible-workers.md).

Töötellimuse planeerimisel arvutatakse erinevad punktisummad, et määrata, millised töötajad peaksid läbi viima töötellimusega seotud tööd (need punktisummad seadistatakse **Varahalduse parameetrite** > **Töötellimuse planeerimise** lingil). Kui kaks või rohkem eelistatud hooldustöötajat või vastutavat hooldustöötajat saavad töötellimuse planeerimisel sama punktisumma, valitakse juhuslikult üks töötaja. Vastasel juhul on alati kõige kõrgema punktisummaga töötaja see, kes määratakse töötellimuse läbiviimiseks.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]