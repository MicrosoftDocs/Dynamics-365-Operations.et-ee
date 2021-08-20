---
title: Laohalduse mobiilirakenduse installimine ja ühendamine
description: Selles teemas selgitatakse, kuidas installida laohalduse mobiilirakendust kõigisse mobiilsetesse seadmetesse ja konfigureerida see keskkonnaga Microsoft Dynamics 365 Supply Chain Management ühenduse loomiseks.
author: MarkusFogelberg
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 338c3129d81fa0428f3470808bc13fc76483ff3aaf19b06708a986aec64b4030
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782343"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Laohalduse mobiilirakenduse installimine ja ühendamine

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Selles teemas selgitatakse, kuidas konfigureerida uut laohalduse mobiilirakendust. Kui otsite teavet vana laorakenduse (iganenud nüüdseks) konfigureerimise kohta, vt [Laorakenduse installimine ja ühendamine](../../supply-chain/warehousing/install-configure-warehousing-app.md).

Selles teemas selgitatakse, kuidas alla laadida ja installida laohalduse mobiilirakendust teie kõigisse mobiilsetesse seadmetesse ja konfigureerida seda keskkonnaga Supply Chain Management ühenduse loomiseks. Saate konfigureerida kõik seadmed käsitsi, importida ühenduse sätted faili kaudu või skannides QR-koodi.

## <a name="system-requirements"></a>Süsteeminõuded

Laohalduse mobiilirakendus on saadaval nii Windowsi kui ka Google’i Androidi operatsioonisüsteemide jaoks. Rakenduse kasutamiseks peab teie mobiiliseadmetesse olema installitud järgmine operatsioonisüsteem.

- Windows 10 (Universaalne Windowsi platvorm \[UWP\]) 2018. a oktoobri värskendus 1809 (versioonijärk 10.0.17763) või uuem
- Android 4.4 või uuem

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Enne rakenduse kasutamist peate seotud funktsiooni oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *uue laorakenduse kasutajasätted, ikoonid ja etapi pealkirjad*

## <a name="get-the-warehouse-management-mobile-app"></a>Laohalduse mobiilirakenduse hankimine

Väiksemate juurutuste puhul võite installida rakenduse igasse seadmesse sobivast poest ja seejärel konfigureerida käsitsi ühenduse nende keskkondadega, mida kasutate.

