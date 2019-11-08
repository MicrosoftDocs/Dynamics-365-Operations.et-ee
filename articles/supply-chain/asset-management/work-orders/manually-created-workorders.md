---
title: Käsitsi loodud töökäsud
description: Selles teemas tutvustatakse, kuidas luua varahalduses käsitsi töökäske.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a8494bdefcf11dc331be18bfe02e0df1e39d602
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626243"
---
# <a name="manually-created-work-orders"></a>Käsitsi loodud töökäsud

[!include [banner](../../includes/banner.md)]


Töökäskude käsitsi loomiseks on kaks võimalust:

- Lehel **Kõik töökäsud** või **Aktiivsed töökäsud** 
- Lehel **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded** või **Minu töö asukoha hooldusnõuded** 

## <a name="create-work-order"></a>Töökäsu loomine

1. Valige **Varahaldus** > **Ühine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige suvand **Uus**.

3. Valige töökäsu tüüp dialoogi **Töökäsu loomine** väljal **Töökäsu tüüp**.

4. Vajadusel valige **Kirjeldus**.

5. Valige vara väljal **Vara**.

>[!NOTE]
>Kui valite vara, võivad rippmenüüs **Vara** saadaval olla kolm vahekaarti. 

- **Aktiivsed varad** – see vahekaart sisaldab kõigi varade loendit, mille vara töötsükli olek on „Aktiivne”. 
- **Varade vaade** – sellel vahekaardil kuvatakse töö asukohtade puuvaade ja neisse paigaldatud varad.
- **Minu varad** – see vahekaart sisaldab varasid, mis on seotud töö asukohtadega, mida teile (töötajale, kes on süsteemi sisse loginud) võidakse eraldada. (Lisateavet seadistuse kohta vt teemast [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md).) Kui töötajale pole töö asukohti seadistatud valikus [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md), pole vahekart **Minu varad** saadaval. 

6. Valige väljal **Hooldustöö tüüp** töökäsu jaoks hooldustöö töö tüüp.

7. Vajadusel valige **Hooldustöö  tüübi variant** ja **Vaheta**.

8. Vajadusel saate väljal **Teenindustase** töökäsu teenindustaset muuta.

9. Valige seotud väljadel **Eeldatud alguskuupäev** ja **Eeldatav lõppkuupäev**.

10. Töökäsu loomiseks klõpsake **OK**.

11. Loendilehel **Kõik töökäsud** saate vajadusel töökäsku redigeerida.

Pidage meeles järgmiseid punkte.

- Loendilehe **Kõik töökäsud** üksikasjalikus vaates saatetöökäsule lisada mitu vara, kui lisate read kiirkaardile **Töökäsu hooldustööd**. Vara juures saate valida ainult neid hooldustööde tüüpe, mis on määratletud varale valitud vara tüübi juures.  

- Kui muudate pärast töökäsu vara kasutamist vara teenusetaset või vara kriitilisust, ei värskendata selle töökäsu teenusetaset või kriitilisust vastavalt. Lisateavet teenusetasemete ja kriitilisuse kohta vt teemast [Vara teenusetasemed](../setup-for-objects/object-priorities.md) ja [Vara kriitilisus](../setup-for-objects/object-criticalities.md).

- Töökäsu kriitilisus arvutatakse ümber iga kord, kui töökäsu rida lisatakse või kustutatakse töökäsult.

- Üksikasjalik vaate **Kõik töökäsud** > vahekaardi **Päis** > kiirkaardi **Graafik** jaotises **Vastutav rühm** või väljal **Vastutav**, saate valida vastutava hooldustöötajate rühma või vastutava hooldustöötaja. Neid sätteid saab muuta, kui töökäsk on aktiivne. Näiteks saab neid muuta, kui töökäsu töötsükli olek muutub. Töökäsu loomisel tehtud automaatne valik põhineb lehe **Vastutavad hooldustöötajad** seadistusel. Kui lisate või eemaldate töökäsu töid pärast töökäsu loomist ja väljad **Vastutav rühm** ja **Vastutav** on töökäsu värskendamise ajal tühjad, proovib varahaldus otsida vastutava hooldustöötajate rühma või vastutavat töötaja võimalikku vastet seadistuse lehel. Kui väli **Vastutav rühm** või **Vastutav** on töökäsu värskendamisel juba seadistatud, siis muudatusi ei tehta. Lisateavet vastutavate hooldustöötajate ja töötajate rühma kohta vt teemast [Vastutavad hooldustöötajad](../setup-for-maintenance-requests/responsible-workers.md).

- Lehel [Hoolduse olek](../controlling-and-reporting/maintenance-status.md) saate teha arvutusi, et saada ülevaade sissetulevate ja lõpetatud töökäskude töökoormusest.  

- Lehe **Kõik töökäsud** üksikasjaliku vaate kiirkaardil **Rea üksikasjad** saate töökäsu töös valitud vara geograafiliste koordinaatide lisamiseks kasutada välju **Laiuskraad** ja **Pikkuskraad**.  


## <a name="create-related-work-order"></a>Loo seotud töökäsk

Saate luua töökäsu, mis on seotud olemasoleva töökäsuga. Funktsioon on kasulik näiteks esmaste ja teisejärguliste töökäskudega töötamise puhul. Uus töökäsk põhineb olemasolevast töökäsust pärit töökäsu tööl.

1. Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Looge töökäsk, millel luua seotud töökäsk.

3. Tehke tegumiriba vahekaardi **Töökäsk** jaotises **Uus** valik **Seotud töökäsk**.

