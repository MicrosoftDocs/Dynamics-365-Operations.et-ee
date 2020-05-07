---
title: Projekti hüvitised
description: Selles teemas selgitatakse, kuidas luua või muuta hüvitist.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282822"
---
# <a name="project-grants"></a>Projekti hüvitised

[!include [banner](../includes/banner.md)]

Hüvitis on rahaline kingitus teatud eesmärgi või projekti jaoks. Tavaliselt on hüvitise kulutamise viisidele seatud piirangud. Projektihalduse ja raamatupidamise jaotises saate sisestada ja jälgida hüvitisi ning määratleda nende seosed projektide ja projektilepingutega. Näiteks saate teha järgmiseid toiminguid.

- Seostage hüvitisi projektide ja rahastamisallikatega, kasutades linke lehtedele **Projekt** ja **Projektilepingu üksikasjad**.
- Sisestage ja jälgige hüvitise muudatusi, kui see liigub ühest olekust teise.
- Sisestage ja jälgige kulusid, taotletud summasid ja preemiasummasid.
- Looge peahüvitisi ja seostage nendega alamhüvitisi.

Saate luua hüvitise, sisestades uude kirjesse kõik üksikasjad, või kopeerida olemasoleva hüvitise üksikasju ning siis neid uuendada.

## <a name="create-a-new-grant"></a>Uue hüvitise loomine

1. Avage **Projektihaldus ja raamatupidamine** \> **Hüvitised** \> **Hüvitised**.
2. Valige **Uus** \> **Hüvitis**.
3. Sisestage hüvitise üksikasjade lehel kiirkaardil **Üldine** väljale **Hüvitise ID** hüvitise jaoks tähtedest ja numbritest koosnev identifikaator.
4. Sisestage hüvitise nimi väljale **Hüvitise nimi**.
5. Lisage väljale **Kirjeldus** uue hüvitise üksikasjad.

    Paljud teised lehel olevad väljad on valikulised ning te saate sisestada nii vähe või palju teavet, kui soovite.

    Järgmises loendis kirjeldatakse teavet, mis asub hüvitise üksikasjade lehe igal kiirkaardil.

    - **Üldine** – sisestage hüvitise nimi, olek, kirjeldus, eesmärk ja summa.
    - **Kontaktandmed** – sisestage hüvitist haldava osakonna ja töötajate üksikasjad ning hüvitist pakkuva kliendi või organisatsiooni üksikasjad. Samuti saate näidata, kas teie organisatsioon on läbiv üksus, mis saab hüvitise ja annab selle seejärel edasi teisele saajale. Klõpsake nuppu **Lisa**, et lisada kontaktandmed, nagu selle organisatsiooni telefoninumbrid ja meiliaadressid, kes hüvitist pakub.
    - **Kuupäevad ja tähtajad** – sisestage kuupäevad, mis on seotud hüvitise ja hüvitise avaldusega. Näidete hulka kuuluvad avalduse tähtaeg, esitamise kuupäev ja hüvitise kinnitamise või tagasilükkamise kuupäev.
    - **Seotud projektid ja projektilepingud** – saate sellel kiirkaardil sisestada teavet ainult juhul, kui väli **Hüvitise olek** on kiirkaardil **Üldine** seatud väärtusele **Aktiivne** või **Määratud**. Valige järgmiste valikute seast, et lõpetada seotud ülesanne.

        - **Lisa rahastamisallikas** – lisage hüvitisele uus rahastamisallikas. Saate sisestada kõik üksikasjad kohe või kasutada vaiketeavet ja uuendada seda hiljem.
        - **Lisa projektileping** – lisage või värskendage projektilepingu teavet.
        - **Lisa projekt** – lisage või uuendage projekti üksikasju.

    - **Seadistus** – sisestage ühtivate fondide üksikasjad, kui see teave on nõutav. Paljud organisatsioonid, kes pakuvad hüvitisi, nõuavad saajalt kindlas summas tema enda raha või ressursside kulutamist, mis vastaks hüvitise summale. Saate sisestada väljale **Kohaliku projekti või jälgimise ID** identifikaatori, mis erineb projekti identifikaatorist.

        > [!NOTE]
        > Kui osa hüvitisest antakse mõnele teisele organisatsioonile, seadke valiku **Alamsaaja** väärtuseks **Jah**. Ameerika Ühendriikides antavate hüvitiste puhul saate määrata, kas hüvitis antakse osariigi- või föderaalloa alusel.

    - **Kasutuselevõtu üksikasjad** – lisage või uuendage teavet, kui tihti saab hüvitisi tagasi võtta, arveldada või kulutada.

## <a name="create-a-new-grant-from-a-copy"></a>Loo koopiast uus hüvitis

1. Avage **Projektihaldus ja raamatupidamine** \> **Hüvitised** \> **Hüvitised**.
2. Valige **Uus** \> **Kopeeri hüvitis**.
3. Sisestage uuele hüvitisele tähtedest ja numbritest koosnev identifikaator ning seejärel valige **OK**.
4. Vaadake hüvitise üksikasjade lehel üle kopeeritud hüvitise üksikasjad ja tehke vajalikud muudatused. Enamik lehel olevatest väljadest on valikulised.

## <a name="view-or-modify-grant-details"></a>Vaadake või muutke hüvitise üksikasju

1. Avage **Projektihaldus ja raamatupidamine** \> **Hüvitised** \> **Hüvitised**.
2. Valige muutmiseks hüvitis.
3. Valige tegumiriba vahekaardi **Hüvitis** grupis **Halda** suvand **Redigeeri**.
4. Vaadake üle toetuse üksikasjad ja tehke vajalikud muudatused.