Suurema juurutamise puhul saate automatiseerida rakenduse juurutamise ja/või konfiguratsiooni, mis on mugavam juhul, kui haldate mitmeid seadmeid. Näiteks võite kasutada mobiilse seadme ja mobiilse rakenduse halduse lahendust, nagu [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Lisateavet selle kohta, kuidas kasutada Intune'i rakenduste lisamiseks, vaadake teemast [Rakenduste lisamine Microsoft Intune'i](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Rakenduse kauplusest rakenduse installimine

Lihtsaim viis rakenduse installimiseks ühte seadmesse on rakenduse installimine rakenduse kauplusest, see võimaldab saada alati värskeima laiemalt saadaoleva versiooni. Microsoft Intune saab rakenduste kauplustest ka rakendusi hankida. Rakenduse kauplusest rakenduse installimiseks kasutage ühte järgmistest linkidest:

- **Windows (UWP):** [laohaldus Microsoft Store poes](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Laohaldus Google Play poes](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Laadige rakendus alla Microsoft App Centerist

Alternatiivina rakenduse kauplusest installimisele saate selle asemel rakenduse Microsoft App Centerist alla laadida. App Center pakub installitavaid pakette, mida saate käsitsi laadida. Lisaks praegusele versioonile laseb App Center teil alla laadida ka varasemaid versioone ja võib pakkuda tulevaste versioonide eelvaadet koos funktsioonidega, mida saate proovida. Laohalduse mobiilirakenduse praeguste, eelmiste või eelvaate versioonide allalaadimiseks Microsoft App Centeri kaudu kasutage ühte järgmistest linkidest:

- **Windows (UWP):** [laohaldus (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Juhiseid, kuidas installida allalaaditud pakett Windowsi seadmesse ja seejärel seadistada nõutavad sertifikaadid, vaadake [Installige Build App Centerist](/appcenter/distribution/installation).

- **Android** [Laohaldus (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Kui laadite alla eelvaate versiooni, on selle installimiseks vaja täiendavaid samme. Üksikasju vt [Androidi rakenduste testimine](/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Veebiteenuse rakenduse loomine Azure Active Directorys

Selleks et laohalduse mobiilirakendus saaks konkreetse Supply Chain Managementi serveriga suhelda, tuleb registreerida veebiteenuse rakendus Azure Active Directorys (Azure AD) Supply Chain Managementi rentnikule. Järgnevalt toodud protseduur on üks viis selle ülesande lõpule viimiseks. Muude võimaluste kohta üksikasjaliku teabe saamiseks, vaadake sellele protseduurile järgnevaid linke.

1. Minge brauseris lehele [https://portal.azure.com](https://portal.azure.com/).
1. Sisestage selle kasutaja nimi ja parool, kellel on juurdepääs Azure’i tellimusele.
1. Valige Azure’i portaalis vasakpoolsel navigeerimispaanil valiku **Azure Active Directory**.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Veenduge, et töötate Azure AD eksemplariga, mida kasutab Supply Chain Management.
1. Klõpsake loendis **Haldamine** suvandit **Rakenduste registreerimised**.

    ![Rakenduste registreerimised.](media/app-connect-azure-register.png "Rakenduste registreerimised")

1. Valige tööriistaribal **Uus registreerimine** viisardi **Rakenduse registreerimine** avamiseks.
1. Sisestage rakenduse nimi ja valige suvand **Ainult selle organisatsioonikataloogi kontod** ja valige **Registreeri**.

    ![Rakenduse viisardi registreerimine.](media/app-connect-azure-register-wizard.png "Rakenduse viisardi registreerimine")

1. Avaneb teie uue rakenduse registreerimisaken. Märkige välja **Rakenduse (klient) ID** väärtus üles, seda läheb hiljem vaja. Sellele ID-le on selles teemas hiljem viidatud kui *kliendi ID*.

    ![Rakenduse (klient) ID.](media/app-connect-azure-app-id.png "Rakenduse (klient) ID")

1. Valige loendist **Haldamine** suvand **Serdid ja saladused**. Seejärel valige üks järgmistest nuppudest, sõltuvalt sellest, kuidas soovite rakendust autentimiseks konfigureerida. (Lisateabe saamiseks vaadake jaotist [Serdi või kliendi saladuse abil autentimine](#authenticate) selles teemas hiljem.)

    - **Serdi üleslaadimine** – laadige üles sert saladusena kasutatamiseks. Soovitame selle lähenemisviisi kasutamist, sest see on turvalisem ja seda saab täielikumalt automatiseerida. Kui käitate laohalduse mobiilirakendust Windowsi seadmetes, märkige üles väärtus **Sõrmejälg**, mida kuvatakse pärast serdi üleslaadimist. Vajate seda väärtust Windowsi seadmetes serdi konfigureerimisel.
    - **Uus kliendi saladus** – looge võti, sisestades võtme kirjeldus ja kestus jaotises **Paroolid** ning seejärel valige **Lisa**. Tehke võtmest koopia ja talletage see turvaliselt.

    ![Serdid ja saladused.](media/app-connect-azure-authentication.png "Serdid ja saladused")

Lisateavet Azure AD-s veebiteenuse rakenduste seadistamise kohta leiate järgmistest allikatest.

- Juhiste saamiseks selle kohta, kuidas kasutada Windows PowerShelli veebiteenuse rakenduste seadistamiseks Azure AD-s, vaadake teemat [Kuidas: teenusesubjekti loomine serdiga Azure PowerShelli abil](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Üksikasjaliku teabe saamiseks, kuidas Azure AD-s käsitsi veebiteenuse rakendust luua, vaadake järgmisi teemasid.

    - [Lühijuhend: rakenduse registreerimine Microsofti identiteedi platvormiga](/azure/active-directory/develop/quickstart-register-app)
    - [Kuidas: portaali abil Azure AD rakenduse ja ressurssidele juurde pääseva teenusesubjekti loomine](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Supply Chain Managementis kasutajakonto loomine ja konfigureerimine

Supply Chain Managementi lubamiseks, et kasutada Azure AD rakendust, toimige järgmiselt.

1. Looge laohalduse mobiilirakenduse kasutaja identimisteabele vastav kasutaja.

    1. Avage Supply Chain Managementis **Süsteemihaldus \> Kasutajad \> Kasutajad**.
    1. Looge kasutaja.
    1. Määrake ladustamise mobiilse seadme kasutaja.

    ![Määrake ladustamise mobiilse seadme kasutaja.](media/app-connect-app-users.png "Ladustamise mobiilse seadme kasutaja määramine")

1. Seostage oma Azure AD rakendus laohalduse mobiilirakenduse kasutajaga.

    1. Minge jaotisse **Süsteemihaldus \> Seadistus \> Azure Active Directory rakendused**.
    1. Looge rida.
    1. Sisestage kliendi ID, mille märkisite üles eelmises jaotises, pange sellele nimi ja valige äsja loodud kasutaja. Soovitame teil sildistada kõik oma seadmed. Sellisel juhul saate seadme kaotamise korral selle lehe kaudu hõlpsalt eemaldada nende Supply Chain Managementi juurdepääsu.

    ![Azure Active Directory rakendused.](media/app-connect-aad-apps.png "Azure Active Directory avaldused")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Autentimine serdi või kliendi saladuse abil

Azure AD-ga autentimine pakub turvalist viisi mobiilse seadme ühendamiseks Supply Chain Managementiga. Saate autentida nii serdi kui ka kliendi saladuse abil. Kui impordite ühenduse sätteid, soovitame kliendi saladuse asemel kasutada serti. Kuna kliendi saladus peab olema alati turvaliselt talletatud, ei saa te seda ühenduse sätete failist või QR-koodist importida, nagu selles teemas hiljem kirjeldatakse.

Serte saab kasutada saladusena rakenduse identiteedi tõestamisel, kui luba taotletakse. Serdi avalik osa laaditakse üles rakenduse registreerimiseks Azure’i portaalis, kuid täielik sert tuleb juurutada igasse seadmesse, kuhu on installitud laohalduse mobiilirakendus. Teie organisatsioon vastutab serdi haldamise eest roteerimise ja muus osas. Teil on võimalik kasutada enda allkirjastatud serte, kuid te peaksite alati kasutama mitte-eksporditavaid serte.

Peate tegema serdi kohalikult kättesaadavaks igas seadmes, kus käitate laohalduse mobiilirakendust. Lisateavet selle kohta, kuidas hallata Intune'i juhitavate seadmete serte Intune'i kasutamise korral, vaadake teemast [Sertide kasutamine Microsoft Intune'is autentimiseks](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Rakenduse konfigureerimine ühenduse sätete importimise abil

Rakenduse haldamise lihtsustamiseks ja selle juurutamiseks mitmes mobiilses seadmes, saate importida ühenduse sätted selle asemel, et neid igas seadmes käsitsi sisestada. Selles jaotises selgitatakse, kuidas neid sätteid luua ja importida.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Ühenduse sätete faili või QR-koodi loomine

Ühenduse sätteid saate importida failist või QR-koodist. Mõlema lähenemisviisi puhul peate esmalt looma sätete faili, mis kasutab vormingut JavaScript Object Notation (JSON) ja selle süntaksit. See fail peab sisaldama ühenduse loendit, mis sisaldab individuaalseid ühendusi, mida peab lisama. Järgmises tabelis võetakse kokku parameetrid, mida peate ühenduse sätete failis määrama.

| Parameeter | Kirjeldus |
|---|---|
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

Tavaliselt kasutate ühenduse sätete failide jaotamiseks kõigisse oma hallatavatesse seadmetesse seadme haldustööriista või skripti. Kui kasutate ühenduse sätete faili salvestamisel kõigis seadmeis selle vaikenime ja -asukohta, impordib laohalduse mobiilirakendus selle automaatselt ka esmakordsel käitamisel pärast rakenduse installimist. Kui kasutate faili jaoks kohandatud nime või asukohta, peab rakenduse kasutaja määrama väärtused esmakordsel käitamisel. Kuid rakendus jätkab edaspidi määratud nime ja asukoha kasutamist.

Rakenduse käivitamisel impordib see ühenduse sätted iga kord uuesti nende eelmisest asukohast, et teha kindlaks, kas on tehtud muudatusi. Rakendus värskendab ainult neid ühendusi, millel on ühenduse sätete failis olevate ühendustega samad nimed. Kasutaja loodud ühendusi, mis kasutavad teisi nimesid, ei värskendata.

Ühenduse sätete faili abil ei saa ühendust eemaldada.

Nagu eelnevalt mainitud, on vaikefaili nimi *connections.json*. Faili vaikeasukoht sõltub sellest, kas kasutate Windowsi või Androidi seadet.

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Tavaliselt luuakse teed automaatselt rakenduse esmakordsel käivitamisel. Kuid saate need käsitsi luua, kui peate enne installimist ühenduse sätete faili seadmesse üle kandma.

> [!NOTE]
> Rakenduse desinstallimisel eemaldatakse vaiketee ja selle sisu.

### <a name="import-the-connection-settings"></a>Ühenduse sätete importimine

Järgige neid juhiseid ühenduse sätete importimiseks failist või QR-koodist.

1. Käivitage laohalduse mobiilirakendus oma mobiilses seadmes. Rakenduse esmakordsel käivitamisel kuvatakse tervitusteade. Valige **Ühenduse valik**.

    ![Tervitussõnum.](media/app-configure-welcome-screen.png "Tervitussõnum")

1. Kui impordite ühenduse sätted failist ja selle salvestamisel kasutati vaikenime ja -asukohta, on rakendus võib-olla juba faili leidnud. Sellisel juhul edasi sammu 4 juurde. Vastasel juhul valige suvand **Häälesta ühendus** ja jätkake siis sammuga 3.

    ![Häälestage ühendus.](media/app-configure-set-up-connection.png "Häälestage ühendus")

1. Valige dialoogiboksis **Ühenduse häälestus** suvand **Lisa failist** või **Lisa QR-koodist**, olenevalt sellest, kuidas soovite sätted importida.

    - Kui impordite ühenduse sätteid failist, valige käsk **Lisa failist**, sirvige failini kohalikus seadmes ja valige see. Kui valite kohandatud asukoha, talletab rakendus selle ja kasutab seda automaatselt järgmisel korral.
    - Kui impordite ühenduse sätted QR-koodi skannimise abil, valige **Lisa QR-koodist**. Rakendus küsib teilt luba seadme kaamera kasutamiseks. Pärast loa andmist käivitatakse kaamera, et saaksite kasutada seda skannimiseks. Olenevalt seadme kaamera kvaliteedist ja QR-koodi keerukusest, võib teil olla raske saada korralikku skanni. Sel juhul proovige QR-koodi keerukust vähendada, luues ainult ühe ühenduse QR-koodi kohta. (Praegu saate QR-koodi skannimiseks kasutada ainult seadme kaamerat.)

    ![Ühenduse häälestusmenüü.](media/app-configure-connection-setup-flyout.png "Ühenduse häälestusmenüü")

1. Kui ühenduse sätted on edukalt laaditud, kuvatakse valitud ühendus.

    ![Ühenduse sätted laaditud.](media/app-configure-select-connection.png "Ühenduse sätted laaditud")

1. Kui kasutate Androidi seadet ja kasutate autentimisel serti, palub seade teil serdi valida.

    ![Serdi valimise viip Android seadmes.](media/app-configure-select-certificate.png "Serdi valimise viip Androidi seadmes")

1. Rakendus loob ühenduse teie Supply Chain Managementi serveriga ja kuvab sisselogimise lehe.

    ![Sisselogimise leht.](media/app-configure-sign-in-page.png "Sisselogimise leht")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Rakenduse käsitsi konfigureerimine

Kui teil pole faili ega QR-koodi, saate rakenduse seadmel käsitsi konfigureerida, et see looks ühenduse Supply Chain Managementi serveriga rakenduse Azure AD kaudu.

1. Käivitage laohalduse mobiilirakendus oma mobiilses seadmes.
1. Kui rakendus on käivitatud **demorežiimis**, valige suvand **Ühenduse sätted**. Kui rakenduse käivitamisel kuvatakse **sisselogimisleht**, valige suvand **Muuda ühendust**.
1. Valige suvand **Häälesta ühendus**.

    ![Häälestage ühendus.](media/app-configure-set-up-connection.png "Häälestage ühendus")

1. Valige **Käsitsi sisestamine**.

    ![Ühenduse häälestusmenüü.](media/app-configure-connection-setup-flyout.png "Ühenduse häälestusmenüü")

    Kuvatakse leht **Uus ühendus** ja kuvab sätted, mis on nõutavad ühenduse üksikasjade käsitsi sisestamiseks.

    ![Käsitsi ühendamise väljad.](media/app-configure-input-manually.png "Käsitsi ühendamise väljad")

1. Sisestage järgmine teave:

    - **Kliendi saladuse kasutamine** – määrake selle suvandi väärtusekd _Jah_, et kasutada kliendi saladust Supply Chain Managementiga autentimiseks. Autentimisel serdi kasutamiseks määrake selle väärtuseks _Ei_. (Lisateavet vt selle teema varasemast jaotisest [Veebiteenuse rakenduse loomine rakenduses Azure Active Directory](#create-service).)
    - **Ühenduse nimi** – sisestage uue ühenduse nimi. See nimi kuvatakse väljal **Ühenduse valimine** järgmisel korral, kui avate ühenduse sätted. Sisestatav nimi peab olema kordumatu. (Teisisõnu peab see erinema kõigist muudest teie seadmesse salvestatud ühenduse nimedest, kui sinna on talletatud teisi ühenduse nimesid.)
    - **Active Directory kliendi ID** – sisestage kliendi ID, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service).
    - **Active Directory kliendi saladus** – see väli on saadaval ainult siis, kui suvandi **Kkliendi saladuse kasutamine** väärtuseks on seatud _Jah_. Sisestage kliendi saladus, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service).
    - **Active Directory serdi sõrmejälg** – see väli on saadaval ainult Windowsi seadmete puhul ja ainult kui suvandi **Kliendi saladuse kasutamine** väärtuseks on seatud _Ei_. Sisestage serdi sõrmejälg, mille märkisite üles Azure AD seadistamise ajal, jaotises [Veebiteenuse rakenduse loomine Azure Active Directorys](#create-service).
    - **Active Directory ressurss** – määrake Supply Chain Managementi juur-URL.

        > [!IMPORTANT]
        > Ärge lisage selle väärtuse lõppu kaldkriipsu (/).

    - **Azure Active directory rentnik** – sisestage Azure AD rentnik, mida kasutate Supply Chain Managementi serveri puhul. Sellel väärtusel on vorm `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Näite leiate siit: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!IMPORTANT]
        > Ärge lisage selle väärtuse lõppu kaldkriipsu (/).

    - **Ettevõte** – sisestage rakendusse Supply Chain Management juriidiline isik (ettevõte), millega soovite rakenduse ühendada.

1. Valige lehe ülemises parempoolses nurgas olev nupp **Salvesta**.
1. Kui kasutate Androidi seadet ja kasutate autentimisel serti, palub seade teil serdi valida.
1. Rakendus loob ühenduse teie Supply Chain Managementi serveriga ja kuvab sisselogimise lehe.

## <a name="remove-access-for-a-device"></a>Seadmelt juurdepääsu äravõtmine

Kui seade läheb kaduma või satub ohtu, peate eemaldama juurdepääsu Supply Chain Managementile sellelt. Järgmised toimingud kirjeldavad juurdepääsu eemaldamise soovituslikku protsessi.

1. Minge jaotisse **Süsteemihaldus \> Seadistus \> Azure Active Directory rakendused**.
1. Kustutage rida, mis vastab seadmele, millelt soovite juurdepääsu ära võtta. Märkige üles seadme jaoks kasutatav kliendi ID, kuna vajate seda hiljem.

    Kui olete registreerinud ainult ühe kliendi ID ja mitu seadet kasutavad sama kliendi ID-d, tuleb teil nende seadmete jaoks uued ühenduse sätted luua. Vastasel juhul kaotavad need juurdepääsu.

1. Logige sisse Azure’i portaali lehel [https://portal.azure.com](https://portal.azure.com/).
1. Valige vasakpoolsel navigeerimispaanil **Active Directory** ja veenduge, et olete õiges kaustas.
1. Valige loendist **Haldamine** suvand **Rakenduste registreerimine** ja seejärel rakendus, mida soovite konfigureerida. Kuvatakse leht **Sätted** koos konfiguratsiooniteabega.
1. Veenduge, et rakenduse kliendi ID ühtib kliendi ID-ga, mille märkisite üles etapis 2.
1. Valige tööriistaribal **Kustuta**.
1. Valige kuvatavast kinnitusteatest **Jah**.

## <a name="additional-resources"></a>Lisaressursid

- [Mobiilse seadme kasutaja sätted](mobile-device-user-settings.md)
- [Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine](step-icons-titles.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]