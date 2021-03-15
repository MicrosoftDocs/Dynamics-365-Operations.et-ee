---
title: Laorakenduse installimine ja ühendamine
description: Selles teemas selgitatakse, kuidas installida laorakendust kõigisse mobiilsetesse seadmetesse ja konfigureerida see keskkonnaga Microsoft Dynamics 365 Supply Chain Management ühenduse loomiseks. Saate konfigureerida kõik seadmed käsitsi, importida ühenduse sätted faili kaudu või skannides QR-koodi.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 411a97427bbb16388e0f60b8ecb5dd3e5a79e87e
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142271"
---
# <a name="install-and-connect-the-warehouse-app"></a>Laorakenduse installimine ja ühendamine

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Selles teemas kirjeldatakse, kuidas konfigureerida vana laorakendust. Kui otsite teavet selle kohta, kuidas konfigureerida uut laohalduse mobiilirakendust (praegu avaliku eelversioonina), vaadake jaotisest [Laohalduse mobiilirakenduse installimine ja ühendamine](install-configure-warehouse-management-app.md).

> [!NOTE]
> Selles teemas kirjeldatakse, kuidas pilvejuurutuse korral konfigureerida laorakendust. Kui soovite teavet asutusesiseste juurutamiste laorakenduse konfigureerimise kohta, vt [Kohapealsete juurutuste ladustamine](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Laorakendus on saadaval Google Play poes ja Microsoft Store'is. See on saadaval eraldiseisva komponendina. Seetõttu peate selle igasse seadmesse eraldi alla laadima ja seejärel konfigureerima selle keskkonnaga Microsoft Dynamics 365 Supply Chain Management ühenduse loomiseks.

Selles teemas selgitatakse, kuidas installida laorakendust kõigisse mobiilsetesse seadmetesse ja konfigureerida see keskkonnaga Supply Chain Management ühenduse loomiseks. Saate konfigureerida kõik seadmed käsitsi, importida ühenduse sätted faili kaudu või skannides QR-koodi.

## <a name="system-requirements"></a>Süsteeminõuded

Laorakendus on saadaval nii Windowsi kui ka Androidi operatsioonisüsteemides. Rakenduse uusima versiooni kasutamiseks peab teie mobiilsesse seadmetesse olema installitud üks järgmistest operatsioonisüsteemidest.

- Windows 10 (Universaalne Windowsi platvorm \[UWP\]) Fall Creators Update 1709 (versioonijärk 10.0.16299) või uuem
- Android 4.4 või uuem

> [!NOTE]
> Kui peate toetama vanemaid Windowsi seadmeid, mis ei saa käitada Windowsi uusimat versiooni, saate siiski Microsoft Store'ist laorakenduse versiooni 1.6.3.0 alla laadida. See versioon töötab Windows 10 (UWP) novembri värskendusega 1511 (versioonijärk 10.0.10586) või uuemaga. Pidage siiski meeles, et see laorakenduse versioon ei toeta ühenduse sätete hulgijuurutamist. Seetõttu peate [konfigureerima ühenduse käsitsi](#config-manually) kõigis seadmeis, mis käitavad rakenduse seda versiooni.

## <a name="get-the-warehouse-app"></a>Laorakenduse hankimine

Rakenduse allalaadimiseks saate kasutada ühte järgmistest linkidest.

- **Windows (UWP):** [Dynamics 365 for Finance and Operations – ladustamine Microsoft Store'is](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Warehousing – Dynamics 365 Google Play poes](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Väiksemate juurutuste puhul võite installida rakenduse iga seadme vastavast poest ja seejärel konfigureerida käsitsi ühenduse keskkondadega, mida kasutate. Kuid laorakenduse versiooni 1.7.0.0 ja uuema puhul saate rakenduse juurutamist ja/või konfigureerimist automatiseerida. See lähenemisviis võib olla mugav, kui haldate paljusid seadmeid ja kasutate mõnda mobiilse seadme halduse ja mobiilirakenduse halduse lahendust, näiteks [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune). Lisateavet selle kohta, kuidas kasutada Intune'i rakenduste lisamiseks, vaadake teemast [Rakenduste lisamine Microsoft Intune'i](https://docs.microsoft.com/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Veebiteenuse rakenduse loomine Azure Active Directorys

Selleks et laorakendus saaks konkreetse Supply Chain Managementi serveriga suhelda, tuleb registreerida veebiteenuse rakendus Azure Active Directorys (Azure AD) Supply Chain Managementi rentnikule. Järgnevalt toodud protseduur on üks viis selle ülesande lõpule viimiseks. Muude võimaluste kohta üksikasjaliku teabe saamiseks, vaadake sellele protseduurile järgnevaid linke.

1. Minge brauseris lehele [https://portal.azure.com](https://portal.azure.com/).
1. Sisestage selle kasutaja nimi ja parool, kellel on juurdepääs Azure’i tellimusele.
1. Valige Azure’i portaalis vasakpoolsel navigeerimispaanil valiku **Azure Active Directory**.

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. Veenduge, et töötate Azure AD eksemplariga, mida kasutab Supply Chain Management.
1. Klõpsake loendis **Haldamine** suvandit **Rakenduste registreerimised**.

    ![Rakenduste registreerimised](media/app-connect-azure-register.png "Rakenduste registreerimised")

1. Valige tööriistaribal **Uus registreerimine** viisardi **Rakenduse registreerimine** avamiseks.
1. Sisestage rakenduse nimi ja valige suvand **Ainult selle organisatsioonikataloogi kontod** ja valige **Registreeri**.

    ![Rakenduse viisardi registreerimine](media/app-connect-azure-register-wizard.png "Rakenduse viisardi registreerimine")

1. Avaneb teie uue rakenduse registreerimisaken. Märkige välja **Rakenduse (klient) ID** väärtus üles, seda läheb hiljem vaja. Sellele ID-le on selles teemas hiljem viidatud kui *kliendi ID*.

    ![Rakenduse (klient) ID](media/app-connect-azure-app-id.png "Rakenduse (klient) ID")

1. Valige loendist **Haldamine** suvand **Serdid ja saladused**. Seejärel valige üks järgmistest nuppudest, sõltuvalt sellest, kuidas soovite rakendust autentimiseks konfigureerida. (Lisateabe saamiseks vaadake jaotist [Serdi või kliendi saladuse abil autentimine](#authenticate) selles teemas hiljem.)

    - **Serdi üleslaadimine** – laadige üles sert saladusena kasutatamiseks. Soovitame selle lähenemisviisi kasutamist, sest see on turvalisem ja seda saab täielikumalt automatiseerida. Kui käitate laorakendust Windowsi seadmetes, märkige üles väärtus **Sõrmejälg**, mida kuvatakse pärast serdi üleslaadimist. Vajate seda väärtust Windowsi seadmetes serdi konfigureerimisel.
    - **Uus kliendi saladus** – looge võti, sisestades võtme kirjeldus ja kestus jaotises **Paroolid** ning seejärel valige **Lisa**. Tehke võtmest koopia ja talletage see turvaliselt.

    ![Serdid ja saladused](media/app-connect-azure-authentication.png "Serdid ja saladused")

Lisateavet Azure AD-s veebiteenuse rakenduste seadistamise kohta leiate järgmistest allikatest.

- Juhiste saamiseks selle kohta, kuidas kasutada Windows PowerShelli veebiteenuse rakenduste seadistamiseks Azure AD-s, vaadake teemat [Kuidas: teenusesubjekti loomine serdiga Azure PowerShelli abil](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Üksikasjaliku teabe saamiseks, kuidas Azure AD-s käsitsi veebiteenuse rakendust luua, vaadake järgmisi teemasid.

    - [Lühijuhend: rakenduse registreerimine Microsofti identiteedi platvormiga](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Kuidas: portaali abil Azure AD rakenduse ja ressurssidele juurde pääseva teenusesubjekti loomine](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Supply Chain Managementis kasutajakonto loomine ja konfigureerimine

Supply Chain Managementi lubamiseks, et kasutada Azure AD rakendust, toimige järgmiselt.

1. Looge laorakenduse kasutaja identimisteabele vastav kasutaja.

    1. Avage Supply Chain Managementis **Süsteemihaldus \> Kasutajad \> Kasutajad**.
    1. Looge kasutaja.
    1. Määrake ladustamise mobiilse seadme kasutaja.

    ![Ladustamise mobiilse seadme kasutaja määramine](media/app-connect-app-users.png "Ladustamise mobiilse seadme kasutaja määramine")

1. Seostage oma Azure AD rakendus laorakenduse kasutajaga.

    1. Minge jaotisse **Süsteemihaldus \> Seadistus \> Azure Active Directory rakendused**.
    1. Looge rida.
    1. Sisestage kliendi ID, mille märkisite üles eelmises jaotises, pange sellele nimi ja valige äsja loodud kasutaja. Soovitame teil sildistada kõik oma seadmed. Sellisel juhul saate seadme kaotamise korral selle lehe kaudu hõlpsalt eemaldada nende Supply Chain Managementi juurdepääsu.

    ![Azure Active Directory rakendused](media/app-connect-aad-apps.png "Azure Active Directory avaldused")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Autentimine serdi või kliendi saladuse abil

Azure AD-ga autentimine pakub turvalist viisi mobiilse seadme ühendamiseks Supply Chain Managementiga. Saate autentida nii serdi kui ka kliendi saladuse abil. Kui impordite ühenduse sätteid, soovitame kliendi saladuse asemel kasutada serti. Kuna kliendi saladus peab olema alati turvaliselt talletatud, ei saa te seda ühenduse sätete failist või QR-koodist importida, nagu selles teemas hiljem kirjeldatakse.

Serte saab kasutada saladusena rakenduse identiteedi tõestamisel, kui luba taotletakse. Serdi avalik osa laaditakse üles rakenduse registreerimiseks Azure'i portaalis, kuid täielik sert tuleb juurutada igasse seadmesse, kuhu on installitud laorakendus. Teie organisatsioon vastutab serdi haldamise eest roteerimise ja muus osas. Teil on võimalik kasutada enda allkirjastatud serte, kuid te peaksite alati kasutama mitte-eksporditavaid serte.

Peate tegema serdi kohalikult kättesaadavaks igas seadmes, kus käitate laorakendust. Lisateavet selle kohta, kuidas hallata Intune'i juhitavate seadmete serte Intune'i kasutamise korral, vaadake teemast [Sertide kasutamine Microsoft Intune'is autentimiseks](https://docs.microsoft.com/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Rakenduse konfigureerimine ühenduse sätete importimise abil

Rakenduse haldamise lihtsustamiseks ja selle juurutamiseks mitmes mobiilses seadmes, saate importida ühenduse sätted selle asemel, et neid igas seadmes käsitsi sisestada. Selles jaotises selgitatakse, kuidas neid sätteid luua ja importida.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Ühenduse sätete faili või QR-koodi loomine

Ühenduse sätteid saate importida failist või QR-koodist. Mõlema lähenemisviisi puhul peate esmalt looma sätete faili, mis kasutab vormingut JavaScript Object Notation (JSON) ja selle süntaksit. See fail peab sisaldama ühenduse loendit, mis sisaldab individuaalseid ühendusi, mida peab lisama. Järgmises tabelis võetakse kokku parameetrid, mida peate ühenduse sätete failis määrama.

| Parameeter | Kirjeldus |
| --- | --- |
| ConnectionName | Määrake ühenduse sätte nimi. Maksimaalne märkide arv on 20. Kuna see väärtus on ühenduse sätte kordumatu identifikaator, veenduge, et see oleks loendis kordumatu. Kui seadmes on sama nimega ühendus juba olemas, alistatakse see imporditud faili sätetega. |
| ActiveDirectoryClientAppId | Määrake kliendi ID, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service). |
| ActiveDirectoryResource | Määrake Supply Chain Managementi juur-URL. |
| ActiveDirectoryTenant | Määrake Azure AD rentnik, mida kasutate Supply Chain Managementi serveriga. Sellel väärtusel on vorm `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Näite leiate siit: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
| Ettevõte | Määrake Supply Chain Managementis juriidiline isik, millega soovite rakenduse ühendada. |
| ConnectionType | (Valikuline) Määrake, kas ühenduse säte peaks keskkonnaga ühenduse loomiseks kasutama serti või kliendi saladust. Kehtivad väärtused on *„sert”* ja *„kliendisaladus”*. Vaikeväärtus on *„sert”*.<p>**Märkus:** kliendi saladusi ei saa importida.</p> |
| IsEditable | (Valikuline) Määrake, kas rakenduse kasutaja saab ühenduse sätteid redigeerida. Kehtivad väärtused on *„tõene”* ja *„väär”*. Vaikeväärtus on *„tõene”*. |
| IsDefault | (Valikuline) Määrake, kas see ühendus on vaikeühendus. Vaikeühenduseks määratud ühendus on automaatselt eelvalitud rakenduse avamisel. Vaikeühenduseks saab määrata ainult ühe ühenduse. Kehtivad väärtused on *„tõene”* ja *„väär”*. Vaikeväärtus on *„väär”*. |
| CertificateThumbprint | (Valikuline) Windowsi seadmete puhul saate määrata ühenduse jaoks serdi sõrmejälje. Androidi seadmete puhul peab rakenduse kasutaja valima serdi ühenduse esmakordsel kasutamisel. |

Järgmises näites kuvatakse kehtivat ühenduse sätete faili, mis sisaldab kahte ühendust. Nagu näete, on ühenduse loend (failis nimega *„ConnectionList”*) objekt, millel on massiiv, mis talletab iga ühenduse objektina. Iga objekt peab olema looksulgude vahel ({}) ja eraldatud komadega ning massiiv peab olema nurksulgudes (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Saate salvestada teabe JSON-failina või luua QR-koodi, millel on sama sisu. Kui salvestate teabe failina, soovitame kasutada selle salvestamiseks vaikenime *connections.json*, eriti kui salvestate selle igas mobiilses seadmes vaikeasukohta.

### <a name="save-the-connection-settings-file-on-each-device"></a>Ühenduse sätete faili salvestamine igasse seadmsesse

Tavaliselt kasutate ühenduse sätete failide jaotamiseks kõigisse oma hallatavatesse seadmetesse seadme haldustööriista või skripti. Kui kasutate ühenduse sätete faili salvestamisel kõigis seadmeis selle vaikenime ja -asukohta, impordib laorakendus selle automaatselt ka esmakordsel käitamisel pärast rakenduse installimist. Kui kasutate faili jaoks kohandatud nime või asukohta, peab rakenduse kasutaja määrama väärtused esmakordsel käitamisel. Kuid rakendus jätkab edaspidi määratud nime ja asukoha kasutamist.

Rakenduse käivitamisel impordib see ühenduse sätted iga kord uuesti nende eelmisest asukohast, et teha kindlaks, kas on tehtud muudatusi. Rakendus värskendab ainult neid ühendusi, millel on ühenduse sätete failis olevate ühendustega samad nimed. Kasutaja loodud ühendusi, mis kasutavad teisi nimesid, ei värskendata.

Ühenduse sätete faili abil ei saa ühendust eemaldada.

Nagu eelnevalt mainitud, on vaikefaili nimi *connections.json*. Faili vaikeasukoht sõltub sellest, kas kasutate Windowsi või Androidi seadet.

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Tavaliselt luuakse teed automaatselt rakenduse esmakordsel käivitamisel. Kuid saate need käsitsi luua, kui peate enne installimist ühenduse sätete faili seadmesse üle kandma.

> [!NOTE]
> Rakenduse desinstallimisel eemaldatakse vaiketee ja selle sisu.

### <a name="import-the-connection-settings"></a>Ühenduse sätete importimine

Järgige neid juhiseid ühenduse sätete importimiseks failist või QR-koodist.

1. Avage laoakendus oma mobiilses seadmes.
1. Avage jaotis **Ühenduse sätted**.
1. Valige suvandi **Kasuta demorežiimi** sätteks _Ei_.

    ![Suvand Kasuta demorežiimi](media/app-connect-app-demo-mode.png "Suvand Kasuta demorežiimi")

1. Valige suvand **Vali fail** või **Skanni QR-kood**, sõltuvalt sellest, kuidas soovite sätteid importida.

    - Kui impordite ühenduse sätted failist, on rakendus võib-olla juba faili leidnud, kui selle salvestamisel kasutati vaikenime ja -asukohta. Muul juhul valige **Vali fail**, sirvige oma kohalikus seadmes failini ja valige see. Kui valite kohandatud asukoha, talletab rakendus selle ja kasutab seda automaatselt järgmisel korral.
    - Kui impordite ühenduse sätted QR-koodi skannimise abil, valige **Skanni QR-kood**. Rakendus küsib teilt luba seadme kaamera kasutamiseks. Pärast loa andmist käivitatakse kaamera, et saaksite kasutada seda skannimiseks. Olenevalt seadme kaamera kvaliteedist ja QR-koodi keerukusest, võib teil olla raske saada korralikku skanni. Sel juhul proovige QR-koodi keerukust vähendada, luues ainult ühe ühenduse QR-koodi kohta. (Praegu saate QR-koodi skannimiseks kasutada ainult seadme kaamerat.)

    ![Ühenduse sätete importimine](media/app-connect-app-select-file.png "Ühenduse sätete importimine")

1. Kui ühenduse sätted on edukalt laaditud, valige lehe vasakus ülanurgas nupp **Tagasi** (vasaknool).

    ![Ühenduse sätted laaditud](media/app-connect-app-settings-loaded.png "Ühenduse sätted laaditud")

1. Kui kasutate Androidi seadet ja kasutate autentimisel serti, palub seade teil serdi valida.

    ![Serdi valimise viip Android seadmes](media/app-connect-app-choose-cert.png "Serdi valimise viip Android seadmes")

1. Rakendus loob ühenduse teie Supply Chain Managementi serveriga ja kuvab sisselogimise lehe.

    ![Sisselogimise leht](media/app-connect-sign-in.png "Sisselogimise leht")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Rakenduse käsitsi konfigureerimine

Saate käsitsi konfigureerida rakenduse seadmel Supply Chain Managementi serveriga rakenduse Azure AD kaudu ühenduse loomiseks.

1. Avage laoakendus oma mobiilses seadmes.
1. Avage jaotis **Ühenduse sätted**.
1. Valige suvandi **Kasuta demorežiimi** sätteks _Ei_.

    ![Demorežiim on välja lülitatud](media/app-connect-app-select-file.png "Demorežiim on välja lülitatud")

1. Puudutage välja **Ühenduse valimine**, et laiendada ühenduse üksikasjade käsitsi sisestamiseks nõutavaid sätteid.

    ![Käsitsi ühendamise väljad](media/app-connect-manual-connect.png "Käsitsi ühendamise väljad")

1. Sisestage järgmine teave:

    - **Kliendi saladuse kasutamine** – määrake selle suvandi väärtusekd _Jah_, et kasutada kliendi saladust Supply Chain Managementiga autentimiseks. Autentimisel serdi kasutamiseks määrake selle väärtuseks _Ei_. (Lugege lisateavet teemast [Veebiteenuse rakenduse loomine rakenduses Azure Active Directory](#create-service) .)
    - **Ühenduse nimi** – sisestage uue ühenduse nimi. See nimi kuvatakse väljal **Ühenduse valimine** järgmisel korral, kui avate ühenduse sätted. Sisestatav nimi peab olema kordumatu. (Teisisõnu peab see erinema kõigist muudest teie seadmesse salvestatud ühenduse nimedest, kui sinna on talletatud teisi ühenduse nimesid.).
    - **Active Directory kliendi ID** – sisestage kliendi ID, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service).
    - **Active Directory kliendi saladus** – see väli on saadaval ainult siis, kui suvandi **Kkliendi saladuse kasutamine** väärtuseks on seatud _Jah_. Sisestage kliendi saladus, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service).
    - **Active Directory serdi sõrmejälg** – see väli on saadaval ainult Windowsi seadmete puhul, kui suvandi **Kkliendi saladuse kasutamine** väärtuseks on seatud _Ei_. Sisestage serdi sõrmejälg, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service).
    - **Active Directory ressurss** – määrake Supply Chain Managementi juur-URL.

        > [!NOTE]
        > Ärge lisage selle väärtuse lõppu kaldkriipsu (/).

    - **Azure Active directory rentnik** – sisestage Azure AD rentnik, mida kasutate Supply Chain Managementi serveri puhul. Sellel väärtusel on vorm `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Näite leiate siit: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Ärge lisage selle väärtuse lõppu kaldkriipsu (/).

    - **Ettevõte** – sisestage rakendusse Supply Chain Management juriidiline isik, millega soovite rakenduse ühendada.

1. Valige lehe ülemises parempoolses nurgas olev nupp **Salvesta**.
1. Kui kasutate Androidi seadet ja kasutate autentimisel serti, palub seade teil serdi valida.
1. Rakendus loob ühenduse teie Supply Chain Managementi serveriga ja kuvab sisselogimise lehe.

## <a name="remove-access-for-a-device"></a>Seadmelt juurdepääsu äravõtmine

Kaotatud või ohtu sattunud seadme puhul on vaja seadmelt juurdepääs Supply Chain Managementile ära võtta. Järgmised toimingud kirjeldavad juurdepääsu eemaldamise soovituslikku protsessi.

1. Minge jaotisse **Süsteemihaldus \> Seadistus \> Azure Active Directory rakendused**.
1. Kustutage rida, mis vastab seadmele, millelt soovite juurdepääsu ära võtta. Märkige üles eemaldatud seadme jaoks kasutatav kliendi ID, kuna vajate seda hiljem.

    Kui olete registreerinud ainult ühe kliendi ID ja mitu seadet kasutavad sama kliendi ID-d, tuleb teil nende seadmete jaoks uued ühenduse sätted luua. Vastasel juhul kaotavad need juurdepääsu.

1. Logige sisse Azure’i portaali lehel [https://portal.azure.com](https://portal.azure.com/).
1. Valige vasakpoolsel navigeerimispaanil **Active Directory** ja veenduge, et olete õiges kaustas.
1. Valige loendist **Haldamine** suvand **Rakenduste registreerimine** ja seejärel rakendus, mida soovite konfigureerida. Kuvatakse leht **Sätted** koos konfiguratsiooniteabega.
1. Veenduge, et rakenduse kliendi ID ühtib kliendi ID-ga, mille märkisite üles etapis 2.
1. Valige tööriistaribal **Kustuta**.
1. Valige kuvatavast kinnitusteatest **Jah**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]