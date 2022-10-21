---
title: Warehouse Management mobiilirakenduse sammude jaoks esiletoodud väljade konfigureerimine
description: See artikkel kirjeldab, kuidas propageerida ja tõsta esile konkreetset teavet mis tahes sammu kohta laohalduse mobiilirakenduse ülesannete voogudes.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepSelectPromotedFields, WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e2d65f20febaf9bd1d143414054b121f8decb7c0
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689826"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobiilirakenduse sammude jaoks esiletoodud väljade konfigureerimine

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Selles artiklis kirjeldatud funktsioonid kehtivad ainult uuele laohalduse mobiilirakendusele. Need ei mõjuta vana laorakendust, mis on nüüdseks iganenud.

See artikkel kirjeldab, kuidas propageerida ja tõsta esile konkreetset teavet mis tahes sammu kohta laohalduse mobiilirakenduse ülesannete voogudes. See võime aitab koondada töötajate tähelepanu kõige olulisematele valdkondadele, kui nad töövoos on. Iga protsessi iga etapi jaoks saavad administraatorid valida, milliseid välju reklaamida ja milliseid esile tõsta.

## <a name="enable-promoted-fields-in-your-system"></a>Lubage oma süsteemis reklaamitud väljad

Kui käitate tarneahela haldamise versiooni 10.0.28 või varem, peate enne propageeritud väljade häälestamist sooritama järgmised protseduurid, et lubada nõutavad funktsioonid ja luua laohalduse mobiilirakenduses nõutavad väljanimed. Kui käitate tarneahela halduse versiooni 10.0.29 või uuemat versiooni, on funktsioonid kohustuslikud ja neid ei saa välja lülitada, seega võite selle protseduuri vahele jätta.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**. (Vt [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) selle lehe kohta lisateabe saamiseks.)
1. Veenduge, et lao *rakenduse juhiste funktsioon* on teie süsteemi jaoks sisse lülitatud. See funktsioon on *Laorakenduse esiletoodud väljad* funktsiooni eeltingimus. Tarneahela halduse versiooni 10.0.29 puhul on see kohustuslik ja seda ei saa välja lülitada. Funktsiooni *Laorakenduse toimingujuhised* kohta lisateabe saamiseks vaadake jaotist [Warehouse Management mobiilirakenduse etappide pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md).
1. Veenduge, et laorakenduse *propageeritud väljade* funktsioon on teie süsteemi jaoks sisse lülitatud. See on selles artiklis kirjeldatud funktsioon. Tarneahela halduse versiooni 10.0.29 puhul on see kohustuslik ja seda ei saa välja lülitada.
1. Värskendage Warehouse Management mobiilirakenduses väljade nimesid, avades **Laohaldus \> Seadistamine \> Mobiilseade \> Laorakenduse väljade nimed** ja valides **Loo vaikeseade**. Korrake seda sammu iga juriidilise isiku (ettevõtte) puhul, kus te kasutate laohalduse mobiilirakendust. Lisateavet vt [Mobiilirakenduse Warehouse Management väljade konfigureerimine](configure-app-field-names-priorities-warehouse.md).

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Esiletoodud väljade konfigureerimine menüüpõhise ülekirjutamise abil

Kasutage esiletoodud väljade seadistamiseks järgmist protseduuri.

