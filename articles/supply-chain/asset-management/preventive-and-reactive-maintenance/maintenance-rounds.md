---
title: Hoolduskorrad
description: Selles teemas selgitatakse hoolduskordi varahalduses.
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
ms.openlocfilehash: a0ac4820d2efa37387382c2890e3ddc7dbc0878b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875606"
---
# <a name="maintenance-rounds"></a>Hoolduskorrad


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


**Varahalduses** saate luua hoolduskordi erinevatele varadele, mille juures on vaja teostada regulaarsete intervallidega sarnaseid ülesandeid. Näiteks määrimistööd või ohutuskontrollid, mida tuleb teostada sama intervalliga mitmel masinal. Esimene etapp on luua hoolduskord koos varadega, mis vajavad samas vormis hooldustööd. Järgmisena ajastate hoolduskorrad. Kui olete hoolduskordade ajastamise lõpetanud, näete kõiki hoolduskorraga seotud töö kirjeid jaotistes **Kõik hooldusgraafikud** ja **Avatud hooldusgraafiku read**.

>[!NOTE]
>Hoolduskordi saab seadistada ka töö asukohtadele, kus need tuleb teostada töö asukohta hoolduskorrapõhise töökäsu loomise hetkel paigaldatud varadele. Lisainfo saamiseks hooldusraundide seadistamiseks töö asukohtadele vt [Töö asukohtade loomine](../functional-locations/create-functional-locations.md).

## <a name="set-up-a-maintenance-round"></a>Hoolduskorra seadistamine

1. Klõpsake suvandil **Varahaldus** > **Seadistus** > **Ennetav hooldus** > **Hoolduskorrad**.

2. Uue hoolduskorra loomiseks klõpsake valikut **Uus**.

3. Sisestage ID väljale **Hoolduskord** ja hoolduskorra nimi väljale **Nimi**.

4. Valige hoolduskorra jaoks alguskuupäev väljal **Alguskuupäev**.

5. Väljadele **Päevi lõpetamiseks** ja **Tunde lõpetamiseks** võite sisestada oodatava lõppkuupäeva päevade ja tundidena. Oodatav lõppkuupäev arvutatakse vastavalt alguskuupäevale, mis arvutatakse välja hoolduskava ridade loomisel. Näiteks võite sisestada väljale **Päevi lõpetamiseks** numbri "7" näitamaks, et seotud töö tuleks lõpetada nädala jooksul alates alguskuupäevast.

6. Valige tumblernupule **Automaatloomine** väärus "Jah", kui töökäsud tuleks sellest hoolduskorrast loodud hoolduskava ridadest automaatselt luua.

7. Valige väljal **Töökäsu tüüp** sellest hoolduskorrast loodud töökäskudele töökäsu tüüp.

8. Valige väljal **Teenindustase** sellest hoolduskorrast loodud töökäskudele töökäsu teenindustase.

9. Klõpsake kiirkaardi **Vara read** jaotisel **Lisa**, et lisada hoolduskorrale vara.

10. Reanumber sisestatakse väljale **Reanumber** automaatselt, et näidata hoolduskorra varade järjestust.

11. Valige vara väljal **Vara**.

12. Valige väljal **Hooldustöö tüüp** varale hooldustöö tüüp.

13. Valige vajadusel hooldustöö tüübiga seotud **Hooldustöö  tüübi variant** ja **Vaheta**.

14. Valige väljal **Perioodi tüüp** korduvus (päev, nädal, jne).

15. Väljale **Perioodi sagedus** sisestage hoolduskorra korduste arv. Näide: Kui olete valinud väljale **Perioodi tüüp** valiku "Päev" ja sisestate sellele väljale arvu "7", luuakse ennetava hoolduse ajastamisel kord nädalas uued hoolduskorra read.

16. Valige väljal **Alguskuupäev** hoolduskorras sisalduvale varale alguskuupäev. See kuupäev võib hoolduskorrale seadistatud alguskuupäevast erineda.

17. Kui soovite hoolduskorrale veel varasid lisada, korrake etappe 9-16.

