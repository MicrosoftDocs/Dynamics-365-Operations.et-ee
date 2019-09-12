---
title: Käsitsi loodud töökäsud
description: Selles teemas tutvustatakse, kuidas luua varahalduses käsitsi töökäske.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875608"
---
# <a name="manually-created-work-orders"></a>Käsitsi loodud töökäsud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Töökäskude käsitsi loomiseks on kaks võimalust:

- jaotistes **Kõik töökäsud** või **Aktiivsed töökäsud**  
- jaotises **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded** või **Minu töö asukoha hooldusnõuded**  

## <a name="create-work-order"></a>Töökäsu loomine

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Klõpsake nuppu **Uus**.

3. Valige ripploendist **Töökäsu loomine** töökäsu tüüp.

4. Vajadusel valige kirjeldus.

5. Valige töökäsule vara ja ka hooldustöö tüüp.

>[!NOTE]
>Kuil valite vara, võib saadaval olla kolm vahekaarti. Vahekaart **Minu varad** sisaldab töö asukohtaga seotud varasid, millele teie (süsteemi sisseloginud töötaja) võite olla määratud (seadistatud jaotises [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md)). Kui töötajale ei ole jaotises [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md) töö asukohti seadistatud, siis vahekaarti **Minu varad** ei kuvata. Vahekaart **Aktiivsed varad** sisaldab kõigi varade loendit, mille vara töötsükli olek on „Aktiivne”. Vahekaardil **Varade vaade** kuvatakse töö asukohtade puuvaade ja nendesse asukohtadesse paigaldatud varad.

6. Vajadusel valige **Hooldustöö  tüübi variant** ja **Vaheta**.

7. Vajadusel saate väljal **Teenindustase** töökäsu teenindustaset muuta.

8. Valige vastavatele väljadele oodatavad algus- ja lõppkuupäevad.

9. Uue töökäsu loomiseks klõpsake **OK**.

10. Vajadusel redigeerige töökäsku jaotises **Kõik töökäsud**.

- Jaotises **Kõik töökäsud** saate töökäsule üksikasjade vaates lisada mitmeid varasid, lisades ridu kiirkaardile **Töökäsu hooldustööd**. Vara juures saate valida ainult neid hooldustööde tüüpe, mis on määratletud varale valitud vara tüübi juures.  
- Kui olete muutnud vara teenindustaset või vara pärast nende töökäsu juures kasutamist kriitiliselt (vt [Vara teenindustasemed](../setup-for-objects/object-priorities.md) ja [Vara kriitilisused](../setup-for-objects/object-criticalities.md)), ei värskendata vastavalt teenindustaset ega töökäsu kriitilisust.
- Töökäsu kriitilisust arvutatakse uuesti iga kord, kui töökäsule lisatakse või sealt kustutatakse töökäsu rida.
- Jaotise **Kõik töökäsud** üksikasjade vaates > vaates **Päis** > kiirkaardil **Ajakava** saate valida vastutava hooldustöötajate rühma või vastutava hooldustöötaja väljadel **Vastutav rühm** või **Vastutav**. Neid sätteid saab muuta seni, kuni töökäsk on aktiivne, näiteks siis kui töökäsu töötsükli olek muutub. Töökäsu loomisel tehtud automaatne valik põhineb jaotise **Vastutavad hooldustöötajad** seadistusel. Kui lisate või eemaldate töökäsu töid pärast töökäsu loomist ja väljad **Vastutav rühm** ja **Vastutav** on töökäsu värskendamise ajal tühjad, otsib varahaldus seadistuse vormil võimalikku vastet vastutavale hooldustöötajate rühmale või vastutavale hooldustöötajale. Kui väli **Vastutav rühm** või väli **Vastutav** on töökäsu värskendamisel juba täidetud, siis muudatusi ei tehta. 

- Jaotises **Hoolduse olek** saate teha arvutusi, et saada ülevaade sissetulevate ja lõpetatud töökäskude töökoormusest.  

- Kasutage kiirkaardil **Rea üksikasjad** välju **Laiuskraad** ja **Pikkuskraad**, et lisada töökäsu tööl valitud varale geograafilised koordinaadid.  

## <a name="create-related-work-order"></a>Loo seotud töökäsk

Võite luua seotud töökäsu olemasolevale töökäsule, kui näiteks soovite töötada peamise ja sekundaarsete töökäskudega. Uus töökäsk põhineb olemasolevast töökäsust pärit töökäsu tööl.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk, millele soovite teha seotud töökäsku.

3. Klõpsake suvandil **Seotud töökäsk**.

