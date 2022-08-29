---
title: Töökäskude loomine
description: See artikkel selgitab, kuidas luua varahalduses töötellimusi.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba01a90f805300a27e4550e1371fb55d5e3a7536
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335041"
---
# <a name="creating-work-orders"></a>Töökäskude loomine

[!include [banner](../../includes/banner.md)]

Pärast ennetavate hooldustööde plaanimist on järgmine etapp luua nende jaoks töökäsud. Saate seda teha, kasutades ühte hooldusgraafikutest. Plaanitud töödel võib hooldusgraafikus olla erinevad viitetüübid, nagu järgmises tabelis on kirjeldatud.

| Viite tüüp | Kirjeldus |
|---|---|
| Hoolduskavad | Ennetavad hooldustööd, mis põhinevad hoolduskava tüübil *Aeg* või *Loendur*. |
| Hoolduskorrad | Ennetavad hooldustööd, mis sisaldavad mitut sarnast tüüpi hooldust nõudvat vara. |
| Hooldusnõue | Käsitsi loodud vara hoolduse või paranduse taotlus. Selle taotluse saab teisendada töökäsuks. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Töökäskude loomine teie hooldusgraafikute põhjal

Hooldusgraafikul põhinevate töökäskude loomiseks tehke järgmist.

1. Avage üks järgmistest lehekülgedest, olenevalt sellest, kuidas te soovite oma töökäsud oma ajakava üksuste jaoks valida.

    - Kogu hooldusgraafik (**Varahaldus \> Haldusgraafik \> Kogu hooldusgraafik**)
    - Hooldusgraafiku ridade avamine (**Varahaldus \> Haldusgraafik \> Ava hooldusgraafiku read**)
    - Hooldusgraafiku kaustade avamine (**Varahaldus \> Haldusgraafik \> Ava hooldusgraafiku kaustad**)

1. Märkige ruudustikus märkeruut iga planeeritud hooldustöö puhul, mille jaoks soovite töökäsu luua. Seejärel valige toimingupaanil suvand **Töökäsk**.

    Kuvatakse dialoogiboks **Töökäskude loomine**. Väli **Hooldusprognoosi tunnid** näitab valitud ridade prognoosi tundide koguarvu.

    ![Töökäskude dialoogiboksi loomine.](media/18-preventive-maintenance.png)

1. Määrake jaotises **Parameetrid** loodavate töökäskude arv. Tehke üks järgmistest valikutest:

    - **Üks töökäsk rea kohta** – looge üks töötellimus iga hooldusgraafiku rea kohta.
    - **Üks töökäsk** – looge töökäsud, mis on rühmitatud vastavalt teiste suvandite sätetele, mis muutuvad selle suvandi valimisel kättesaadavaks.

1. Väljal **Töökäsu tüüp** valige töökäsu tüüp, mida kõigi loodavate töötellimuste puhul kasutada.
1. Vastavalt oma seadistustele töökäskude loomiseks valige **OK**.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Hooldusplaani käitamise ajal automaatselt loodavate töökäsu ridade rühmitamine

See funktsioon võimaldab teil määrata reeglid töökäsu ridade rühmitamiseks ühe töökäsu alla, kui süsteem on häälestatud koostama töökäske hooldusplaani põhjal automaatselt. Varem võisid automaatselt loodud töökäsud sisaldada ainult ühte rida. Samas nüüd saate töökäske rühmitada näiteks vara, vara tüübi või töö asukoha alusel. (Käsitsi loodud töötellimusi saab sel viisil juba grupeerida, nagu on kirjeldatud selle artikli eelmises jaotises.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Automaatselt loodud töökäskude rühmitamise lubamine

Enne selle funktsiooni kasutamist tuleb see teie süsteemi jaoks sisse lülitada. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *varahaldus*
- **Funktsiooni nimi:** *töökäskude rühmitamise reeglite rakendamine hooldusplaani käitades*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Automaatselt loodud töökäskude rühmitamise häälestamine

Automaatselt loodud töökäskude rühmitamise häälestamiseks tehke järgmist.

1. Avage **Varahaldus \> Seadistus \> Ennetav hooldus \> Hooldusplaanid**.
1. Iga plaani jaoks, kus soovite rühmitatud töökäsud luua, tehke järgmist.

    1. Valige loendipaanil plaan.
    1. Veenduge kiirkaardil **Read**, et märkeruut **Loo automaatselt** oleks igal real valitud.

1. Avage **Varahaldus \> Perioodiline \> Ennetav hooldus \> Hoolduskavade plaanimine**.
1. Dialoogiboksis **Hoolduskavade plaanimine** jaotises **Perioodiline** määrake plaani ajahorisont (kui kaugele töö loomise jaoks plaanitud hooldustööde otsimisel ette vaadata).
1. Määrake suvand **Loo töökäsk graafikust automaatselt** valikule *Jah*.
1. Valige jaotisest **Töökäsk** üks järgmistest suvanditest.

    - **Üks töökäsk rea kohta** – looge üks töötellimus iga hooldusgraafiku rea kohta. (See suvand pakub samu funktsioone, mis on saadaval, kui funktsioon *Töökäskude rühmitamise reeglite rakendamine hooldusplaani käitades* on välja lülitatud.)
    - **Üks töökäsk** – looge töökäsud, mis on rühmitatud vastavalt teiste suvandite sätetele, mis muutuvad selle suvandi valimisel kättesaadavaks.

1. Kui soovite valikuid rakendada siis, kui käivitate ainult mõned oma hoolduskavad, lisage kiirkaardil **Kaasatavad kirjed** vastavalt vajadusele filtrid, nagu võite teha Microsoft Dynamics 365 Supply Chain Managementi teiste pakett-tööde puhul.
1. Häälestage kiirkaardil **Käivita taustal** vastavalt vajadusele partii ja plaanimise valikud, nagu võite teha teiste rakenduse Supply Chain Management pakett-töödes.
1. Valitud hoolduskavade käivitamiseks ja/või plaanimiseks valige **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]