18. Klõpsake kiirkaardil **Töö asukoha read** hoolduskorrale töö asukohta lisamiseks valikut **Lisa**. Vaadake eespoolt seotud väljade kirjeldust. Saadaval on samad väljad, mis ka vara rea loomisel, aga saate vajadusel töö asukohale valida ka **Tootja** ja **Mudeli**. Kui valite reale ainult töö asukoha aga ei tee valikuid **Vara tüüp**, **Tootja**, **Mudel**, **Hooldustöö tüüp**, **Hooldustöö  tüübi variant** ja **Vahetus**, kaasatakse hoolduskorda kõik selle töö asukohaga hoolduse ajastamise hetkel seotud töö asukohad.

19. Klõpsake kiirkaardil **Kogumid** hoolduskorda kaasatava töökäsu kogumi valimiseks suvandit **Lisa**. Ühe hoolduskorraga saab ühendada mitu töökäsu kogumit.

20. Salvestage oma seadistus.

>[!NOTE]
>Väljad **Varad** ja **Read**, mis asuvad rühmas **Üksikasjad** kiirkaardil **Päis** näitavad valitud hoolduskorraga seotud varade ja ridade koguarvu.

![Joonis 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Hoolduskordade plaanimine

Kui olete hoolduskorra seadistanud, käivitate ajastamise töö, et ajastada kõik hoolduskorraga seotud tööd.

1. Klõpsake **Varahaldus** > **Perioodiline** > **Ennetav hooldus** > **Hoolduskordade ajastamine** või **Varahaldus** > **Üldine** > **Hooldusgraafik** > **Kõik hooldusgraafikud** või **Ava hooldusgraafiku read** või **Ava hooldusgraafiku kogumid** > valige loendist hooldusgraafiku rida > nupp **Hoolduskorrad**.

2. Valige väljal **Periood** ajastamise tööks kasutatav perioodi tüüp.

3. Väljale **Perioodi sagedus** sisestage ajastamise töös sisalduv perioodide arv. Ajastamise alguseks on praegune kuupäev.

4. Valige tumblernupule **Automaatloomine** väärus "Jah", kui selle hoolduskorra põhjal tuleks automaatselt luua töökäsk.

>[!NOTE]
>Kui tumblernupp on seatud väärtusele "Jah" ja tumblernupp **Automaatloomine** on samuti vormi **Hoolduskorrad** hoolduskorral seatud väärtusele "Jah", luuakse töökäsud hoolduskorra ridade põhjal ja luuakse ka hooldusgraafiku read olekuga "Töökäsk loodud". Kui ainult üks tumblernuppudest **Automaatloomine** on seadistatud väärtusele "Jah" kas selles ripploendis või jaotises **Hoolduskorrad**, luuakse hooldusgraafiku read ainult olekuga "Loodud". Sellisel juhul töökäske ei looda.

5. Vajaduse korral saate ajastamise tööle valida konkreetsed hoolduskorrad või teise alguskuupäeva. Klõpsake suvandil **Filter** ja lisage hoolduskorrad.

6. Klõpsake valikut **OK**.

7. Nüüd saate hoolduskordade töid näha jaotises **Varahaldus** > **Üldine** > **Hooldusgraafik** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read**. Kui ajastatud hoolduskorrad on ühendatud töökäskude kogumiga, näete hooldusgraafiku ridu ka jaotises **Avatud hooldusgraafiku kogumid**. Hoolduskorrast loodud hooldusgraafiku ridadel on viitetüüp "Hoolduskorrad".

![Joonis 2](media/14-preventive-maintenance.png)

![Joonis 3](media/15-preventive-maintenance.png)

- Kui tarnija garantii alla käivatele varadele tehakse töökäsud käsitsi, kuvatakse dialoogikasti, et teavitada kasutajat garantiist. Siis saab töökäsu loomise tühistada. Automaatselt loodud töökäskudel on garantii seose kontrollimine välja jäetud.  
- Kiirkaardil **Taustal käitamine** saate seadistada pakett-töö regulaarsete intervallidega hoolduskordade ajastamiseks.  
- Kui hoolduskord sisaldub mitmes töökäsu kogumis (vt [Töökäskude kogumid](../work-orders/work-order-pools.md)), kuvatakse ühte kirjet igas jaotise **Avatud hooldusgraafiku kogumid** kogumis. Seda tehakse töökäsu kogumite filtreerimisvalikute optimeerimiseks.

