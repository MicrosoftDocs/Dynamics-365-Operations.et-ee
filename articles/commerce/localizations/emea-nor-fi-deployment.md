---
title: Norra kassaregistrite juurutuse juhised
description: See artikkel annab juhiseid selle kohta, kuidas lubada kassaaparaatide funktsioone Norra Microsoft Dynamics 365 Commerce lokaliseerimisel.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 0e66ef93e65fecaca23f0434c386507a0672d251
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631311"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norra kassaregistrite juurutuse juhised

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Rakendage selles artiklis kirjeldatud sammud ainult juhul, kui kasutate Microsoft Dynamics 365 Commerce versiooni 10.0.29 või uuemat versiooni. Commerce’i versioonis 10.0.28 või varem peate kasutama jaemüügitarkvara arenduskomplekti (SDK) eelmist versiooni elutsükli teenuste (VM) Microsoft Dynamics arenduskomplektis. Lisateavet vt Norra kassaraamatute [juurutuse juhistest (pärand)](./emea-nor-loc-deployment-guidelines.md). Kui kasutate Commerce’i versiooni 10.0.28 või varasemat versiooni ja kannate üle Commerce’i versiooni 10.0.29 või uuemasse versiooni, [peate järgima Norra pärand commerce’i funktsioonide migreerimine](./emea-nor-fi-migration.md).

