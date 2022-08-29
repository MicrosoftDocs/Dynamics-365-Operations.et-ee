---
title: Kaupade registreerimine on lubatud laohaldusprotsesside jaoks saabuva kauba töölehe abil
description: See artikkel sisaldab stsenaariumi, mis näitab, kuidas registreerida kaupu kauba saabumise töölehel, kui kasutate laohaldusprotsesse (WMS).
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66fc9e21b79d70ec14750440c74d354bb8ec0695
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219594"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Kaupade registreerimine on lubatud laohaldusprotsesside jaoks saabuva kauba töölehe abil

[!include [banner](../../includes/banner.md)]

See artikkel sisaldab stsenaariumi, mis näitab, kuidas registreerida kaupu kauba saabumise töölehel, kui kasutate laohaldusprotsesse (WMS). Seda teeb üldjuhul vastuvõtuametnik.

## <a name="enable-sample-data"></a>Luba näidisandmed

Selle stsenaariumi läbimiseks, kasutades käesoleva artikli näidiskirjeid ja -väärtusi, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../../fin-ops-core/fin-ops/get-started/demo-data.md), *ja enne alustamist peate valima USMF-i* juriidilise isiku.

Selle stsenaariumi saate läbi töötada, asendades väärtused oma andmetega, kui teil on saadaval järgmised andmed.

- Kinnitatud ostutellimus peab olema avatud ostutellimuse reaga.
- Real olev kaup peab olema ladustatav. See ei tohi kasutada tootevariante ja sellel ei tohi olla jälgimisdimensioone.
- Üksus peab olema seotud salvestusmõõtmete grupiga, millel on lubatud laohalduse protsess.
- Kasutatav ladu peab OLEMA WMS-i jaoks lubatud ja vastuvõtul kasutatav asukoht peab olema litsentsiplaadiga juhitav.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Kauba saabumise töölehe päise loomine, mis kasutab laohaldust

Järgnev stsenaarium näitab, kuidas luua saabuva kauba töölehe päist, mis kasutab laohaldust.

1. Veenduge, et teie süsteem sisaldaks kinnitatud ostutellimust, mis vastab eelmises jaotises toodud nõuetele. See stsenaarium kasutab ostutellimust ettevõttele *USMF*, hankija kontole *1001*, laole *51* tellimuse reaga *10 PL* (10 kaubaalust) kaubakoodiga *M9200*.
1. Märkige üles ostutellimuse number, mida kasutate.
1. Avage **Varude haldus \> Töölehe sisestused \> Kauba saabumine \> Kauba saabumine**.
1. Valige Toimingupaanil suvand **Uus**.
1. Avaneb dialoogiboks **Laohalduse töölehe loomine**. Valige väljal **Nimi** töölehe nimi.
    - Kui kasutate *USMF* näidisandmeid, valige *WHS*.
    - Kui kasutate oma andmeid, peab teie valitava töölehe valik **Kontrolli komplekteerimisasukohta** olema seadistatud valikule *Ei* ja **Vahelao haldus** valikule *Ei*.
1. Määrake **Viide** väärtuseks *Ostutellimus*.
1. Määrake **Konto number** väärtuseks *1001*.
1. Määrake **Number** selle ostutellimuse numbrile, mille selle teostamistaotluse puhul määratlete.

    ![Saabuva kauba tööleht.](../media/item-arrival-journal-header.png "Saabuva kauba tööleht")

1. Valige töölehe päise loomiseks **OK**.
1. Valige jaotises **Töölehe read** suvand **Lisa rida** ja sisestage järgmised andmed.
    - **Kauba number** – määrake väärtuseks *M9200*. **Piirkond**, **Ladu** ja **Kogus** seatakse 10 kaubaaluse laokande andmete põhjal (1000 ea.).
    - **Asukoht** – seadistage väärtuseks *001*. See konkreetne asukoht ei jälgi litsentsiplaate.

    ![Kauba saabumistöölehtede rida.](../media/item-arrival-journal-line.png "Kauba saabumistöölehtede rida")

    > [!NOTE]
    > Väli **Kuupäev** määratleb kuupäeva, millal selle kauba vaba kaubavaru kogus laos registreeritakse.  
    >
    > **Partii ID** sisestab süsteem, kui esitatud teabe põhjal on võimalik see üheselt tuvastada. Vastasel juhul peate selle sisestama käsitsi. See on vajalik väli, mis seob registreeringu kindla lähtedokumendi reaga.  

1. Valige toimingupaanil **Valideeri**. See kontrollib, kas tööleht on sisestamiseks valmis. Kui kontrollimine nurjub, peate tõrked enne töölehe sisestamist kõrvaldama.  
1. Avaneb dialoogiboks **Kontrolli töölehti**. Valige nupp **OK**.
1. Vaadake üle sõnumiriba. Kuvatama peaks teade, et toiming on lõpule viidud.  
1. Tehke toimingupaanil valik **Väljastamine**.
1. Avaneb dialoogiboks **Sisesta tööleht**. Valige nupp **OK**.
1. Vaadake üle sõnumiriba. Kuvatama peaks teade, et toiming on lõpule viidud.
1. Valige toimingupaanil **Funktsioonid > Toote tšekk** ostutellimuse rea värskendamiseks ja toote tšeki sisestamiseks.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
