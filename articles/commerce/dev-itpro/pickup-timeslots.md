---
title: Kliendi järeletulemise ajavahemike loomine ja värskendamine
description: See teema kirjeldab kliendi järeletulemise ajavahemike loomist, konfigureerimist ja värskendamist Commerce Headquartersis.
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: a9ee1356bfcaeee881c28cf0361b34b2c65acbc7a3b57347fa2581a8a935da42
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713417"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Kliendi järeletulemise ajavahemike loomine ja värskendamine

[!include [banner](../../includes/banner.md)]

See teema kirjeldab kliendi järeletulemise ajavahemike loomist, konfigureerimist ja värskendamist Commerce Headquartersis.

Ajavahemiku funktsioon annab jaemüüjatele võimaluse määratleda ajavahemiku kaupadele, mille jaoks kliendi järeletulemisega tarneviis on sisse lülitatud. Ajavahemikud võimaldavad jaemüüjatel määratleda päevad ja kellaajad, kui tellimustele saab poodi järele tulla. Jaemüüjad saavad määratleda ka tellimuste arvu, millele saab kindla perioodi jooksul järele tulla. Sel viisil saavad jaemüüjad piirata selliste tellimuste arvu, millele saab kindlal päeval ja kindlal kellaajal järele tulla. Tulemuseks on kvaliteetsem klienditeenindus.

> [!NOTE]
> Ajavahemiku funktsioon on saadaval rakenduse Microsoft Dynamics 365 Commerce versioonis 10.0.15 ja uuemates versioonides.

Järgmisel joonisel on näidatud ajavahemiku valiku näide e-kaubanduse kassas.