See artikkel annab juhiseid selle kohta, kuidas lubada kassaaparaatide funktsioone Norra Commerce’i lokaliseerimise jaoks. Lokaliseerimine koosneb mitmest komponendi laiendist, mis lubab teil sooritada toiminguid, nagu kohandatud väljade printimine sissetulekutele, auditi lisasündmuste, müügikannete ja maksekannete printimine müügikohas (POS), müügikannete digitaalselt allkirjastamine ja aruannete printimine kohalikes vormingutes. Lisateavet Norra lokaliseerimise kohta vt Norra kassaraamatu [funktsioonist](./emea-nor-cash-registers.md). Lisateavet Norra äri konfigureerimise kohta vt Häälestage [Norra äri.](./emea-nor-cash-registers.md#setting-up-commerce-for-norway)

## <a name="set-up-fiscal-registration-for-norway"></a>Saate häälestada Norra finantsregistreerimist.

Norra fiskaalregistreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on Osa Commerce SDK-st. Näidis asub lahenduste hoidla **kaustas FiscalIntegration\\\\ SequentialSignatureNorway**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast ja fiskaalühendusest, mis on Commerce Runtime’i () laiendid CRT. Lisateavet Commerce SDK kasutamise kohta vt commerce SDK [näidised ja viitepakendite allalaadimine GitHub-st NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ja koostevõimaluste kohta sõltumatu pakendamise SDK-le](../dev-itpro/build-pipeline.md).

Lõpetage finantsregistreerimise seadistuse etapid, mida on kirjeldatud [Ärikanalite fiskaalintegratsiooni seadistamises](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Seadistage fiskaalregistreerimise protsess](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Tehke kindlasti märkus Norrale omase fiskaalregistreerimise protsessi [sätete kohta](#configure-the-fiscal-registration-process).
1. [Tõrke käsitlemise sätete seadistamine](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Luba edasilükatud fiskaalregistreerimise käsitsi käivitamine](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Kanali komponentide konfigureerimine](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Fiskaalregistreerimisprotsessi konfigureerimine

Järgige neid samme, et lubada Commerce Headquartersis Norra fiskaalregistreerimise protsess.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid Commerce SDK-st:

    1. [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Lahenduste hoidla avamine.
    1. Avage viimane saadav väljalaskeharu.
    1. Saate **avada src \> FiscalIntegrationi \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Laadige alla finantsdokumendi pakkuja konfiguratsioonifail at **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml**.
    1. Laadige alla fiskaalkonnektori **konfiguratsioonifail konnektoris.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml**.

1. Minge rakenduse **Retail ja Commerce \> Headquarters häälestusparameetrite \> ühiskasutusega \> parameetritesse**. Seadke vahekaardil **Üldine** suvand Luba fiskaalintegratsioon **väärtusele** **Jah**.
1. Minge jaemüügi- **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalkonnektori ja laadige varem alla laaditud fiskaalkonnektori** konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \>\> finantsdokumendi pakkujate** juurde ja laadige varem alla laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiscal \> integration Connectori funktsiooniprofiilidesse \>**. Looge uus ühendusfunktsionaalne profiil ning valige dokumendipakkuja ja ühendus, mille varem laadisite.
1. Minge jaemüügi ja **ärikanali häälestuse \> finantsintegratsiooni \> konnektori \> tehnilistesse profiilidesse**. Looge uus konnektori tehniline profiil ja valige ühendus, mille varem laadisite. Seadke konnektori tüübiks Internal (**Sisemine**).
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalühenduse** gruppidesse ja looge varem loodud konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalregistreerimisprotsessidesse \>**. Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige finants **registreerimisprotsessi kiirkaardil** varem loodud fiskaalregistreerimise protsess. Valige finantsteenuste **kiirkaardil** varem loodud konnektori tehniline profiil. 
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**. Avage jaotusgraafik ja valige kanali andmebaasi **andmete ülekandmiseks tööd 1070** **ja 1090**.

### <a name="configure-the-digital-signature-parameters"></a>Digitaalallkirja parameetrite konfigureerimine

Teil tuleb konfigureerida tunnistused, mida kasutatakse kaupluses müügikannete digitaalallkirjasmiseks. Digitaalserti, mis on talletatud Azure Key Vault’is, kasutatakse allkirjastamiseks. Modern POS-i võrguühenduseta režiimi korral saab allkirjastamist teha ka digitaalse serdiga, mis on salvestatud Modern POS-i installitud arvuti kohalikku salvestusse.

Enne, kui saate kasutada vaultvõtme talletatud digitaalserdit, tuleb läbida järgmised sammud.

1. Võtme hoidla peab olema loodud. Soovitame teil juurutada ladustamise samas geograafilises piirkonnas nagu Commerce Scale Unit.
1. Sert tuleb üles laadida võtmehoidlasse alus64 stringisaladusena.
1. Rakendusobjekti serveri (AOS) rakendus peab olema volitatud lugemiseks võtmesalvestuse turvahoidla saladusi.

Lisateavet selle kohta, kuidas võtmega Vault töötada, vt [Teemat Alustamine Azure’i võtme vault-ga](/azure/key-vault/key-vault-get-started).

Seejärel peate võtme **hoidla parameetrite lehel** määrama parameetrid võtme hoidlasse pääsemiseks:

- **Nimi** ja **kirjeldus** – võtmesalvestuse nimi ja kirjeldus.
- **Võtme hoidla URL – võtmesalvestuse URL**.
- **Vault-võtme klient** – autentimiseks võtmesalvestusega seostatud (Azure Active Directory) rakenduse interaktiivne kliendi-ID Azure AD. Sellel kliendil peab olema juurdepääs salvestuse lugemissaladustele.
- **Võtme vault-salavõti** – salavõti, Azure AD mis on seostatud rakendusega, mida kasutatakse autentimiseks võtme hoidlas.
- **Nimi**, **kirjeldus** ja **salaviide**– tunnistuse nimi, kirjeldus ja salaviide.

Seejärel peate konfigureerima konnektori oma sertide jaoks, mis on talletatud võtme vault- või kohalikus serdilaos. Seda ühendust kasutatakse kanali poolele allkirjastamiseks.

1. Minge jaemüügi ja **ärikanali häälestuse \> finantsintegratsiooni \> konnektori \> tehnilistesse profiilidesse**.
1. **Määrake kiirkaardil** Sätted digitaalallkirjade jaoks järgmised parameetrid.

    - **Salanimi** – valige varem konfigureeritud **võtme** hoidla parameetrite lehel salanimi.
    - **Kohaliku serdi sõrmejälg** – sisestage sõrmejälg kohalikult talletatavale serdile.
    - **Räsialgoritm** – määrake üks krüptograafilise räsi algoritmidest, mida Microsoft .NET toetab näiteks **SHA1**.
    - **Serdi kaupluse nimi** – see väli on valikuline. Kasutage seda kaupluse vaikenime määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Serdi kaupluse asukoht** – see väli on valikuline. Kasutage seda kaupluse vaikeasukoha määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Proovige esmalt kohalikku serti** – valige see suvand, et kasutada vaikimisi kohaliku kaupluse serti allkirjastamise andmete, mitte võtme vault serdi puhul.
    - **Aktiveeri seisundi kontroll** – lisateabe saamiseks tervisekontrolli funktsiooni kohta vt fiskaalregistreerimise [seisundi kontroll](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Praegu on **Norra jaoks vastuvõetav ainult SHA1** krüptograafiline räsialgoritm.
> - Kohalike sertide otsimise lihtsustamiseks lisatakse kaupluse vaikenimi ja kaupluse asukoht CRT. X509StoreProvideril on loend kaustadest, kus serte talletatakse. Kui kaupluse vaikenimi ja vaikeasukoht on määramata, proovib X509StoreProvider leida sertifikaati kõigis selle loendi kaustades.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

#### <a name="development-environment"></a>Arenduskeskkond

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

1. Rakenduste hoidla leidmine [Dynamics 365 Commerce või](https://github.com/microsoft/Dynamics365Commerce.Solutions) allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt commerce [SDK näidised ja viitepakendid alla laadida GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. **Avage lahendus SequentialSignatureNorway.sln** **dynamics365Commerce.Solutions\\ FiscalIntegration\\ SequentialSignatureNorway** ja koostage see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit:** **kaustas SequentialSignatureNorway\\ ScaleUnit\\ ScaleUnit.SequentialSignNorway.Installer\\ bin\\ Debug\\ net461** leidke **ScaleUnit.SequentialSignNorway.Installer**.
        - **CRT Kohalik modern POS-s:** **leidke kaustas SequentialSignatureNorway\\ ModernPOS.SequentialSignNorway.Installer\\\\ bin\\ Debug\\ net461** kaustas **ModernPos.SequentialSignNorway.Installer**.

    1. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni [näidise](fiscal-integration-sample-build-pipeline.md) jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid fiskaalintegratsiooni näidiskomplekti jaoks. Malli **SequentialSignatureNorway build-pipeline.jaml** malli JAML **\\ faili leiate lahenduste hoidla YAML_Files**[Dynamics 365 Commerce müügivõimaluste](https://github.com/microsoft/Dynamics365Commerce.Solutions) kaustast.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Digitaalallkirja lubamine Modern POS-i võrguühenduseta režiimis

Modern POS-i võrguühenduseta režiimis digitaalallkirja lubamiseks peate järgima neid samme pärast Modern POS-i aktiveerimist uues seadmes.

1. Logige teenusesse POS sisse.
1. Andmebaasi ühenduse **oleku lehel** veenduge, et ühenduseta andmebaas on täielikult sünkroonitud. Kui välja Ootel allalaadimised **väärtus** on **0** (null), siis on andmebaas täielikult sünkroonitud.
1. Logige müügikohast välja.
1. Oodake, kuni ühenduseta andmebaas täielikult sünkroonitakse.
1. Logige teenusesse POS sisse.
1. Andmebaasi ühenduse **oleku lehel** veenduge, et ühenduseta andmebaas on täielikult sünkroonitud. Kui ootel kannete väärtus **võrguühenduseta andmebaasi väljal** on **0** (null), siis andmebaas täielikult sünkroonitakse.
1. Modern POS-i taasavamine.