4. Valige rippdialoogis **Loo seotud töökäsk** see töökäsu töö väljal **Töökäsu töö**, millele soovite seotud töökäsku luua.

5. Valige hooldustöö tüüp väljal **Hooldustöö tüüp** ja vajadusel seotud hooldustöö  tüübi variant ning vahetage väljadel **Hooldustöö  tüübi variant** ja **Vaheta**.

6. Kui see on esimene seotud töökäsk, mille teete, klõpsake raadionuppu **Uus töökäsk**.

7. Valige vastavatel väljadel **Töökäsu tüüp** ja **Kirjeldus**.

8. Vajadusel muutke väljal **Teenindustase** töökäsu teenindustaset.

9. Sisestage vastavatele väljadele oodatavad algus- ja lõppkuupäevad.

10. Klõpsake valikut **OK**. Uut seotud töökäsku kuvatakse loendis **Kõik töökäsud**.

11. Kui loote seotud töökäsu töökäsule, millel juba on seotud töökäske, võite lisada töökäsu töö juba soetud töökäsule. Selleks klõpsake etapis 6 raadionuppu **Lisa seotud töökäsk**. Seejärel valite seotud töökäsu, millele soovite lisada uut töökäsu tööd. Redigeerige vajadusel välju **Teenindustase**, **Oodatav algus** ja **Oodatav lõpp** ning klõpsake **OK**. Töökäsu töö lisatakse olemasolevale seotud töökäsule.


![Joonis 1](media/03-work-orders.png)

**Märkus:** kui olete seadistanud seotud töökäsu maski jaotise **Varahalduse parameetrid** > **Töökäsud** lingi > väljal **Seotud töökäsu mask**, luuakse töökäsu ID-d vastavalt maski seadistusele. Kui seotud töökäsu maski ei ole seadistatud, kasutatakse seotud töökäskudele järgmist saadaolevat töökäsu ID-d.

## <a name="copy-work-order"></a>Töökäsu kopeerimine

Võimalik on luua olemasolevast töökäsust kiiresti uus töökäsk. Selline töökäskudega töötamine erineb hoolduskavade põhjal töökäskude loomisest. See on kasulik näiteks siis, kui teil on töökäsk, mis sisaldab palju töökäsu töid mitmete erinevate varade töödega, mis tuleksid teostada regulaarsete intervallidega.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk, mille sisu soovite kopeerida.

3. Klõpsake suvandil **Kopeeri töökäsk**. Kuvatakse valitud töökäsu seadistust valitud töökäsust. Vajadusel saate mõnda nendest väljadest redigeerida.

4. Uue töökäsu loomiseks klõpsake **OK**.

5. Vajadusel redigeerige töökäsku jaotises **Kõik töökäsud**.

>[!NOTE]
>Kui töökäsk on loodud, kopeeritakse osad andmed otse olemasolevast töökäsust. Prognooside, tööriistade, hoolduse kontrollnimekirjade, töö asukohtade, aadresside ja ajastamise infot ei kopeerita, vaid lähtestatakse kehtivast varahalduse seadistusest. See tähendab, et kui ajavahemikult esimese töökäsu loomisest kuni töökäsu koopia tegemiseni tehti aeg-ajalt nendes andmetes muudatusi, sisalduvad need muudatused uues loodud töökäsus. Näited prognoosi muudatustest või värskendatud hoolduse kontrollnimekirjast.


![Joonis 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Töökäsu loomine hooldusnõude põhjal

1. Klõpsake **Varahaldus** > **Üldine** > **Hooldusnõuded** > **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded**.

2. Valige hooldusnõuded, millele soovite luua töökäsu, ning klõpsake **Redigeeri**.

3. Klõpsake jaotises **Kõik nõuded** valikut **Töökäsk**.

4. Täitke ripploend **Töökäsk**. Kui hooldusnõudes on valitud hooldustöö tüüp, saate valida vajadusel teise hooldustöö tüübi, kui loote töökäsu.

5. Klõpsake valikut **OK**. Näete teadet, mis teavitab teid, et töökäsk on loodud.

6. Kui soovite näha millised töökäsud on hooldusnõudega ühendatud, valige hooldusnõue loendist **Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused** ning klõpsake nupul **Töökäsud**.


![Joonis 3](media/05-work-orders.png)


>[!NOTE]
>Töökäske saab ka automaatselt luua ajastades hoolduskava töid või seadistades varale "Automaatselt loodavaid" hoolduskavasid või hoolduskordi. Hooldusnõuetest loodud töökäsud jaotises **Hooldusgraafik** luuakse nii, et hooldusnõuetest on valitud hooldustöö tüübid.

