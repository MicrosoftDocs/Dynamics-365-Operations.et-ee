---
title: Globaliseerimisfunktsiooni loomine
description: See teema kirjeldab, kuidas luua globaliseerimisfunktsiooni.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94038b0eb412632c348081bbf467f44310d9e955
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603021"
---
# <a name="create-a-globalization-feature"></a>Globaliseerimisfunktsiooni loomine

[!include [banner](../includes/banner.md)]

Saate luua nullist elektroonilise arveldamise funktsiooni või luua selle olemasoleva funktsiooni alusel. Kui loote funktsiooni nullist, peate elektroonilise aruandluse (ER) konfiguratsioonid ja muud komponendid, nt funktsiooni häälestus ja rakenduse seadistuse üksikasjad käsitsi lisama. Olemasoleval funktsioonil põhineva funktsiooni loomisel pärib uus funktsioon kõik põhifunktsiooni konfiguratsioonid ja parameetrid. Saate üle vaadata selle, mis on kopeeritud põhifunktsioonist uude funktsiooni.

## <a name="create-a-feature-from-scratch"></a>Loo nullist funktsioon

See jaotis selgitab, kuidas luua elektroonilise arveldamise funktsioon, kui globaalses hoidlas pole teie äristsenaariumide jaoks globaalses hoidlas saadaval ühtegi boksist väljas asuvat funktsiooni.

Elektroonilise arveldamise funktsiooni loomiseks järgige neid samme.

1. Logige oma teenuse Regulatory Configuration Service (RCS) kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
3. **Valige** suvand Lisa ja seejärel valige ripploendist suvand **Uus** funktsioon.
4. Sisestage elektroonilise arveldamise funktsiooni nimi ja kirjeldus.
5. Valige **Loo funktsioon**. Uue funktsiooni esimene versioon kuvatakse lehe paremal küljel ja selle olek on **Mustand**.

    Järgmiseks peate lisama ER-i konfiguratsioonid ja funktsiooni seadistused. Enne uute või olemasolevate ER-vormingu konfiguratsioonide lisamiseks veenduge, et need on olemas teie kohalikus RCS-i hoidlas.

6. Valige elektroonilise arveldamise funktsioon, millega te töötate.
7. Valige vahekaardil **Konfiguratsioonid** suvand **Lisa**.
8. Sirvige **konfiguratsiooniruudustikus** vormingu konfiguratsioonide leidmiseks, mis on nõutavad konveieri töötlemiseks (nt elektrooniliste arvefailide loomiseks või väliste veebiteenuste vastuste töötlemiseks).
9. Valige nupp **OK**. Konfiguratsioone saate nüüd kasutada müügivõimaluste töötlemise tegevustes. Lisateavet vt teemast Konfiguratsioonide [abil töötada](e-invoicing-work-configurations.md).
10. Elektroonilise arveldamise funktsiooniseadistuse lisamiseks looge see uue **funktsiooni lehe** seadistuste **vahekaardil**. Lisateavet vt Töö [funktsiooniseadistustega](e-invoicing-feature-setup.md).
11. Viige seadistus lõpule ja juurutage elektroonilise arveldamise funktsioon teenuse keskkonda. Lisateavet vt teemast Globaliseerimisfunktsiooni [lõpule viimine, avaldamine ja juurutamine](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Looge failivormingu konfiguratsioonid, mis on tuletatud olemasolevast arvemudelist.

Kui te ei pea looma ER konfiguratsioone, vaid saate olemasolevaid versioone alusena uuesti kasutada, võite selle vahele jätta.

See protseduur näitab, kuidas luua failivormingu konfiguratsioone, mis on nõutavad uue elektroonilise arveldamise funktsiooni jaoks, mida soovite luua. Looge elektroonilise arve failivormingu konfiguratsioon ja kõik muud failivormingu konfiguratsioonid, mida teie uue elektroonilise arveldamise funktsioon nõuab.

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
3. Valige arvemudel **või** brasiilia stsenaariumite puhul **fiskaalmudel**.
4. Valige **konfiguratsioon** loomine ja seejärel valige ripploendist **suvand Andmemudelil põhinev arvevorming**.
5. Sisestage paketi nimi ja kirjeldus vormingu konfiguratsiooniks.
6. Valige **Vormingi tüüp** väljal mahaarvamise tüüp.
7. Valige andmemudeli **definitsiooniväljal** juurstruktuur, et vorming vastendada. Näiteks Arvecustomeri **kasutatakse** kliendiarve vormingute jaoks.
8. Valige **Konfiguratsiooni loomine**.
9. Valige uue vormingu konfiguratsioon.
10. Valige **kujundaja** ja kasutage faili paigutuse konfigureerimiseks vormingukujundaja tööriista nii, et see vastaks failivormingu spetsifikatsioonidele.
11. Sulgege leht.
12. Valige kiirkaardil **Versioonid** käsk **Muuda olekut** \> **Täielik**.
13. Valige **Muuda olekut** \> **Ühiskasutus** et avaldada vormingu konfiguratsioon globaalses hoidlas.

Uued failivormingu konfiguratsioonid tuleb jagada Microsofti domeeniga, enne kui elektroonilise arvelduse teenus neid tarbib.

1. Valige vormingu konfiguratsioon, millega te töötate. Konfiguratsiooni olek peab olema **Ühiskasutuses**.
2. Valige vahekaardil **Versioonid** suvand **Täpsem ühiskasutus** \> **globaalne hoidla**.
3. Valige kiirkaardil **Ühiskasutuses kasutajaga** suvand **Organisatsioon**.
4. Sisestage **väljale Parameetrid** vorming **microsoft.com** et vormingu konfiguratsiooni Microsofti domeeniga jagada.
5. Valige nupp **OK**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Looge funktsioon, mis põhineb olemasoleval funktsioonil.

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
3. Veenduge, **et väljal** Konfiguratsioonipakkuja on valitud aktiivne konfiguratsioonipakkuja. Nii kuvatakse uus elektroonilise arveldamise funktsioon loendis pärast selle loomist. Kui teie aktiivse konfiguratsioonipakkujat ei ole valitud, filtreeritakse uus funktsioon loendist välja.
4. Valige **Lisa** ja seejärel valige dialoogiakna ripploendist suvand **Olemasoleval versioonil põhinev**.
5. Sisestage funktsiooni nimi ja kirjeldus.
6. **Valige funktsiooni põhiversioon** väljal Alusfunktsioon.
7. Valige **Loo funktsioon**. Funktsioon on loodud ja selle olek on **Mustand**.
8. Vaadake üle funktsiooni komponendid, et teha kindlaks, kas värskendused on vajalikud.

    - Vaadake konfiguratsioonid üle, kui teil tuleb kohandada ER-vormingud ja nende sidumine funktsiooni versiooni vorminguvastendustega.
    - Vaadake seadistus üle, kui peate kohandama vahekaardil **Toimingud**, **Kohaldatavusreeglid** või **funktsiooni** versiooni jaoks vahekaardil Muutujad.

9. Viige seadistus lõpule ja juurutage elektroonilise arveldamise funktsioon teenuse keskkonda. Lisateavet vt teemast Globaliseerimisfunktsiooni [lõpule viimine, avaldamine ja juurutamine](e-invoicing-complete-publish-deploy-globalization-feature.md).