1. Looge vastava menüü ja sammu jaoks menüüpõhine ülekirjutamine, nagu on kirjeldatud jaotises [Warehouse Management mobiilirakenduse sammude pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md).
1. Leidke **Etapi ID** ja **menüüelemendi nime** nende väärtuste kombinatsioon, mida soovite redigeerida, ja valige väärtus veerus **Etapi ID**.
1. Ilmuva lehe kiirkaardil **Esiletoodud väljade valimine** valige tööriistaribal **Vali väljad**.
1. Valige dialoogiboksis **Esiletoodud väljad** väljad, mida soovite välja tuua. Samuti saate esile tõsta kuni kaks valitud välja. Esiletõstetud väljad kuvatakse Warehouse Management mobiilirakenduses paksus kirjas. Väljade valimisel arvestage asjaoluga, et mõned ekraanid võivad olla piisavalt suured, et kuvada ainult üks või kaks ülemist esiletoodud välja. Näide, mis näitab, kuidas neid sätteid kasutada, vaadake stsenaariumi selles artiklis hiljem.

    > [!NOTE]
    > Loend **Saadaolevad väljad** on piiratud väljadega, mis võivad kuvada menüüüksuse jaoks. Kuid muud tegurid (nt kauba koostis) määravad, kas väli tegelikult Warehouse Management mobiilirakenduses kuvatakse. Kui olete reklaamiväljad konfigureerinud, kuvatakse Warehouse Management mobiilirakenduse avalehel ainult valitud väljad. Töötajad saavad siiski vaadata ülejäänud välju, vajutades üksikasjade lehte.

1. Sätete rakendamiseks valige **OK**. Teie valitud väljad on nüüd loetletud kiirkaardil **Valige esiletoodud väljad**.

## <a name="example-scenario"></a>Näidisstsenaarium

### <a name="enable-sample-data"></a>Luba näidisandmed

Määratud näidiskirjete ja väärtuste kasutamiseks selle stsenaariumi läbimiseks peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md). Enne alustamist peate valima ka **USMF-i** juriidilise isiku.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigureerige müügikomplekti numbrimärgi etapil esiletoodud sammudega

Selle protseduuri käigus seadistate numbrimärgi etapis menüüüksuse **Müügiks valimine** jaoks reklaamitud ja esiletõstetud väljad.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme etapid**.
1. Otsige üles sammu ID, mille nimi on *LicensePlateId* ja valide see.
1. Valige toimingupaanilt suvand **Lisa etapi konfiguratsioon**.
1. Kasutage rippmenüü dialoogiboksis välja **Menüüüksus**, et leida ja valida *Müügiks valimine*.
1. Valige nupp **OK**.
1. Ilmub äsja loodud ülekirjutamise üksikasjade leht. Kiirkaardil **Esiletoodud väljade valimine** valige tööriistaribal **Vali väljad**.
1. Saate dialoogiboksis **Esiletoodud väljad** valida väljad mida reklaamida ja esile tõsta. Otsige üles ja valige loendist **Saadaolevad väljad** järgmised väljad ning liigutage need nuppude abil loendisse **Valitud väljad**.

    - Asukoht
    - Kaup
    - Toote nimi
    - Lao olek

1. Kasutage üles- ja allanoole nuppe, et kohandada väljade järjekorda loendis **Valitud väljad**. Warehouse Management mobiilirakenduses kuvatakse väljad siin seatud järjekorras.
1. Valige väli **Asukoht** ja seejärel **Esiletõstmine**.
1. Valige konfiguratsiooni salvestamiseks **OK**.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobiilirakenduse jaoks esiletoodud väljade kuvamine

Selle protseduuri käigus avate Warehouse Management mobiilirakenduse ja läbite eelmises protseduuris reklaamitud ja esile tõstetud väljade kuvamiseks vajalikud toimingud.

1. Looge Microsoft Dynamics 365 Supply Chain Management rakenduses müügitellimus, mis nõuab numbrimärki jälgitavast asukohast valimiseks valimisetappi. Seejärel vabastage müügitellimus lattu. Märkige üles loodava töö ID.
1. Avage Warehouse Management mobiilirakendus ja logige sisse lattu 24. (Standardsete demoandmete korral logige sisse, kasutades kasutaja ID-na nr *24* ja paroolina nr *1*.)
1. Valige menüü **Väljaminev** ja seejärel menüüelement **Müükide komplekteerimine**.
1. Järgige ekraanil kuvatavaid andmesisestusjuhiseid, et sisestada 1. sammus loodud töö ID.
1. Sammul, mis sisaldab teksti **Skanni numbrimärki**, peaksite nägema üksikasjade lehel tehtud muudatusi. Väljad kuvatakse esiletoodud väljade jaoks määratud järjekorras ja väli **Asukoht** kuvatakse paksus kirjas.
