---
title: SharePointi kanali konfigureerimine
description: See artikkel selgitab, kuidas konfigureerida Microsofti kanalit SharePoint sissetulevate elektrooniliste arvete töötlemiseks.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 89538adde4d14212fb0deccad05f828d146f16db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910037"
---
# <a name="configure-a-sharepoint-channel"></a>SharePointi kanali konfigureerimine

[!include [banner](../includes/banner.md)]

Eeltingimusena Microsofti kanali konfigureerimisel sissetulevate SharePoint dokumentide töötlemiseks viige lõpule [ühenduse konfigureerimises kirjeldatud juhised SharePoint](e-invoicing-create-sharepoint-connection.md).

Kanalit saate kasutada SharePoint oma kaustades talletatud failidest elektrooniliste hankijaarvete importimiseks SharePoint.

1. Looge oma SharePoint saidil järgmised kaustad:

    - **Põhikaust** – kaust, millelt teenus faile töötleb.
    - **Arhiivikaust** – kaust, kuhu töödeldud failid talletatakse.
    - **Tõrgete kaust** – kaust, kuhu süsteem teisaldab failid, kui töötlemine nurjub.

2. Valige regulatiivses konfiguratsiooniteenuses (RCS) loodud elektroonilise arveldamise funktsioon. Veenduge, et valite versiooni, mille olek on **Mustand**.
3. Vahekaardil **Seadistused** valige **lisa**.
4. **Valige väljagrupi Uus** funktsiooniseadistuse loomine **ripploendist** Uus suvand Kohandatud **seadistus**.
5. Valige jaotises **Seadistuse** tüüp suvand **Andmekanal**.
6. **Valige kaust väljal Andmekanali** **SharePoint valimine**.
7. Valige **Loo**.
8. Valige rida, mille lõite, ja seejärel valige käsk **Redigeeri**.
9. **Seadke jaotise Parameetrid** vahekaardil **Andmekanal** järgmised nõutavad väljad.

    | Väli                 | Kirjeldus |
    |-----------------------|-------------|
    | Andmekanal          | Sisestage kordumatu nimi andmekanali tuvastamiseks. Nime maksimumpikkus on 10 märki. Sellele viidatakse kommunikatsiooniprotsessi jooksul kohaldatavusreeglites ja ühendatud rakendustes. |
    | SharePointi aadress    | Sisestage SharePoint URL. Sisestage näiteks `<domain>.sharepoint.com`. |
    | Rakenduse ID        | Sisestage Azure Key Vault-saladus, mis sisaldab kasutajakonto SharePoint ID-d. See saladus tuleb luua Võtme vaultis ja seadistada oma teenuse keskkonnas. Väärtus on ühenduse **konfigureerimise rakenduse (kliendi) ID**[SharePoint väärtus.](e-invoicing-create-sharepoint-connection.md) |
    | Rakenduse saladus    | Sisestage võtme vault-saladus, mis sisaldab kasutajakonto SharePoint parooli. Väärtus on rakenduse registreerimise **salaväärtus** ühenduse [konfigureerimisest SharePoint](e-invoicing-create-sharepoint-connection.md). |
    | Saidi nimi             | Sisestage saidi SharePoint nimi. |
    | Dokumenditeegi nimi | Sisestage dokumenditeegi SharePoint nimi. |
    | Ajalõpp               | Sisestage maksimaalne aeg millisekundites (ms), mida süsteem peaks vastuseks ootama. Vaikeväärtus on 10 000 ms (10 sekundit). |
    | Põhikaust           | Määrake faili importimise allikas või kaust, millelt teenus faile töötleb. |
    | Arhiivikaust        | Määrake kaust, kuhu töödeldud failid tuleks salvestada. |
    | Tõrke kaust          | Määrake kaust, kuhu süsteem peaks failid teisaldama, kui töötlemine nurjub. |
    | Maksimaalne faili maht         | Sisestage töödeldav üksikfaili maksimaalne suurus baitides. Vaikeväärtus on 20,000,000 baiti. |
    | Maksimaalne failide arv      | Sisestage maksimaalne failide arv, mida üksiku tegevuse puhul töödelda. Kui te ei soovi failide arvu piirata, seadke väärtuseks **0** (null). |
    | Faili filter           | Sisestage string failinime järgi filtreerimiseks. Väli on valikuline. Toetatakse lihtmaski, nagu näiteks **\*smth\*.ext**, kus iga tärn (\*) tähistab iga tähemärgi nulli või rohkem esinemiskordi. Sisestage näiteks **\*.pdf,** et konfigureerida kanal PDF-faile loema. |
    | Kohandatud failinimi      | Sisestage kliendist kohandatud faili nimi. |

10. Vaadake vahekaardil **Kohaldatavusreeglid** läbi ja uuendage kriteeriume vastavalt vajadusele. Kanali välja väärtus **peab** olema võrdne eelmises sammus **andmekanali** väljale sisestatud väärtusega.
11. Valige **Salvesta** ja sulgege leht.
