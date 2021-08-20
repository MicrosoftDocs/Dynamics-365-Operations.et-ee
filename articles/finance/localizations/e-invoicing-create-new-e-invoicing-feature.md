---
title: Elektroonilise arvelduse funktsioonide loomine
description: See teema kirjeldab, kuidas luua uus elektroonilise arveldamise funktsioon, kui teie riigi või regiooni jaoks pole konfigureeritavat funktsiooni saadaval.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744931"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Elektroonilise arvelduse funktsioonide loomine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua uus elektroonilise arveldamise funktsioon, kui teie riigi või regiooni jaoks pole konfigureeritavat funktsiooni saadaval.

Järgige neid samme, et luua uus elektroonilise arvelduse funktsioon:

1. Looge uus failivormingu konfiguratsioon, kasutades antud arve mudeli konfiguratsiooni ja kasutades olemasolevat arve vastendamist funktsioonile, mida soovite luua.
2. Lisage failivormingu konfiguratsioonid elektroonilise arvelduse funktsiooni konfiguratsioonidele.
3. Loodud elektroonilise arvelduse funktsiooni seadistamine.
4. Viige uus elektroonilise arveldamise funktsioon lõpule ja avaldage see oma organisatsiooni globaalses hoidlas.
5. Uue elektroonilise arveldamise funktsiooni juurutamine teenuse keskkonda.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Looge uued failivormingu konfiguratsioonid, mis on tuletatud olemasolevast arvemudelist

Selles protseduuris loote failivormingu konfiguratsioonid, mis on nõutavad uuele elektroonilise arveldamise funktsioonile, mida soovite luua. Saate luua elektroonilise arve failivormingu konfiguratsiooni ja mis tahes muud failivormingu konfiguratsioonid, mida teie uus elektroonilise arveldamise funktsioon võib vajada.

Enne selle protseduuri alustamist logige sisse Regulatory Configuration Service (RCS) kontole.

1. Rakenduses Microsoft Dynamics 365 Finance **Elektrooniline aruandluse** tööruumis valige **Hoidlad** **Microsoft** konfiguratsiooni pakkuja jaoks.
2. Valige **globaalne**, käsk **Ava** ja seejärel vasakul paanil **arvemudeli** konfiguratsioon.

    > [!IMPORTANT]
    > Brasiilia puhul valige selle asemel **fiskaaldokumentide** mudeli konfiguratsioon.

3. Valige vahekaardil **Konfiguratsioonid** suvand **Impordi**.
4. Sulgege leht.
5. Sulgege leht.
6. Valige **Aruandluskonfiguratsioonid** paanil ja seejärel valige imporditav arvemudel.
7. Valige käsk **Loo konfiguratsioon** ja seejärel valige arve **kontekstimudelil põhinev vorming**.
8. Sisestage paketi nimi ja kirjeldus vormingu konfiguratsiooniks.
9. Valige **Vormingi tüüp** väljal mahaarvamise tüüp.
10. Valige **Loo konfiguratsioon** ja seejärel valige äsja loodud konfiguratsiooni vorming.
11. Valige **kujundaja** ja kasutage faili paigutuse konfigureerimiseks vormingukujundaja tööriista nii, et see vastaks failivormingu spetsifikatsioonidele.
12. Sulgege leht.
13. Valige kiirkaardil **Versioonid** käsk **Muuda olekut** \> **Täielik**.
14. Valige **Muuda olekut** \> **Ühiskasutus** et avaldada vormingu konfiguratsioon globaalses hoidlas.

Uus failivormingu konfiguratsioon tuleb ühiskasutusse anda Microsoft domeeniga, enne kui elektroonilise arvelduse teenus saab konfiguratsiooni tarbida.

1. Valige vormingu konfiguratsioon, millega te töötate. Konfiguratsiooni olek peab olema **Ühiskasutuses**.
2. Valige vahekaardil **Versioonid** suvand **Täpsem ühiskasutus** \> **globaalne hoidla**.
3. Valige kiirkaardil **Ühiskasutuses kasutajaga** suvand **Organisatsioon**.
4. Sisestage **Parameetrid** väljale **Microsoft.com** et vormingu konfiguratsiooni Microsoft`i domeeniga jagada.
5. Valige nupp **OK**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Uue elektroonilise arvelduse funktsiooni loomine

1. RCS-i tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
2. Valige **Lisa** ja seejärel **Uus funktsioon**.
3. Sisestage nimmi ja kirjeldus elektroonilise arvelduse funktsioonile.
4. Valige **Loo funktsioon**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Lisage elektroonilise arvelduse funktsiooni konfiguratsioonid

1. Valige elektroonilise arvelduse funktsioon, millega töötate.
2. Valige vahekaardil **Konfiguratsioonid** suvand **Lisa**.
3. Ruudustikus **konfiguratsioonid** sirvige ja valige failivormingu konfiguratsioonid, mida teie elektroonilise arveldamise funktsioon vajab elektroonilise arvefaili loomiseks.
4. Valige nupp **OK**.

## <a name="add-electronic-invoicing-feature-setups"></a>Elektroonilise arvelduse lisandmooduli seadistuse lisamine

1. Valige **Seadistused suvand** vahekaardil **Lisa** ja seejärel **kohandatud häälestus**.
2. Sisestage funktsiooni seadistuse nimi ja kirjeldus.
3. Väljal **Häälestustüüp** valige suvand **Töötlemise torujuhe**.
4. Valige **Loo**.
5. Valige seadistus, millega töötate, ja seejärel valige **Redigeeri**.
6. **Töötlemise torujuhe** vahekaardil valige **Uus** müügivõimaluste tegevuse lisamiseks. Lisateavet müügikanalite kohta vaata [Tegevused](e-invoicing-configuration-rcs.md#actions).
7. Vahekaardil **Rakendatavuse reeglid** valige **Uus**, et lisada kohaldatavuse reegli klausleid. Lisateavet rakendatavuse reeglite kohta vt jaotisest [Rakendatavuse reeglid](e-invoicing-configuration-rcs.md#applicability-rules).
8. **Muutujate** vahekaardil lisage **uus** et lisada muutujaid nagu soovitud.
9. Valige **Salvesta** ja seejärel valige **Valideeri** et kontrollida konfiguratsiooni ühtsust.
10. Sulgege leht.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Uue elektroonilise arveldamise funktsiooni juurutamine teenuse keskkonda

Teavet selle ülesande lõpule viimise kohta vaadake [Elektroonilise arveldamise funktsiooni juurutamine teenuse keskkonda](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Elektroonilise arveldamise funktsiooni juurutamine ühendatud rakendusse

Teavet selle ülesande lõpule viimise kohta vt [Rakenduse häälestuse konfigureerimine](e-invoicing-get-started.md#configure-the-application-setup) ja  [Elektroonilise arveldamise funktsiooni juurutamine ühendatud rakendusega](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
