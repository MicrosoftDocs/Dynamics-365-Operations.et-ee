---
title: Norra kassaregistrite juurutuse juhised
description: See teema annab juhiseid selle kohta, kuidas lubada kassaaparaatide funktsioone Microsoft Dynamics 365 Commerce Norra lokaliseerimisel.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c7e64dbfe6a300c097b5b3711ac4310f3386df11
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944736"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norra kassaregistrite juurutuse juhised

[!include[banner](../includes/banner.md)]

See teema annab juhiseid selle kohta, kuidas lubada kassaaparaatide funktsioone Microsoft Dynamics 365 Commerce Norra lokaliseerimisel. Lokaliseerimine koosneb mitmest komponentide laiendist. Need laiendid lasevad teil teha toiminguid, nagu kohandatud väljade printimine kviitungitele, täiendavate auditisündmuste, müügikannete ja maksekannete registreerimine kassas (POS), müügikannete digitaalselt allkirjastamine ja aruannete printimine kohalikes vormingutes. Lisateavet Norra lokaliseerimise kohta vt Norra [kassaraamatu funktsioonist](./emea-nor-cash-registers.md). Lisateavet Norra äri konfigureerimise kohta vt [Häälestage Norra äri](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [lokaliseerimisfunktsiooni](../dev-itpro/build-pipeline.md) jaoks kasutada. Peate kasutama Norra digitaalallkirja näidisversiooni jaemüügi tarkvara arenduskomplekti (SDK) eelmises versioonis arendaja virtuaalmasinas (VM) elutsükli Microsoft Dynamics teenustes (LCS). Lisateavet vt Norra [kassaraamatute juurutuse juhistest](./emea-nor-loc-deployment-guidelines.md) (pärand).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

## <a name="set-up-fiscal-registration-for-norway"></a>Saate häälestada Norra finantsregistreerimist.

Norra fiskaalregistreerimise näidis põhineb [fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md) funktsioonil ja on osa jaemüügi SDK-st. Näidis asub lahenduste hoidla **kaustas \\ FiscalIntegration \\ SequentialSignatureNorway (näiteks näidis**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[väljalaskest/9.34).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway) Näidis koosneb [fiskaaldokumendi](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) pakkujast ja fiskaalühendusest, mis on Commerce Runtime CRT () laiendid. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

Täitke finantsregistreerimise seadistuse etapid, mida kirjeldatakse [ärikanalite fiskaalintegratsiooni](./setting-up-fiscal-integration-for-retail-channel.md) seadistamisel:

1. [Seadistage fiskaalregistreerimise](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) protsess. Tehke kindlasti märkus Norrale omase fiskaalregistreerimise [protsessi sätete](#configure-the-fiscal-registration-process) kohta.
1. [Tõrke käsitlemise sätete](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) seadistamine.
1. [Luba edasilükatud fiskaalregistreerimise käsitsi](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) käivitamine.
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="configure-the-fiscal-registration-process"></a>Fiskaalregistreerimisprotsessi konfigureerimine

Järgige neid samme, et lubada Commerce Headquartersis Norra fiskaalregistreerimise protsess.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid Commerce SDK-st:

    1. Lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla avamine.
    1. Avage viimane saadav väljalaskeharu (nt **[vabastamine/9.34).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**
    1. Saate **avada src \>\> FiscalIntegrationi SequentialSignatureNorway \> CommerceRuntime.**
    1. Laadige alla fiskaaldokumendi pakkuja **konfiguratsioonifail documentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** (nt [väljalaske/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml) fail).
    1. Laadige alla fiskaalkonnektori **konfiguratsioonifail konnektoris.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml (nt väljalaske**[fail/9.34).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)

1. Minge rakenduse **Retail ja Commerce Headquarters \>\> häälestusparameetrite ühiskasutuses \>** parameetritesse. Seadke **vahekaardil** Üldine suvand Luba **fiskaalintegratsioon** väärtusele **Jah**.
1. Minge **jaemüügi- ja ärikanali \>\>\> häälestuse fiskaalintegratsiooni fiskaalkonnektori ja laadige varem alla** laaditud fiskaalkonnektori konfiguratsioonifail.
1. Minge jaemüügi **ja ärikanali häälestuse \>\> fiskaalintegratsiooni finantsdokumendi pakkujate juurde ja laadige varem alla \>** laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> konnektori** funktsiooniprofiilidesse. Looge uus ühendusfunktsionaalne profiil ning valige dokumendipakkuja ja ühendus, mille varem laadisite.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> finantsintegratsiooni \> konnektori tehnilistesse** profiilidesse. Looge uus konnektori tehniline profiil ja valige ühendus, mille varem laadisite. Seadke konnektori tüübiks **Internal** (Sisemine).
1. Minge jaemüügi- ja ärikanali häälestuse fiskaalintegratsiooni fiskaalühenduse gruppidesse ja looge varem loodud **\>\>\>** konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
1. Minge jaemüügi **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalregistreerimisprotsessidesse.** Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige **finants registreerimisprotsessi** kiirkaardil varem loodud fiskaalregistreerimise protsess. Valige **finantsteenuste** kiirkaardil varem loodud konnektori tehniline profiil. 
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**. Avage jaotusgraafik ja valige kanali andmebaasi andmete ülekandmiseks **tööd** **1070 ja 1090.**

### <a name="configure-the-digital-signature-parameters"></a>Digitaalallkirja parameetrite konfigureerimine

Teil tuleb konfigureerida tunnistused, mida kasutatakse kaupluses müügikannete digitaalallkirjasmiseks. Digitaalserti, mis on talletatud Azure Key Vault'is, kasutatakse allkirjastamiseks. Modern POS-i võrguühenduseta režiimi korral saab allkirjastamist teha ka digitaalse serdiga, mis on salvestatud Modern POS-i installitud arvuti kohalikku salvestusse.

Enne, kui saate kasutada vaultvõtme talletatud digitaalserdit, tuleb läbida järgmised sammud.

1. Võtme hoidla peab olema loodud. Soovitame teil juurutada ladustamise samas geograafilises piirkonnas nagu Commerce Scale Unit.
1. Sert tuleb üles laadida võtmehoidlasse alus64 stringisaladusena.
1. Rakendusobjekti serveri (AOS) rakendus peab olema volitatud lugemiseks võtmesalvestuse turvahoidla saladusi.

Lisateavet selle kohta, kuidas võtmega Vault töötada, vt [Teemat Alustamine Azure'i võtme vault-ga](/azure/key-vault/key-vault-get-started).

Seejärel peate võtme hoidla parameetrite lehel määrama parameetrid võtme hoidlasse **pääsemiseks**:

- **Nimi** **ja kirjeldus –** võtmesalvestuse nimi ja kirjeldus.
- **Võtme hoidla URL** – võtmesalvestuse URL.
- **Vault-võtme klient – autentimiseks võtmelaoga seostatud () rakenduse interaktiivne** Azure Active Directory Azure AD kliendi-ID. Sellel kliendil peab olema juurdepääs salvestuse lugemissaladustele.
- **Võtme vault-salavõti – salavõti, mis on seostatud rakendusega, mida kasutatakse** Azure AD autentimiseks võtme hoidlas.
- **Nimi,** **kirjeldus ja** **salaviide** – tunnistuse nimi, kirjeldus ja salaviide.

Seejärel peate konfigureerima konnektori oma sertide jaoks, mis on talletatud võtme vault- või kohalikus serdilaos. Seda ühendust kasutatakse kanali poolele allkirjastamiseks.

1. Minge jaemüügi ja **ärikanali \> häälestuse \> finantsintegratsiooni \> konnektori tehnilistesse** profiilidesse.
1. Määrake **kiirkaardil** Sätted digitaalallkirjade jaoks järgmised parameetrid.

    - **Salanimi – valige varem konfigureeritud võtme hoidla parameetrite lehel** **salanimi**.
    - **Kohaliku serdi** sõrmejälg – sisestage sõrmejälg kohalikult talletatavale serdile.
    - **Räsialgoritm** – määrake üks krüptograafilise räsi algoritmidest, mida toetab näiteks Microsoft .NET **SHA1**.
    - **Serdi kaupluse nimi** – see väli on valikuline. Kasutage seda kaupluse vaikenime määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Serdi kaupluse asukoht** – see väli on valikuline. Kasutage seda kaupluse vaikeasukoha määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Proovige esmalt kohalikku serti – valige see suvand, et kasutada vaikimisi kohaliku kaupluse serti allkirjastamise** andmete, mitte võtme vault serdi puhul.
    - **Aktiveeri seisundi** kontroll – lisateabe saamiseks tervisekontrolli funktsiooni kohta vt fiskaalregistreerimise seisundi [kontroll](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Praegu on **Norra jaoks vastuvõetav ainult SHA1** krüptograafiline räsialgoritm.
> - Kohalike sertide otsimise lihtsustamiseks lisatakse kaupluse vaikenimi ja kaupluse CRT asukoht. X509StoreProvideril on loend kaustadest, kus serte talletatakse. Kui kaupluse vaikenimi ja vaikeasukoht on määramata, proovib X509StoreProvider leida sertifikaati kõigis selle loendi kaustades.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

### <a name="development-environment"></a>Arenduskeskkonnad

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

1. Rakenduste hoidla [Dynamics 365 Commerce leidmine](https://github.com/microsoft/Dynamics365Commerce.Solutions) või allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi SDK näidised ja viitepakendid alla laadida [GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage **lahendus SequentialSignatureNorway.sln** **dynamics365Commerce.Solutions \\ FiscalIntegration \\ SequentialSignatureNorway ja koostage** see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit:** **kaustas SequentialSignatureNorway \\\\ ScaleUnit ScaleUnit.SequentialSignNorway.Installer \\ bin \\ Debug \\ net461** leidke **ScaleUnit.SequentialSignNorway.Installer.**
        - **Kohalik CRT modern POS-s: leidke** **kaustas SequentialSignatureNorway \\\\ ModernPOS.SequentialSignNorway.Installer \\ bin \\ Debug \\ net461** **kaustas ModernPos.SequentialSignNorway.Installer.**

    1. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni näidise jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid [fiskaalintegratsiooni](fiscal-integration-sample-build-pipeline.md) näidiskomplekti jaoks. Malli **SequentialSignatureNorway build-pipeline.jaml malli JAML faili leiate lahenduste** **\\ hoidla YAML_Files**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) müügivõimaluste kaustast.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Digitaalallkirja lubamine Modern POS-i võrguühenduseta režiimis

Modern POS-i võrguühenduseta režiimis digitaalallkirja lubamiseks peate järgima neid samme pärast Modern POS-i aktiveerimist uues seadmes.

1. Logige teenusesse POS sisse.
1. Andmebaasi ühenduse **oleku lehel** veenduge, et ühenduseta andmebaas on täielikult sünkroonitud. Kui välja Ootel **allalaadimised** väärtus on **0** (null), siis on andmebaas täielikult sünkroonitud.
1. Logige müügikohast välja.
1. Oodake, kuni ühenduseta andmebaas täielikult sünkroonitakse.
1. Logige teenusesse POS sisse.
1. Andmebaasi ühenduse **oleku lehel** veenduge, et ühenduseta andmebaas on täielikult sünkroonitud. Kui ootel kannete **väärtus võrguühenduseta andmebaasi väljal** on **0** (null), siis andmebaas täielikult sünkroonitakse.
1. Modern POS-i taasavamine.
