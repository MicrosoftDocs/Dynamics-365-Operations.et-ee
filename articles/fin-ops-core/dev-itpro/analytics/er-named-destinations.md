---
title: Prindihalduse kirjepõhise ER-i sihtkoha konfigureerimine
description: Sellest teemast selgitatakse, kuidas konfigureerida prindijuhtimise kirje konkreetseid sihtkohti elektroonilise aruandluse (ER) vormingule, mis on konfigureeritud väljaminevate dokumentide genereerimiseks.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4cd99b1d2c0dbbf48e7eee7e1233e3b078d14ba3
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603050"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Prindihalduse kirjepõhise ER-i sihtkoha konfigureerimine

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas süsteemiadministraatori või saadaolevate arvete haldaja rollis olev kasutaja saab täita järgmisi ülesandeid:

- Konfigureerige nimeline [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) sihtkohad ER-i lahendusele, mis loob vabas vormis arved.
- Määrake ER-i sihtkoht ühele [prindihalduse](document-reporting-services.md) kirjele.

Protseduurid saab lõpule viia USMF -i ettevõttes. Koodi pole vaja kirjutada.

## <a name="introduction"></a>Sissejuhatus

Saate konfigureerida [sihtkohad](electronic-reporting-destinations.md) iga failiväljundi komponendi kausta jaoks ER [vormingu](general-electronic-reporting.md) [konfiguratsioon](general-electronic-reporting.md#Configuration) , mida kasutatakse väljamineva dokumendi jaoks. Kasutajad, kes kasutavad seda tüüpi ER-vormingut ja kellel on vastavad pääsuõigused, saavad muuta konfigureeritud sihtkoha sätteid ka käitusajal.

Finantsversioonis Microsoft Dynamics 365.0.17 **ja** uuemas versioonis saab ER-vormingu jaoks häälestada tegevuskoodi, et määratleda tegevus, [mida](er-apis-app10-0-17.md) kasutajad selle ER-vormingu käivitades teevad. Näiteks moodulis **Müügireskontro**, saate prindihalduse sätetes valida ER-vormingu, mis loob kindla äridokumendi, nt vabas vormis arve. Seejärel saate arve eelvaate kuvamiseks valida nupu **Kuva** või printerisse saatmiseks nupu **Prindi**. Kui kasutaja tegevus edastatakse töötavasse ER-vormingusse käitusajal, saate [konfigureerida erinevate ER sihtkohtadde erinevatele kasutajatoimingutele](er-action-dependent-destinations.md).

Finants **versioonis 10.0.21 ja uuemas** saab nimelise sihtkoha [seadistada](er-apis-app10-0-21.md) ER-vormingu jaoks ja määrata prindihalduse kirjele, mis töödeldakse ER-vormingu käivitamisel. Näiteks moodulis **Müügireskontro** prindihalduse sätetes kui soovite konfigureerida **Algse** kirje, et sooritama järgmisi toiminguid:

- ER-vormingute käitamine.
- Saate loodud arve kliendile meiliga saata.
- Konfigureerige **Kopeeri** kirje, et käitada sama vormi.
- Saate printida arve koopia võrguprinterile.

Sellisel juhul peate konfigureerima käitatavale ER-vormingule erinevad ER sihtkohad ja peate valima sihtkohad erinevatele prindihalduse kirjetele.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist peab **Luba seadistada ER sihtkohti prindihalduse üksusel** funktsioon olema sisse lülitatud [funktsiooni haldus](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) tööruumis. Lähtekoodi tuleb muuta ka, et lubada nimetatud ER-sihtkohtade konfigureerimist praeguses Finance eksemplaris ja lubada [uus](er-apis-app10-0-21.md) ER API.

Lisaks tuleb **Vabas vormis arve (Excel)** ER-i konfiguratsiooni [importida](er-download-configurations-global-repo.md) praeguses rakenduses Finance.

## <a name="configure-a-new-er-destination"></a>Elektroonilise uue sihtkoha konfigureerimine

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige arve kliendikontole **USA-001**.
3. Lehel **Vabas vormis arve** vahekaardil **Arve** **Prindihalduse** grupis valige **Prindihaldus**.
4. Lehel **Prindihalduse seadistus** laiendage valikut **Moodul - müügireskontro** \> **Dokumendid** \> **Vabas vormis arve** ja seejärel **Originaal** kirje, ja siis järgige järgmisi tegevusi:

    1.  Jälgige valitud kirje praegusi sätteid:
        -   Vaikimisi SSRS-aruanne **VabaTekstiArve.Aruanne** on valitud **aruande vormingu** väljal.
        -   Nimi **\<Default\>** kuvatakse **Siht** väljal teavitades, et määratud SSRS-aruande jaoks pole valitud kohandatud sihtkohta. 
    2.  Valige **Arruande vormingu** väljal **Vabas vormis arve (Excel)** ER vormingu konfiguratsioon.
        -   **Sihtkoha** nimi väljal muudetakse **Sihtkoha nimi**.
        -   Väljal **\<No named destination\>** nimi kuvatakse **Sihtkoha nimi** mis teatab, et määratud ER -vormingu jaoks pole valitud sihtkohta valitud.
    3.  Valige **sihtnime** väljast paremal asuv nooleklahv.    
    4. Lehele **Elektroonilise aruandluse nimelise sihtkoha** väljale **Nimi** sisestage **Põhisihtkoht**.
    5. Valige käsk **Salvesta**.
    6. **Faili sihtkoha** kiirkaardil [konfigureerige](er-destination-type-email.md) **E-kirja** sihtkoht **Aruande** komponendi jaoks.
    7. Sulgege **elektroonilise aruandluse siht** leht.
    8. Valige **prindihalduse seadistus** lehe **Sihtkoha nimi** väljal **põhisihtkoht** nimetatud sihtkoht.

    ![Nimelise ER-i sihtkoha konfigureerimine valitud ER-vormingu jaoks ja selle määramine konfigureeritud prindihalduse kirjele prindihalduse häälestuslehel](./media/er-named-destinations-01.gif)

    Olete nüüd konfigureerinud nimelise ER sihtkoha **Põhisihtkoht** vomingu **Vaba vormis arve (Excel)** ja määranud selle jaotises **Originaal** prindihaldus kirje **Moodul - müügirreskontro** \> **Dokumendid** \> **Vabas vormis arve**.

5. Laiendage **Moodul - müügireskontro** \> **Konto - US-001** \> **Vabas vormis arve** valige **Originaal** kirje ja seejärel järgige neid samme:

    1. Valige fail ja hoidke all (või paremklõpsake) kirjel ning seejärel valige **Kirjuta üle**.
    2. Valige **sihtnime** väljast paremal asuv nooleklahv.
    3. **Elektroonilise aruandluse siht** lehel tegevuspaanil valige **Uus**.
    4. Väljale **Nimi** sisestage **US-001 sihtkoht**.
    5. **Faili sihtkoha** kiirkaardil [konfigureerige](er-destination-type-print.md) **Printeri** sihtkoht **Aruande** komponendi jaoks.
    6. Sulgege **elektroonilise aruandluse siht** leht.
    7. Valige **prindihalduse seadistus** lehe **Sihtkoha nimi** väljal valige **US-001 sihtkoht** nimetatud sihtkoht.

    ![Nimelise ER-i sihtkoha konfigureerimine valitud ER-vormingu jaoks ja selle määramine konfigureeritud prindihalduse kirjele prindihalduse häälestuslehel](./media/er-named-destinations-02.gif)

    Olete nüüd konfigureerinud nimelise ER sihtkoha **US-001 sihtkoht** vomingu **Vaba vormis arve (Excel)** ja määranud selle jaotises **Originaal** prindihaldus kirje **Moodul - müügirreskontro** \> **Konto - US-001** \> **Vabas vormis arve**.

Nüüd, kui töödeldakse vabas vormis arvet, käivitatakse **vabas vormis arve (Excel)** ER-vorming ja toimub üksjärgmistest sündmustest:

- Kui vabas vormis arve on kliendile, kes ei ole US-001, saadetakse loodud dokument meiliga.
- Kui vabas vormis arve on kliendile, kes ei ole US-001, prinditakse loodud dokument.

> [!NOTE]
> Kui nimega sihtkoht pole käitusajal töödeldav prindihalduse kirje jaoks määratletud, kasutatakse ER-i vaikesihtkohti, kui need on saadaval käitatavale ER-vormingule.

> [!IMPORTANT]
> Kui **Elektroonilise aruandluse sihtlehel** lehel (**organisatsiooni halduse** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse sihtkoht**) valite ER -vormingu, mille jaoks on konfigureeritud vähemalt üks nimega sihtkoht, teavitatakse teid nimetatud sihtkohtade olemasolust.
>
> ![Teatis konfigureeritud nimega sihtkohtade olemasolu kohta valitud ER-vormingu jaoks elektroonilise aruandluse sihtlehel](./media/er-named-destinations-03.png)
>
> Kui kustutate vaikesihtkoha, kustutatakse ka kõik nimetatud sihtkohad. Kui prindihalduse kirjete jaoks on valitud need nimega sihtkohad, tühistatakse nende sihtkohtade valik.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Olemasoleva ER-sihtkoha kopeerimine uue nimega sihtkohana

Kui ER-i vaikesihtkoht on ER-vormingu jaoks saadaval, saab seda kasutada uute ER-sihtkohtade mallina. Vaikesihtkohal põhineva uue ER-i sihtkoha loomiseks valige suvand **Kopeeri vaikimisi** **Elektroonilise aruandluse nimega siht** lehel. Uue sihtkoha nimi on **Vaikimisi**. Võite seda sammu korrata nii mitu korda kui vaja.

Uue nimega sihtkoha mallina saate valida mis tahes olemasoleva nimega sihtkoha. Vaikesihtkohal põhineva uue ER-i sihtkoha loomiseks valige suvand **Kopeeri** **Elektroonilise aruandluse nimega siht** lehel. Uuel sihtkohal on valitud nimega sihtkohaga sama nimi, kuid lisatakse järelliide "Kopeeri". Võite seda sammu korrata nii mitu korda kui vaja.

## <a name="security-considerations"></a>Turbemeetmed

Nimelise ER sihtkoha saate seadistada **prindihalduse seadistus** lehel, siis, kui teil on [luba](../sysadmin/role-based-security.md#permissions) seda ülesannet teostada. Teile antakse luba, kui **konfigureerite elektroonilise aruandlusvormingu sihtkoha** [kohustusele](../sysadmin/role-based-security.md#duties) on määratud üks teie [turberollidest](../sysadmin/role-based-security.md#security-roles). Lisateavet leiate teemast [Turvakaalutlused](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)

[Elektroonilise aruandluse raamistiku API muudatused Application update 10.0.17 puhul](er-apis-app10-0-17.md)

[Elektroonilise aruandluse raamistiku API muudatused Application update 10.0.21 puhul](er-apis-app10-0-21.md)

[Koodi muutmine, et lubada kasutajatel nimega ER-sihtkohti konfigureerida ja kasutada](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
