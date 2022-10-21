---
title: Arve hõivamise lahenduse konfigureerimine
description: See artikkel selgitab arve hõivamise lahenduse konfigureerimist.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690975"
---
# <a name="configure-the-invoice-capture-solution"></a>Arve hõivamise lahenduse konfigureerimine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pärast arve hõivamise lahenduse installimist tuleb teil keskkond konfigureerida. Protsess koosneb järgmistest põhietappidest.

1. **Nõutav:** sünkroonige juriidilised isikud rakendusest Microsoft Dynamics 365 Finance. Seda sammu kasutatakse organisatsiooni struktuuri häälestamiseks Microsoft Power Platform.
2. **Nõutav:** konfigureerige arve piltide importimise kanalid. Lahendus toetab järgmisi kanaleid:

    - Office 365 Outlook (vaikimisi)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Valikuline:** määrake täiendavad konfiguratsioonigrupid optilise märgituvastuse (OCR) teenuse jaoks.
4. **Valikuline:** määrake juriidilise isiku, hankija konto, kauba ja hanke tüübi vastendamisreeglid.

See artikkel keskendub protsessi kahele nõutavale astmele. Lisateavet konfiguratsioonigruppide kohta vt arve hõivamise [lahenduse konfiguratsioonigruppidest](invoice-capture-config-group.md). Lisateavet vastendamisreeglite kohta vt arve hõivamise [lahenduse vastendamise reeglitest](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Juriidiliste isikute haldamine

Finants määratleb juriidilised isikud organisatsioonina, mis tuvastatakse juriidilistes isikutes registreerimise kaudu. Äritegevusi teostatakse ja kirjendatakse eraldi juriidilistes isikutes. Äriüksustes Microsoft Power Platform on turberollid ja kasutajad ühendatud rollipõhisele turvamudelile vastaval viisil.

Äriüksusi kasutatakse andmepääsu juhtimiseks koos turberollidega. Kasutajad näevad ainult teavet, mida nad vajavad oma tööde jaoks. Arve hõivamise lahendus pakub konfiguratsiooniruumi, kus saate laadida põhiteavet finantside olemasolevatelt juriidilistelt isikutelt ja hallata neid üksusi, mis luuakse käsitsi. Juriidilisi isikuid kasutatakse hankija arvetel ja turvalisuse kontrollis.

Kui loendivaates luuakse ja kuvatakse juriidiline isik, luuakse automaatselt sama nimega vaikeäriüksus. Meeskonnale antakse **AP-ametniku turberoll**. Kui juriidilised isikud on imporditud, imporditakse finantside põhiandmed. Olematud kaubad tuvastab juriidiline isik ja need lisatakse arve hõivamise lahendusele. Konfiguratsiooni vaikegrupp määratakse uutele juriidilistele isikutele.

### <a name="sync-legal-entities"></a>Sünkrooni juriidilised isikud

Te ei saa juriidiliseid isikuid otse luua. Kuid finantside kaudu saate juriidilisi isikuid sünkroonida. Juriidiliste isikute sünkroonimiseks järgige neid samme.

1. Avage häälestussüsteemi **\> häälestus \> juriidilise isiku haldamine**.
2. Valige **suvand Sünkrooni juriidilised** isikud ja seejärel valige **kinnituse** dialoogiboksis OK.

Pärast sünkroonimise lõpetamist kuvatakse uute juriidiliste isikute arv. Uued juriidilised isikud kuvatakse loendivaates. Konfiguratsiooni vaikegrupp määratakse uutele juriidilistele isikutele.

## <a name="configure-invoice-import-channels"></a>Arve importimise kanalite konfigureerimine

Hankijad saadavad arveid erinevatest kanalitest (meil, faili tööruum või arveportaal) erinevate vormingute (paber või pilt) kaudu. Arve hõivamise lahendus saab käsitleda erinevaid kanaleid ja vorminguid. Toetatakse järgmisi tüüpe:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Kui kindlale kontole luuakse kanal, luuakse eelmääratletud malliga automatiseeritud voog sissetulevate meilide või failide jälgimiseks sisendkausta või ruumi. Iga kehtiva arvega faili saab tuvastada ja saata arvealasse, et oodata ostureskontro (AP) ametniku töötlemist. Manus peab olema PDF- või pildivormingus. Arveid saab arvehõive lahendusse laadida vastavalt kanali konfiguratsioonile.

### <a name="create-a-channel"></a>Kanali loomine

Kui olete importinud täiendava lahendusepaketi (Dynamics 365 arve hõivamine – installitööriistad), Office 365 on Outlooki vaikeühendus kasutamiseks valmis. Kui soovite luua ühendusi erinevatele e-posti kontodele või muudele kanali tüüpidele, vaadake [teemat Kanalitele lisaühenduse loomine](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Kanali loomiseks järgige neid samme.

1. Minge süsteemi häälestuse **\> konfiguratsioonikanalitesse \>**.
2. Valige suvand **Uus**.
3. Seadistage järgmised väljad.

    - Kanali nimi
    - Kirjeldus
    - Tüüp
    - Ühendus

Lahendusse saab importida ainult järgmisi kriteeriumitele vastavad e-kirjad või failid.

| Tüüp               | Konfiguratsioon  | Lisateave |
|--------------------|----------------|------------------|
| Office 365 Outlook | Kaust         | E-posti kaust peab olema juurkaustas. Vaikimisi kasutatakse kausta Sisse. Alamkausta ei toetata. |
|                    | Teema filter | (Valikuline) Alamring, mis tuleks teemasse kaasata. |
|                    | Lähtekoht           | (Valikuline) Saatja või saatja meiliaadress. Kui määrate mitu aadressi, kasutage semikoolonit (;) eraldajana. |
| SharePoint         | Saidi aadress   | Saidi aadressi URL. |
|                    | Kaust         | Kaust saidi aadressis. |

### <a name="activate-the-channel"></a>Kanali aktiveerimine

Voo salvestamisel kuvatakse väljadel kanali olek ja loomise kellaaeg. Algselt on välja **Olek** väärtuseks seatud **Passiivne**. Oleku **põhjuse väli** näitab, et kanal on käivitatud ja aktiveerimiseks valmis.

Kanali aktiveerimiseks valige **Aktiveeri**. Värskendatakse **oleku** **ja oleku** põhjuse väljad.

Kui kanal pole nõutav, saate selle desaktiveerida. Kanali desaktiveerimiseks valige desaktiveerige **.** Värskendatakse **oleku** **ja oleku** põhjuse väljad.

### <a name="manage-flows-in-flow-management"></a>Voohalduse voogude haldamine

Kanalit saate vaadata konfiguratsioonikanalite **lehel** või voohalduses.

Üksikasjade vaatamiseks minge haldussüsteemi vaikelahenduse **\> pilve \> voogudesse** ja valige sihtvoog. Kuvatavad üksikasjad hõlmavad seotud ühendusi, omanikku ja käitusajalooid.

Oleku sünkroonimiseks valige suvand **Kontrolli**, et kinnitada, et kanali olek vastab voo olekule.

Mõned erandite käsitsemise juhtumid kuvatakse väljal **Oleku põhjus**:

- **Ühendus Dataverse puudub** – praegune kasutaja ei ole loonud vähemalt ühte ühenduse **Microsoft Dataverse** viidet.
- **Ei leitud** – kanaliga lingitud voog on voohalduses kustutatud. Uue kanali loomiseks tuleb kanal uuesti salvestada.
- **Inaktiveeritud voohalduses** – voog on voohalduses inaktiveeritud ja kanali olek erineb voo olekust.
- **Aktiveeritud voohalduses** – voog on voohalduses aktiveeritud ja kanali olek erineb voo olekust.
- **Ilmnes ootamatu tõrge** – kasutaja peab kinnitama, et sait on sidesaidiks ja et see kaust on dokumenditeek.
