---
title: 'Installida ja konfigureerida Microsoft Dynamics 365 toimingute & #8211; Ladustamine'
description: Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 toiminguteks - lao.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installida ja konfigureerida Microsoft Dynamics 365 toimingute & #8211; Ladustamine

Selles teemas kirjeldatakse, kuidas installida ja konfigureerida Microsoft Dynamics 365 toiminguteks - lao.

Dynamics 365 toiminguteks - ladustamine on rakendus saadaval Google Play Store ja Windows Store. Praeguse versiooni Microsoft Dynamics 365 toiminguteks, see rakendus on saadaval autonoomne komponent, mis tähendab enese juurutamine seadmeid kasutada lao ülesanded. Kasutada rakendust Dynamics 365 tegevuse keskkond, peate igas seadmes rakenduse alla laadida ja seadistada oma Dynamics 365 tegevuse keskkonna loomiseks. Selles teemas kirjeldatakse installige rakendus oma seadmes. Lisaks selgitatakse, kuidas konfigureerida rakendus teie Dynamics 365 tegevuse keskkonna loomiseks.

## <a name="prerequisites"></a>Eeltingimused
Rakendus on saadaval Android ja Windows operatsioonisüsteemides. Selle rakenduse kasutamiseks peab teil olema üks järgmistest toetatud operatsioonisüsteemide seadmetesse installitud. Teil olema ka üks järgmistest toetatud versioonide Dynamics 365 toiminguteks. Juulil teabe abil hinnata, kas teie riistvara ja tarkvara keskkonnas on valmis toetama paigaldamine.

| Platvorm                    | Versioon                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (kõik versioonid)                                                                                                                                                   |
| Dynamics 365 toiminguteks | Värskendus Microsoft Dynamics 365 versioon 1611 - või - Microsoft Dynamics Dynamics AX versioon 7.0/7.0.1 ja Microsoft Dynamics AX platvormile 2 käigultparanduste KB 3210014 |

