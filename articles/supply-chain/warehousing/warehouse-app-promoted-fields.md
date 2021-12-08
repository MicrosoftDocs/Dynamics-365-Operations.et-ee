---
title: Warehouse Management mobiilirakenduse sammude jaoks esiletoodud väljade konfigureerimine
description: Selles teemas kirjeldatakse, kuidas reklaamida ja esile tõsta konkreetset teavet Warehouse Management mobiilirakenduse toiminguvoogude mis tahes etapis.
author: MarkusFogelberg
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 392fc4d7e4f423b38e8394fa25d2e42de913bfc6
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860454"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobiilirakenduse sammude jaoks esiletoodud väljade konfigureerimine

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until GA with 10.0.23 -->

> [!IMPORTANT]
> Selles teemas kirjeldatud funktsioonid kehtivad ainult uue mobiilirakenduse Warehouse Management kohta. Need ei mõjuta vana laorakendust, mis on nüüdseks iganenud.

Selles teemas kirjeldatakse, kuidas reklaamida ja esile tõsta konkreetset teavet Warehouse Management mobiilirakenduse toiminguvoogude mis tahes etapis. See võime aitab koondada töötajate tähelepanu kõige olulisematele valdkondadele, kui nad töövoos on. Iga protsessi iga etapi jaoks saavad administraatorid valida, milliseid välju reklaamida ja milliseid esile tõsta.

## <a name="enable-promoted-fields-in-your-system"></a>Lubage oma süsteemis reklaamitud väljad

Enne reklaamiväljade seadistamist peate täitma järgmise protseduuri, et lubada vajalikud funktsioonid ja genereerida vajalikud väljanimed Warehouse Management mobiilirakenduses.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
1. Tööruumis [**Funktsioonihaldus**](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lubage järgmine loetletud funktsioon.

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi:** *laorakenduse etapiviisilised juhised*

    Funktsiooni *Laorakenduse toimingujuhised* kohta lisateabe saamiseks vaadake jaotist [Warehouse Management mobiilirakenduse etappide pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md). See funktsioon on *Laorakenduse esiletoodud väljad* funktsiooni eeltingimus.

1. Lubage loetletud funktsioon järgmisel viisil.

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi:** *Laohalduse rakenduse esiletoodud väljad*

    Seda funktsiooni kirjeldatakse selles teemas.

1. Värskendage Warehouse Management mobiilirakenduses väljade nimesid, avades **Laohaldus \> Seadistamine \> Mobiilseade \> Laorakenduse väljade nimed** ja valides **Loo vaikeseade**. Lisateavet vt [Mobiilirakenduse Warehouse Management väljade konfigureerimine](configure-app-field-names-priorities-warehouse.md).
1. Korrake eelmist sammu iga juriidilise isiku (ettevõtte) puhul, kus kasutate Warehouse Management mobiilirakendust.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Esiletoodud väljade konfigureerimine menüüpõhise ülekirjutamise abil

Kasutage esiletoodud väljade seadistamiseks järgmist protseduuri.

1. Looge vastava menüü ja sammu jaoks menüüpõhine ülekirjutamine, nagu on kirjeldatud jaotises [Warehouse Management mobiilirakenduse sammude pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md).
1. Leidke **Etapi ID** ja **menüüelemendi nime** nende väärtuste kombinatsioon, mida soovite redigeerida, ja valige väärtus veerus **Etapi ID**.
1. Ilmuva lehe kiirkaardil **Esiletoodud väljade valimine** valige tööriistaribal **Vali väljad**.
1. Valige dialoogiboksis **Esiletoodud väljad** väljad, mida soovite välja tuua. Samuti saate esile tõsta kuni kaks valitud välja. Esiletõstetud väljad kuvatakse Warehouse Management mobiilirakenduses paksus kirjas. Väljade valimisel arvestage asjaoluga, et mõned ekraanid võivad olla piisavalt suured, et kuvada ainult üks või kaks ülemist esiletoodud välja. Näide, mis näitab, kuidas neid sätteid kasutada, vaadake selle teema hilisemat stsenaariumi.

    > [!NOTE]
    > Loend **Saadaolevad väljad** on piiratud väljadega, mis võivad kuvada menüüüksuse jaoks. Kuid muud tegurid (nt kauba koostis) määravad, kas väli tegelikult Warehouse Management mobiilirakenduses kuvatakse. Kui olete reklaamiväljad konfigureerinud, kuvatakse Warehouse Management mobiilirakenduse avalehel ainult valitud väljad. Töötajad saavad siiski vaadata ülejäänud välju, vajutades üksikasjade lehte.

1. Sätete rakendamiseks valige **OK**. Teie valitud väljad on nüüd loetletud kiirkaardil **Valige esiletoodud väljad**.

## <a name="example-scenario"></a>Näidisstsenaarium

### <a name="enable-sample-data"></a>Luba näidisandmed

Määratud näidiskirjete ja -väärtuste kasutamiseks selle stsenaariumi läbimiseks peate kasutama süsteemi, kuhu on installitud standardsed demoandmed. Enne alustamist peate valima ka **USMF-i** juriidilise isiku.

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
