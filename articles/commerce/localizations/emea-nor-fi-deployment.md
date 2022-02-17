---
title: Norra kassaaparaatide kasutuselevõtu juhised
description: See teema annab juhiseid selle kohta, kuidas lubada Norra lokaliseerimise Microsoft Dynamics 365 Commerce kassafunktsiooni.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f0744b18ed59c692ae336c92e488d339ae158368
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077136"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norra kassaaparaatide kasutuselevõtu juhised

[!include[banner](../includes/banner.md)]

See teema annab juhiseid selle kohta, kuidas lubada Norra lokaliseerimise Microsoft Dynamics 365 Commerce kassafunktsiooni. Lokaliseerimine koosneb mitmest komponentide laiendusest. Need laiendused võimaldavad teil teha selliseid toiminguid nagu kohandatud väljade printimine kviitungitele, täiendavate auditisündmuste, müügitehingute ja maksekannete registreerimine müügikohas (kassa), müügitehingute digitaalne allkirjastamine ja aruannete printimine kohalikes vormingutes. Lisateavet Norra lokaliseerimise kohta leiate teemast [Norra kassafunktsioonid](./emea-nor-cash-registers.md). Lisateavet Norra kaubanduse konfigureerimise kohta leiate teemast [Norra kaubanduse häälestamine](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle lokaliseerimisfunktsiooni jaoks kasutada. Peate kasutama Norra digitaalallkirjastamise näidise versiooni Retail tarkvaraarenduskomplekti (SDK) eelmises versioonis arendaja virtuaalses masinas (VM) lifecycle Microsoft Dynamics Services (LCS). Lisateavet vt [teemast Deployment guidelines for Norway (legacy)](./emea-nor-loc-deployment-guidelines.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

## <a name="set-up-fiscal-registration-for-norway"></a>Norra maksuregistreerimise häälestamine

Norra maksuregistreerimisvalim põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Proov asub lahenduste hoidla kaustas  **src\\FiscalIntegration\\SequentialSignatureNorway** [Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov väljalaskes/9.34 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway) Valim [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast ja fiskaalse konnektorist, mis on Commerce'i käitusaja (CRT) laiendused. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

Täitke eelarve registreerimise häälestustoimingud, mida on kirjeldatud jaotises [Commerce'i kanalite](./setting-up-fiscal-integration-for-retail-channel.md) fiskaalintegratsiooni häälestamine.

1. [Saate häälestada finantsregistreerimise protsessi](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Pange kindlasti tähele Norrale [omaste eelarve registreerimise protsessi](#configure-the-fiscal-registration-process) sätteid.
1. [Saate määrata tõrkekäsitluse sätted](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Lubage edasilükatud finantsregistreerimise käsitsi käivitamine](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="configure-the-fiscal-registration-process"></a>Finantsregistreerimise protsessi konfigureerimine

Norra eelarveregistreerimise protsessi lubamiseks kaubanduse peakorteris tehke järgmist.

1. Laadige Commerce SDK-st alla rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonifailid.

    1. Avage lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla.
    1. Avage viimane saadaval olev väljalaskeharu (nt **[release/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Avage **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Laadige alla rahandusdokumendi pakkuja konfiguratsioonifail aadressil DocumentProvider.SequentialSignNorway Configuration DocumentProviderSequentialSignatureNorwaySample.xml **(nt \> väljalaskefail/9.34 \>).**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)
    1. Laadige alla fiskaalse konnektori konfiguratsioonifail aadressil Connector.SequentialSignNorway Configuration ConnectorSequentialSignatureNorwaySample.xml **(näiteks \> väljalaskefail/9.34 \>).**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)

1. Minema **Jaemüük ja kaubandus \> Peakorteri seadistamine \> Parameetrid \> Jagatud parameetrid**. peal **Kindral** vahekaardil määrake **Luba maksuintegratsioon** võimalus **Jah**.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühendused** ja laadige varem alla laaditud fiskaalse konnektori konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Maksudokumentide pakkujad** ja laadige varem alla laaditud maksudokumendi pakkuja konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori funktsionaalsed profiilid**. Looge uus konnektori funktsionaalne profiil ja valige dokumendi pakkuja ja varem laaditud konnektor.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**. Looge uus konnektori tehniline profiil ja valige varem laaditud konnektor. Määrake konnektori tüübiks **Sisemine**.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühenduste rühmad** ja looge varem loodud konnektori funktsionaalprofiili jaoks uus fiskaalne konnektorirühm.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalsed registreerimise protsessid**. Looge uus maksuregistreerimisprotsess ja fiskaalse registreerimise protsessi etapp ning valige varem loodud maksuühenduse rühm.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud poega, kus registreerimisprotsess tuleks aktiveerida. peal **Maksustamise registreerimise protsess** FastTab, valige varem loodud maksuregistreerimisprotsess. peal **Fiskaalteenused** FastTab, valige varem loodud konnektori tehniline profiil. 
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**. Avage levitamise ajakava ja valige tööd **1070** ja **1090** andmete edastamiseks kanali andmebaasi.

### <a name="configure-the-digital-signature-parameters"></a>Konfigureerige digitaalallkirja parameetrid

Peate konfigureerima sertifikaadid, mida kasutatakse kaupluses müügitehingute digitaalseks allkirjastamiseks. Allkirjastamiseks kasutatakse digitaalset sertifikaati, mis on salvestatud Azure Key Vault. Modern POS-i võrguühenduseta režiimis saab allkirjastada ka digitaalse sertifikaadi abil, mis on salvestatud selle masina kohalikku salvestusruumi, kuhu Modern POS on installitud.

Enne Key Vaulti salvestusruumi salvestatud digitaalse sertifikaadi kasutamist tuleb teha järgmised toimingud.

1. Key Vaulti salvestusruum tuleb luua. Soovitame salvestusruumi juurutada samasse geograafilisse piirkonda, kus on Commerce Scale Unit.
1. Sertifikaat tuleb üles laadida Key Vaulti salvestusruumi base64 stringsaladusena.
1. Rakendusobjektiserveri (AOS) rakendusel peab olema volitused Key Vaulti salvestusruumi saladuste lugemiseks.

Key Vaultiga töötamise kohta lisateabe saamiseks vt [Alustage Azure Key Vaultiga](/azure/key-vault/key-vault-get-started).

Järgmisena kohta **Key Vaulti parameetrid** lehel peate määrama Key Vaulti salvestusruumile juurdepääsu parameetrid:

- **Nimi** ja **Kirjeldus** – Key Vaulti salvestusruumi nimi ja kirjeldus.
- **Võtmehoidla URL** – Key Vaulti salvestusruumi URL.
- **Key Vaulti klient** – interaktiivne kliendi ID Azure Active Directory (Azure AD) rakendus, mis on autentimise eesmärgil seotud Key Vaulti salvestusruumiga. Sellel kliendil peaks olema juurdepääs salvestusruumist saladuste lugemiseks.
- **Key Vaulti salajane võti** – salajane võti, mis on seotud Azure AD rakendus, mida kasutatakse Key Vaulti salvestusruumi autentimiseks.
- **Nimi**, **·**, ja **Salajane viide** – Sertifikaadi nimi, kirjeldus ja salajane viide.

Järgmisena peate konfigureerima oma sertifikaatide jaoks konnektori, mis on salvestatud võtmehoidlasse või kohalikku sertifikaatide salvestusruumi. Seda pistikut kasutatakse allkirjastamiseks kanali poolel.

1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**.
1. peal **Seaded** FastTab, määrake digitaalallkirjade jaoks järgmised parameetrid:

    - **Salajane nimi** – Valige salajane nimi, mille olete varem konfigureerinud **Key Vaulti parameetrid** lehel.
    - **Kohaliku sertifikaadi pöidlajälg** – Andke kohalikult salvestatud sertifikaadile pöidlajälg.
    - **Räsi algoritm** – Määrake üks krüptograafiline räsialgoritm, mida toetab Microsoft .NET, nagu näiteks **SHA1**.
    - **Sertifikaadi poe nimi** – See väli on valikuline. Kasutage seda kaupluse vaikenime määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Sertifikaadi poe asukoht** – See väli on valikuline. Kasutage seda kaupluse vaikeasukoha määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.
    - **Proovige esmalt kohalikku sertifikaati** – Valige see suvand, et kasutada andmete allkirjastamiseks vaikimisi kohaliku poe sertifikaati Key Vaulti sertifikaadi asemel.
    - **Aktiveerige tervisekontroll** – Tervisekontrolli funktsiooni kohta lisateabe saamiseks vt [Maksuregistri tervisekontroll](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Ainult **SHA1** krüptograafiline räsialgoritm on praegu Norras vastuvõetav.
> - Kohalike sertifikaatide otsimise protsessi lihtsustamiseks lisatakse poe vaikenimi ja poe asukoht CRT. X509StoreProvideril on loend kaustadest, kus serte talletatakse. Kui vaikepoe nime ja vaikepoe asukohta pole määratud, proovib X509StoreProvider leida sertifikaati kõigist loendis olevatest kaustadest.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

### <a name="development-environment"></a>Arenduskeskkonnad

Arengukeskkonna seadistamiseks järgige neid juhiseid, et saaksite proovi testida ja pikendada.

1. Kloonige või laadige alla [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla. Valige õige väljalaske haru versioon vastavalt oma SDK/rakenduse versioonile. Lisateabe saamiseks vt [Laadige alla jaemüügi SDK näidised ja viitepaketid GitHubist ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Ava **SequentialSignatureNorway.sln** lahendus all **Dynamics365Commerce.Solutions\\ Fiskaalintegratsioon\\ SequentialSignatureNorra** ja ehitage see üles.
1. Installige CRT laiendused:

    1. Otsige üles CRT laienduse paigaldaja:

        - **Kaubanduse mastaabiüksus:** Aastal **SequentialSignatureNorra\\ Skaalaühik\\ ScaleUnit.SequentialSignNorway.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ScaleUnit.SequentialSignNorway.Installer** paigaldaja.
        - **Kohalik CRT kaasaegses POS-is:** Aastal **SequentialSignatureNorra\\ Kaasaegne POS\\ ModernPos.SequentialSignNorway.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ModernPos.SequentialSignNorway.Installer** paigaldaja.

    1. Alustage CRT laienduse installija käsurealt:

        - **Kaubanduse mastaabiüksus:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT kaasaegses POS-is:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. The **SequentialSignatureNorway build-pipeline.yaml** malli YAML-faili leiate **Torujuhe\\ YAML_Files** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Lubage kaasaegse POS-i jaoks võrguühenduseta režiimis digitaalallkiri

Modern POS-i võrguühenduseta režiimis digitaalse allkirja lubamiseks peate järgima neid samme pärast Modern POS-i aktiveerimist uues seadmes.

1. Logige teenusesse POS sisse.
1. peal **Andmebaasi ühenduse olek** lehel, veenduge, et võrguühenduseta andmebaas oleks täielikult sünkroonitud. Kui väärtus **Ootel allalaadimised** väli on **0** (null), on andmebaas täielikult sünkroonitud.
1. Logi kassast välja.
1. Oodake, kuni võrguühenduseta andmebaas on täielikult sünkroonitud.
1. Logige teenusesse POS sisse.
1. peal **Andmebaasi ühenduse olek** lehel, veenduge, et võrguühenduseta andmebaas oleks täielikult sünkroonitud. Kui väärtus **Ootel tehingud võrguühenduseta andmebaasis** väli on **0** (null), on andmebaas täielikult sünkroonitud.
1. Avage Modern POS uuesti.