![Ajavahemiku valiku näide e-commerce kassas.](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Ajavahemike atribuudid

Ajavahemik on konkreetne intervall, kus klient saab valida tellimusele kindlasse poodi või kohta järeletulemise. Ajavahemike halduse funktsioon on saadaval ainult siis, kui kliendi järeletulemisega tarneviis on konfigureeritud rakenduses Dynamics 365 Commerce.

Ajavahemik määratletakse järgmiste atribuutide abil.

- **Tarneviis** – määrake järeletulemisega tarneviis, millele ajavahemikku rakendatakse.
- **Minimaalne kuupäev** ja **Maksimaalne kuupäev** – määrake varaseim ja hiliseim kuupäev, mida saab tellimuse esitamise kuupäeva suhtes järeleletulemiseks valida. 

    Atribuut **Minimaalne kuupäev** tagab, et jaemüüjal on piisavalt aega tellimuse töötlemiseks, enne kui see on järeletulemiseks valmis. Atribuut **Maksimaalne kuupäev** tagab, et kasutaja ei saa valida kuupäeva, mis on liiga kauges tulevikus. Näiteks, kui minimaalseks väärtuseks määratakse **1** ja tellimus esitati 20. septembril, on tellimusele võimalik järele tulla kõige varem järmisel sobival päeval (21. septembril). Sarnaselt saate maksimaalse väärtuse määramisega määratleda maksimaalse päevade arvu, mille jooksul tellimusele järele tulla saab. Kui miinimum- ja maksimumväärtus on määratletud, saavad saidi kasutajad kassat kasutades kuvada ja valida vaid kindla hulga päevi.

    Saate määrata minimaalse väärtuse kümnendkoha väärtusele, mis on väiksem kui 1. Näiteks kui järeletulemine on saadaval neli tundi pärast tellimuse esitamist, määrake minimaalseks väärtuseks **0,17** (= 4 ÷ 24, ümardatuna kahe kümnendkohani). Kuid kui määrate minimaalse väärtuse kümnendkoha väärtusele, mis on suurem kui 1, ümardatakse see alati üles lähima täisarvuni. Näiteks väärtus **1,2** ümardatakse väärtuseni **2**. Samamoodi, kui määrate maksimaalse väärtuse kümnendkoha väärtusele, ümardatakse see alati üles lähima täisarvuni. 

- **Alguskuupäev** ja **Lõppkuupäev** – määrake ajavahemiku algus- ja lõppkuupäev. Igal ajavahemiku kirjel on alguskuupäev ja lõppkuupäev. Seega saate aasta jooksul lisada erinevaid ajavahemikke (näiteks järeletulemine puhkuse ajal). Kui ajavahemiku algust ja kuupäevi muudetakse pärast tellimuse esitamist, ei rakendata selle tellimuse puhul muudatusi. Kui määrate algus- ja lõppkuupäevad, tuleb arvestada kaupluse sulgemise kuupäevadega (nt jõulupühaga) ja tagada, et ajavahemikke nende päevade jaoks ei määrata.
- **Aktiivne järeletulemisaeg** – määrake periood, kus järeletulemine on lubatud. Näiteks võib järeletulemise aeg olla iga päev kella 14.00 ja 17.00 vahel. See atribuut võimaldab järeletulemise aja poe lahtiolekuajaks sõltumatuks teha. Seetõttu saab jaemüüja konfigureerida järeletulemise ajad, mis vastavad kindla ettevõtte vajadustele. Kui määrate aktiivse järeletulemisaja, tuleb arvestada poe lahtiolekuajaga ja tagada, et järeletulemine ei ole määratud ajale, kui pood on suletud.

    > [!NOTE]
    > Poodi järeletulemise ajad tuleb määratleda vastava poe ajavööndis.

- **Ajavahemiku intervall** – määrake igale ajavahemikule antav kestus. Näiteks võib iga ajavahemiku kestus olla 15 minutit, 30 minutit või üks tund. Kui ajavahemiku väärtus on 0, on ajavahemik saadaval kogu kestuse jooksul algusajast kuni lõpuajani.
- **Vahemikud intervalli kohta** – määrake klientide või tellimuste arv, keda või mida saab iga ajavahemiku intervalli jooksul järeletulemisega teenindada. Näiteks sisestage **1**, **2**, **3** või mõni muu täisarv.
- **Aktiivsed päevad** – määrake nädalapäevad, kui järeletulemise ajavahemikud on aktiivsed. See atribuut võimaldab jaemüüjal määratleda päevad, mil ta soovib järeletulemisega tellimusi toetada.
- **jaemüügikanalid** – saate määrata jaemüügikanalid. Iga ajavahemikku saab seostada ühe või mitme jaekauplusega. Sõltuvalt iga poe lahtiolekuajast saab luua ja kanaliga seostada vähemalt ühe ajavahemikukande. 

<!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Kanali kohta saab konfigureerida ainult ühe ajavahemiku malli. Need kanalid hõlmavad tellis-ja mördi kauplusi, kõnekeskusi, mobiiliseadmeid ja e-kaubanduse saite.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Ajavahemiku funktsiooni konfigureerimine Commerce'i peakontoris

Ajavahemikud tuleb määratleda iga järeletulemisega tarneviisi puhul Commerce'i peakontoris, nii et kassa ja e-kaubanduse kanalid saaksid neile viidata.

- Iga poe või kanaliga saab seostada ainult ühe ajavahemiku malli.
- Iga loodud ajavahemik peab igas mallis iga tarneviisi puhul olema kordumatu.
- Pärast ajavahemiku funktsiooni konfigureerimist on ajavahemiku kalender saadaval valitud poodide või poegruppide jaoks. Lisaks kuvatakse see teabe näitamiseks kassas.

Ajavahemiku funktsiooni konfigureerimiseks Commerce'i peakontoris tehke järgmist.

1. Valige **Kaubandus** \> **Kanali häälestus** \> **Poodi järeletulemise ajavahemik**.
1. Valige uue ajavahemiku malli loomiseks nupp **Uus**. Olemasoleva malli kasutamiseks valige vasakul paneelil mall.
1. Sisestage väärtused väljadesse **Ajavahemiku ID** ja **Kirjeldus**.
1. Valige kiirkaardil **Tellimusele järeletulemine – kellaaja sätted** nupp **Lisa**.
1. Määrake dialoogiboksis **Tellimusele järeletulemine – kellaaja sätted** kuupäevavahemik, tarneviis, aktiivne järeletulemisaeg, aktiivsed päevad, ajavahemikku intervall, ajavahemikud intervalli kohta ja muud sätted.

    Kui ajavahemikud on prognoosi kohaselt muutumatud, seadistage väli **Lõpukuupäev** väärtusele **Mitte kunagi**.

    > [!NOTE]
    > Saate luua mitu malli, kuid ühe kanali või poega saab seostada ainult ühe malli.

    ![Tellimusele järeletulemine - kellaaja sätete dialoogiboks.](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Kui olete lõpetanud, valige **OK**.
1. Kui ajavahemikud päeva jooksul varieeruvad, looge kiirkaardil **Tellimusele järeletulemine – kellaaja sätted** veel kirjeid, et kuupäevad ja kellaajad ei kattuks.
1. Valige kiirkaardil **jaemüügikanalid** nupp **Lisa**, et seostada ajavahemiku mall nende poodide või kanalitega, kus seda kasutatakse.
1. Kasutage dialoogiboksis **Organisatsiooni sõlmede valimine** poodide, regioonide ja organisatsioonide, millega mall peaks seotud olema, valimiseks (või valiku tühistamiseks) noolenuppe.

    <!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Kui olete lõpetanud, valige **OK**.
1. Käivitage lehel **Jaotusgraafik** tööd **1070** ja **1135**, et sünkroonida andmed kanalitega.

## <a name="time-slot-selection-for-pos-orders"></a>Kassatellimuste ajavahemike valimine

Kui kassas määratakse kindlaks järeletulemisega tellimuse rida, saab kassapidaja valida järeletulemiseks po või asukoha ning kuupäeva ja kellaaja ajavahemiku. Kui kliendil on teise kaupluse tellimus, saab kassapidaja valida kuupäevad, millal üleskorje on selles poes saadaval. Kaupluse otsing annab viite kuupäevadele ja kaupluse lahtiolekuaegadele.

Järgmisel joonisel on näidatud ajavahemiku valiku näide kassatellimuses.

![Ajavahemiku valiku näide kassatellimuse jaoks.](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>E-kaubanduse ajavahemike valimine

Lisateavet selle kohta, kuidas valida e-kaubanduse tellimuste jaoks ajavahemikku, leiate teemast [Järeletulemisteabe moodul](../pickup-info-module.md).

> [!NOTE]
> Kasutajad saavad vaadata või redigeerida järeletulemise ajavahemikke Commerce'i saidi maksmise lehel ainult juhul, kui järeletulemisteabe moodul on lisatud sellele lehele. Kui maksmise lehel järeletulemisteavet pole, esitatakse tellimused, lubamata kasutajatel ajavahemiku teavet määrata või vaadata.

Järgmisel joonisel on kujutatud e-kaubanduse tellimuse näide, kus järeletulemise ajavahemik on valitud.

![Näide e-commerce tellimusest, kus järeletulemise ajavahemik on valitud.](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Kõnekeskuse tellimustele ajavahemiku valimine

Kõnekeskuse rakenduses saavad kõnekeskuse agendid valida järeletulemise poe või asukoha ning ka kuupäeva ja ajavahemiku, nii nagu välja toodud järgmisel joonisel.

![Näide kõnekeskuse tellimusest, kus järeletulemise ajavahemik on valitud.](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Lisaressursid

[Järeletulemise teabe moodul](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]