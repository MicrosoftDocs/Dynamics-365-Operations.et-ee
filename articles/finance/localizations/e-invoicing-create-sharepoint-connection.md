---
title: SharePoint Ühenduse konfigureerimine
description: See teema selgitab, kuidas konfigureerida ühendust nii, et elektrooniline arveldamine pääseks Microsofti saidile SharePoint.
author: dkalyuzh
ms.date: 12/15/2021
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
ms.openlocfilehash: 6b9fffc1f3525e69792517dd1c6ebdcfbe5a74d2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371862"
---
# <a name="configure-a-sharepoint-connection"></a>SharePoint Ühenduse konfigureerimine

[!include [banner](../includes/banner.md)]

Elektroonilise arveldamise teenus saab lugeda Microsofti kaustadest faile SharePoint ja laadida faile üles SharePoint. Tagamaks, et elektroonilisel arveldamisel on juurdepääs SharePoint konkreetsele saidile, peate andma saidi mandaadid elektroonilise arvelduse teenusele. Lisaks, kindlustamaks, et mandaadid on turvaliselt talletatud, ärge neid otse esitage. Selle asemel ladustage need Azure'i võtme hoidlasse ja sisestage Azure'i võtme hoidla saladus.

## <a name="grant-access-to-a-sharepoint-folder"></a>Anna juurdepääs kaustale SharePoint

1. Looge rakenduse registreerimine rentnikus, kuhu on installitud Regulatory Configuration Service (RCS).

    1. Logige sisse [Azure’i portaali](https://portal.azure.com/).
    2. Avage rakenduse **registreerimised**.
    3. Valige **Uus registreerimine**.
    4. Sisestage nimi, nt **SharePoint Elektroonilise arvelduse rakendus**, ja lõpetage registreerimine
    5. Valige uus rakenduse registreerimine.
    6. Lubage vahekaardil **Autentimine** suvand Luba avaliku **kliendi voogu**.
    4. Vahekaardil Tunnistused **> saladused** valige suvand Uus **kliendi saladus** kliendisaladuse loomiseks.
    5. Kopeerige loodud saladuse väärtus.

    Järgige neid juhiseid:

    - Ärge kasutage sama rakenduse registreerimist erinevate teenuste jaoks.
    - Järgige paroolipoliitika [soovitusi](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Saate seadistada paroolide pöörete arvu. Rotatsiooni ajal looge rakenduse registreerimiseks uus kliendisaladus, uuendage võtme hoidla ja seejärel kustutage vana saladus.

2. Salvestage **rakenduse registreerimise saladus** ja **rakenduse (kliendi) ID** väärtused kahe uue salana võtme vaultis elektroonilise arveldamise keskkonna seadistuses.
3. Lisage RCS-i elektroonilise arvelduskeskkonna seadistuses võtme vaultparameetritele loodud saladusi.
4. Azure'i portaalis andke juurdepääs rakendusele SharePoint. Selle sammu peab läbima rentniku administraator.

    1. Valige rakenduse registreerimine, mille lõite.
    2. **Vahekaardil API õigused** valige suvand **Lisa õigus**.
    3. Valige **Microsofti graafiku (rakenduse õigused) saidid.Valitud** \> **·**.
    4. Valige **hüvitise administraatori nõustumine.\<user&nbsp;name\>**
    5. Vaadake üle **olekuväli**, et veenduda õiguste andmises.

        ![Api lubade vahekaardil antud load.](media/configured-permissions.jpg)

    6. Avage [Graph Explorer – Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) ja logige sisse.
    7. Valige vasakul paanil näidispäringute vahekaardil Sites (**Saidid)** **SharePoint suvand Hangi** sait saidi suhtelisel teel põhinevalt **.SharePoint**
    8. Sisestage hostinime **\{ja\}** serveri **\{suhtelise tee parameetrid \}**. Näiteks sisestage hostinimi `<domain>.sharepoint.com`**\{ja serveri \}**`sites/<siteName>`**\{suhteline tee \}**.

        > [!NOTE]
        > Vaike veebisaidi puhul jätke serveri suhtelise **\{tee parameeter\}** tühjaks.

    9. Valige **käivitamispäring** ja salvestage tulemus.
    10. Konfigureerige järgmine päring.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Selles päringus **\{on saidi-ID\}** eelmise **päringu vastuse ID-sõlme** väärtus.

        Siin on taotluse keha.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        Selles taotluse kehas **\{on rakenduse ID\}** rakenduse **(kliendi) ID** väärtus ja **\{rakenduse\}** nimi on **rakenduse nime** väärtus.

        ![SISESTA päring.](media/app-id-query.jpg)

    11. Vahekaardil Õiguste **muutmine valige ava õiguste** paneel ja seejärel **valige** Sites.FullControl.All **·** \> **·**\> Consent.**·**
    12. Valige **Käivita päring**.

Elektroonilise arveldamise teenusel on nüüd juurdepääs teie saidile SharePoint.