4. Valige dialoogi **Seotud töökäsu loomine** väljal **Töökäsu töö** töökäsu töö, millele luua seotud töökäsk.

5. Väljal **Hooldustöö tüüp** valige hooldustöö tüüp.

6. Vajadusel valige seotud hooldustöö tüübi variant ja vahetus väljadel **Hooldustöö tüübi variant** ja **Vahetus**.

7. Kui see töökäsk on esimene seotud töökäsk, mis on valitud töökäsu jaoks loodud, toimige järgmiselt.
    1. Tehke valik **Uus töökäsk**.
    2. Valige töökäsu tüüpväljal **Töökäsu tüüp**.
    3. Sisestage kirjeldus väljale **Kirjeldus**.
    4. Vajadusel muutke töökäsu teenusetaset väljal **Teenusetase**.
    5. Valige algus-ja lõppkuupäevad väljal **Eeldatav algus** ja **Eeldatav lõpp** .
    6. Valige nupp **OK**. Uus seotud töökäsk kuvatakse loendilehel **Kõik töökäsud**.  

8. Kui töökäsul, millele loote seotud töökäsu, on seotud töökäsud juba olemas, järgige uue töökäsu töö lisamiseks olemasolevale seotud töökäsule järgmisi juhiseid.
    1. Valige **Lisa seotud töökäsule**.
    2. Valige väljal **Töökäsk** seotud töökäsk, millel lisada uus töökäsk.
    3. Vajadusel muutke töökäsu teenusetaset väljal **Teenusetase**.
    4. Vajadusel muutke eeldatavad algus- ja lõppkuupäevad väljadel **Eeldatav algus** ja **Eeldatav lõpp**.
    5. Valige nupp **OK**. Töökäsu töö lisatakse olemasolevale seotud töökäsule.

Alloleval joonisel kuvatakse dialoogi **Seotud töökäsu loomine** näide.

![Joonis 1](media/03-work-orders.png)

>[!NOTE]
>Kui olete seadistanud seotud töökäsu maski vahekaardi **Varahalduse parameetrid** > **Töökäsud** > väljal **Seotud töökäsu mask**, luuakse töökäsu ID-d vastavalt maski seadistusele. Kui seotud töökäsu maski ei ole seadistatud, kasutatakse seotud töökäskudele järgmist saadaolevat töökäsu ID-d.

## <a name="copy-a-work-order"></a>Töökäsu kopeerimine

Saate olemasolevast töökäsust kiiresti luua uue töökäsu. Sel viisil töökäskudega töötamine erineb töökäskude loomisest [hooldusgraafikute](../preventive-and-reactive-maintenance/maintenance-plans.md) põhjal. See on kasulik näiteks siis, kui töökäsk sisaldab mitut töökäsu tööd ja erinevate varade mitmed tööd tuleb lõpule viia regulaarsete intervallidega.

1. Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk, mille sisu soovite kopeerida.

3. Tehke tegumiribal > vahekaardi **Töökäsk** > jaotises **Uus** valik **Kopeeri töökäsk**.

4. Kuvatakse valitud töökäsu seadistust valitud töökäsust. Vajadusel saate mõnda nendest väljadest redigeerida.

5. Uue töökäsu loomiseks valige **OK**.

6. Loendilehel **Kõik töökäsud** saate vajadusel töökäsku redigeerida.

>[!NOTE]
>Kui töökäsk on loodud, kopeeritakse osad andmed otse olemasolevast töökäsust. Teavet prognooside, tööriistade, hoolduse kontrollnimekirjade, töö asukoha, aadresside ja ajastamise kohta ei kopeerita. Selle asemel lähtestatakse see varahalduse praegusest seadistusest. Seega, kui seda teavet muudeti esimese töökäsu loomise ja töökäsu koopia tegemise aja vahel, kaasatakse muudatused uude töökäsku. Näitena võib tuua prognooside muudatused ja hoolduse kontrollnimekirjade värskendused.

Alloleval joonisel kuvatakse dialoogi **Töökäsu kopeerimine** näide.

![Joonis 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Töökäsu loomine hooldusnõude põhjal

1. Valige **Varahaldus** > **Ühine** > **Hooldusnõuded** > **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded**.

2. Valige hooldusnõuded, millele soovite luua töökäsu, ning klõpsake **Redigeeri**.

3. Tehke tegumiriba > vahekaardi **Hooldusnõue** > jaotises **Uus** valik **Töökäsk**.

4. Seadistage väljad dialoogis **Töökäsk**. Kui hooldusnõudes on valitud hooldustöö tüüp, saate valida vajadusel teise hooldustöö tüübi, kui loote töökäsu.

5. Valige nupp **OK**. Teates teavitatakse teid töökäsu loomisest.

6. Et vaadata, millised töökäsud on hooldusnõudega ühendatud, valige hooldusnõue loendilehel **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded**. Seejärel tehke vahekaardi **Hooldusnõue** jaotise **Kuva** tegumiribal valik **Töökäsud**.


Allolevalt joonisel kuvatakse dialoogis **Töökäsu loomine** näide.

![Joonis 3](media/05-work-orders.png)


>[!NOTE]
>Kui soovite, et töökäsud loodaks automaatselt, saate vara hoolduskava töid ajastada või seadistada [hoolduskavade](../preventive-and-reactive-maintenance/maintenance-plans.md) või [hoolduskordade](../preventive-and-reactive-maintenance/maintenance-rounds.md) automaatse loomise. Hooldusnõuetest loodud töökäskudel on loendilehel **Kogu hooldusgraafik** hooldustööde tüübid, mis on hooldusnõuetes valitud.