## <a name="get-the-app"></a>Hankige rakendus
-   Windows (UWP) - [Dynamics 365 toiminguteks - ladustamine Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 toiminguteks - lao Google Play pood](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Luua veebirakenduse teenuse Active Directory
Suhelda teatud Dynamics 365 toimingute server rakenduse lubamiseks peate registreerima web Teenuserakenduse Azure Active Directory'is Dynamics 365 toimingute üürnikule. Turvalisuse huvides soovitame luua web teenuserakenduse iga seadmega, mida kasutada. Luua veebirakenduse teenust Azure Active Directory (Azure AD), tehke järgmist:

1.  Minge veebibrauseris, <https://manage.windowsazure.com>.
2.  Sisestage nimi ja parool kasutajale, kellel on juurdepääs Azure'i abonementide.
3.  Azure'i portaal Vasakpoolsel navigeerimispaanil, klõpsake **Active Directory**. [](./media/wh-01-active-directory-example.png)[![wh-01-aktiivne-kataloog-näide](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Võrku, valige Active Directory eksemplari, mis kasutab Dynamics 365 toiminguteks.
5.  Top tööriistaribal klõpsake **rakenduste**. [![wh-02-aktiivne-kataloog-rakendused](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Alumisel paanil klõpsake **lisa**. Selle **taotluse lisada** viisard käivitub.
7.  Sisestage nimi rakendus ja valige **veebirakendus ja/või web API**. [![wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Sisestage sisselogimise URL, mis on rakenduse URL oma rentniku just toimingute URL. Sisselogimise URL praegu mitte aktiivselt kasutatakse manifestidest rakenduse, kuid on kohustuslik väli. Sisestage rakenduse ID URI väljal sama URL. [![wh-04-ad-lisa-atribuudid](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Mine ning **konfigureerimine** vahekaart. [![wh-05-ad-konfigureerida-rakendus](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Kerige alla, kuni näete selle **õigusi teistele rakendustele** lõik. Klõpsake **taotluse lisada**. [![wh-06-ad-app-Add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Valige **Microsoft Dynamics ERP** loendis. Klõpsake selle **lõpule viia sisse** nuppu lehe paremas nurgas. [![wh-07-ad-Vali-õigused](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Aastal ning **Delegaadi õigused** valige kõik märkeruudud. Click **Save**. [![wh-08-ad-Delegaadi-õigused](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Märkige üles järgmised andmed:
    -   **Kliendi ID** - liikudes üles lehele, näed **kliendi ID** kuvada.
    -   **Võti** - aga ka **võtmed** jagu, võtme loomiseks valige kestus ja koopia võti. See võti hiljem viidatakse kui ka **klient saladus**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Looge ja konfigureerige kasutajakonto Dynamics 365 toiminguteks
Toiminguteks kasutada Azure AD rakendus Dynamics 365 lubamiseks peate täitma konfiguratsioon järgmist:

1.  Uue kasutajakonto loomine Azure Active Directory'is Dynamics 365 toimingute üürnikule. Selle kasutajakonto eesmärk on konkreetne kohandatud teenusega tolliladustamise app, mis paljastab Dynamics 365 toimingute server. Pärast selle sammu, peate WMDP kasutaja mandaati, mis koosnevad WMDP e-posti aadressi ja salasõna WMDP. Üldised juhised Azure AD kasutajate lisamine õppida ja Dynamics 365 korral viidata õpetamisel: [Microsoft Dynamics 365 toimingute liitumisleping, registreeru](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Luua Dynamics 365 toimingute kasutaja, mis vastab tolliladustamise rakenduse kasutaja mandaati.
    1.  Dynamics 365 toiminguteks, minge **süsteemi halduse**&gt;**levinud**&gt;**kasutajate**.
    2.  Uue kasutajakonto loomiseks.
    3.  Määrata lao mobiilseade kasutaja, nagu järgmine pilt. [![wh-09-Add-User-Security-Role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Rakenduse Azure Active Directory'is seostada tolliladustamise rakenduse kasutaja.
    1.  Dynamics 365 toiminguteks, minge **süsteemi halduse**&gt;**install**&gt;**Azure Active Directory rakenduste**.
    2.  Looge uus rida.
    3.  Sisestage selle **kliendi ID** (saadud viimases osas), talle nimi ja valige varem loodud kasutaja. Soovitame, et sa saaksid kergesti eemaldada juurdepääsu Dynamics 365 operatsioonide sellelt lehelt ei kadunud tag kõigis seadmetes. [![wh-10-ad-rakendused-vormi](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigureerige rakenduse
Seadme Dynamics 365 toimingute server kasutades Azure AD ühenduse loomiseks tuleb konfigureerida rakendus. Selleks tehke järgmist.

1.  Minge rakenduses **sätted**.
2.  Selge on **Demo režiimis** välja. [![wh-11-app-Connection-Settings-Demo-Mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Sisestage järgmine teave:- **Azure Active directory kliendi ID** -ID kliendile juhises 13 "Active Directory teenuse veebirakenduse loomine". - **Azure Active directory kliendi saladus** -klient saladus on saadud "Create web teenuserakenduse Active Directory" samm 13. - **Azure Active directory ressursside** -Azure AD directory ressursile kujutab Dynamics 365 toimingute root URL. **Märkus**: Ärge katkestage väli märgiga kaldkriips (/). - **Azure Active directory rentniku** -Azure AD directory üürnikule kasutada Dynamics 365 toimingute server: https://login.windows.net/&lt;oma-AD-rentniku-ID&gt;. Näiteks: https://login.windows.net/contosooperations.onmicrosoft.com. **Märkus**: Ärge katkestage väli märgiga kaldkriips (/). - **Ettevõtte** -sisestage juriidilise Dynamics 365 rakendus ühenduse loomiseks soovitud toiminguid. [![wh-12-app-ühendus-seaded](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valige selle **tagasi** nuppu vasakus nurgas taotluse. Rakendus loob nüüd ühenduse teie Dynamics 365 toimingute server ja kuvatakse laotöötaja sisselogimine. [![wh-13-sisselogimine](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Juurdepääsu seadme eemaldamine
Kaotatud või rikutud seadme puhul peate eemaldama Dynamics 365 taotleda tegevustele seadme. Järgnevalt kirjeldatakse soovitatav protsessi juurdepääsu.

1.  Dynamics 365 toiminguteks, minge **süsteemi halduse**&gt;**install**&gt;**Azure Active Directory rakenduste**.
2.  Kas kustutada rida, mis vastab seade, millele soovite juurdepääsu. Pange kirja ka **kliendi ID** eemaldatud seadme jaoks kasutada.
3.  Logi sisse Azure'i klassikaline portaali aadressil <https://manage.windowsazure.com>.
4.  Klõpsake selle **Active Directory** ikooni vasakpoolsest menüüst, ja seejärel klõpsake soovitud kataloogi.
5.  Klõpsake menüü top **rakenduste**, ja seejärel klõpsake soovitud konfigureerimise programm. Selle **Quick Start** kuvatakse ühekordse sisselogimise ja muu konfiguratsiooniteabe.
6.  Klõpsake selle **konfigureerimine** sakk, liikuge allapoole ja tagada, et selle **kliendi ID** taotluse on sama nagu samm 2 käesolevas paragrahvis.
7.  Klõpsake selle **kustutada** nuppu käsuriba.
8.  Klõpsake **Jah** kinnituse sõnumi.



