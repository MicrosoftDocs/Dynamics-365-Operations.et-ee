---
title: CPOS-i konfigureerimine kohandatud Azure AD rakenduse kasutamiseks
description: See artikkel selgitab, kuidas konfigureerida Cloud POS-i (CPOS) kohandatud Azure Active Directory (Azure AD) rakendust kasutama.
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746256"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>CPOS-i konfigureerimine kohandatud Azure AD rakenduse kasutamiseks

[!include [banner](includes/banner.md)]

Vaikimisi osutab Cloud POS (CPOS) Microsoft Dynamics 365 Commerce registreeritud esimese osapoole Microsofti rakendusele rakenduses Azure Active Directory (Azure AD). Seetõttu saate CPOS-i kasutada ilma, et teil oleks vaja teha muudatusi Azure AD. Kuid võib-olla soovite oma CPOS-i eksemplari osutada kohandatud rakendusele Azure AD, mida kontrollite. See artikkel selgitab, kuidas konfigureerida CPOS-i kohandatud rakenduse Azure AD kasutamiseks.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Kohandatud jaemüügiserveri rakenduse saate häälestada rakenduses Azure AD

Kohandatud jaemüügiserveri rakenduse loomiseks ja konfigureerimiseks Azure AD järgige neid samme.

1. Logige mis tahes [Azure Active Directory kasutajakonto abil](https://aad.portal.azure.com) halduskeskusesse Azure AD sisse. Kasutajakontol ei pea olema administraatoriõigusi.
1. Valige **Azure Active Directory**.
1. Valige **rakenduse registreerimised** ja seejärel valige uus **registreerimine**, et avada **dialoogiboks** Rakenduse registreerimine.
1. Seadistage järgmised väljad.

    - **Nimi** : sisestage rakendusele kohandatud nimi. Sisestage näiteks kohandatud **jaemüügiserver**.
    - **Tugikonto tüübid** – valige vaikesuvand, **ainult selle organisatsioonikausta kontod (ainult Microsoft – üks rentnik)**.
    - **Ümbersuunamise URI** – väli on valikuline. Jätke see tühjaks.
    - **Teenuspuu ID** – väli on valikuline. Jätke see tühjaks.
    
1. Valige suvand **Registreeri**. Kuvatakse äsja registreeritud rakenduse konfiguratsioonileht.
1. Jaotises Ülevaate põhiosa valige lisa rakenduse ID URI **ja seejärel \> valige käsk Määra** **rakenduse ID URI kõrval**.**·** **·** Tehke soovitusliku väärtuse kohta märkus ja seejärel valige salvesta **, et** selle väärtuse aktsepteerida. 
1. Valige **lisa ulatus ja** seadke seejärel järgmised väljad:

    - **Ulatuse nimi** : sisestage ulatuse kohandatud nimi. Näiteks sisestage **Legacy.Access.Full**.
    - **Kes võib olla nõus** – määrake, kas nii administraatorid kui ka kasutajad või ainult administraatorid saavad teie organisatsiooni turvapoliitikate alusel nõustuda.
    - **Administraatori nõusolekuta kuvatav nimi** – sisestage kuvatav nimi. Sisestage näiteks Juurdepääs **jaemüügiserverile**.
    - **Administraatori loa kirjeldus** – sisestage kirjeldus. Näiteks sisestage väärtus Annab **juurdepääsu jaemüügiserveri API-le**.

1. Valige **ulatuse lisamine** ulatuse loomise protsessi lõpetamiseks.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Kohandatud CPOS-rakenduse häälestamine rakenduses Azure AD

> [!IMPORTANT]
> Kui täiendate olemasolevat kohandatud CPOS-rakendust, mis loodi enne rakenduse Commerce 10.0.21, järgige juhiseid olemasoleva kohandatud CPOS-rakenduse Azure AD täiendamises [, Azure AD mis loodi enne rakenduse Commerce versiooni 10.0.21](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021).

Kohandatud CPOS-rakenduse loomiseks ja konfigureerimiseks Azure AD järgige neid samme.

1. Logige mis tahes [Azure Active Directory kasutajakonto abil](https://aad.portal.azure.com) halduskeskusesse Azure AD sisse. Kasutajakontol ei pea olema administraatoriõigusi.
1. Valige **Azure Active Directory**.
1. Valige **rakenduse registreerimised** ja seejärel valige uus **registreerimine**, et avada **dialoogiboks** Rakenduse registreerimine.
1. Seadistage järgmised väljad.

    - **Nimi** : sisestage rakenduse nimi. Sisestage näiteks kohandatud **pilve kassa**.
    - **Tugikonto tüübid** – valige vaikesuvand, **ainult selle organisatsioonikausta kontod (ainult Microsoft – üks rentnik)**.
    - **Ümbersuunamise URI** **– valige ripploendist ühe lehega rakendus (SPA)** ja sisestage seejärel oma CPOS-URI.
    - **Teenuspuu ID** – väli on valikuline. Jätke see tühjaks.

1. Valige suvand **Registreeri**. Kuvatakse äsja registreeritud rakenduse konfiguratsioonileht.
1. Seadke manifesti jaotises parameetrid **oauth2AllowIdTokenImplicitFlow** **ja oauth2AllowImplicitFlow** tõesed **ning** seejärel valige **salvestamine**.**·**
1. **Loa konfiguratsiooni jaotises** järgige neid samme kahe nõude lisamiseks:

    1. Valige **suvand Lisa valikuline nõue**. Seadke loa **tüübi väljale** **ID ja** seejärel valige **sid-nõue**. Valige **Lisa**.
    1. Valige **suvand Lisa valikuline nõue**. Seadke loa **tüübi väljale** Juurdepääs ja **seejärel** valige **sid-nõue**. Valige **Lisa**.

1. **Valige API õiguste** jaotises suvand **Lisa õigus**.
1. Vahekaardil MINU **organisatsioon kasutab** API-sid, otsige [jaemüügiserveri rakendust, mille lõite jaotises Kohandatud jaemüügiserveri rakenduse Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) häälestamine. Seejärel valige **lisa õigused**.
1. **Tehke jaotises** Ülevaade märkus väärtuse kohta väljal Rakenduse (kliendi **) ID**.

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Täiendage olemasolevat kohandatud CPOS-rakendust Azure AD, mis on loodud enne Commerce versiooni 10.0.21.

Enne äriversiooni 10.0.21 loodud olemasoleva kohandatud CPOS-rakenduse Azure AD täiendamiseks järgige neid samme. 

1. Avage oma kohandatud CPOS-rakendus Azure AD Azure’i portaalis.
1. Valige vahekaart **Autentimine**.
1. Kopeerige ja salvestage algse ümbersuunamise URI veebitüübist **hilisemaks** kasutamiseks ning seejärel kustutage see.
1. Valige **lisa platvorm** ja seejärel valige **üheleheline rakendus (SPA).**
1. Lisage esialgne veebi ümbersuunamise URI, mis on kopeeritud SPA platvormile.
1. **Loa konfiguratsiooni jaotises** järgige neid samme kahe nõude lisamiseks:
    1. Valige **suvand Lisa valikuline nõue**. Seadke loa **tüübi väljale** **ID ja** seejärel valige **sid-nõue**. Valige **Lisa**.
    1. Valige **suvand Lisa valikuline nõue**. Seadke loa **tüübi väljale** Juurdepääs ja **seejärel** valige **sid-nõue**. Valige **Lisa**.

## <a name="update-the-cpos-configuration-file"></a>CPOS-i konfiguratsioonifaili värskendamine

Avage fail CPOS config.json ja tehke selles järgmised uuendused.

1. Asendage **AADClientId** **võtmeväärtus rakenduse (kliendi) ID** väärtusega kohandatud CPOS-rakendusel [, mille lõite jaotises Kohandatud CPOS-rakenduse Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) häälestamine.
1. Asendage **võtmeväärtus AADRetailServerResourceId** **kohandatud jaemüügiserveri rakenduse rakenduse URI**[väärtusega, mille lõite jaotises Häälestage kohandatud jaemüügiserveri Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) rakendus.

CPOS kasutab turbeluba soetustaotluste Azure AD saatmisel mõlemat parameetrit.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Identiteedi pakkujate sätete värskendamine Commerce Headquartersis

Seejärel peate värskendama identiteedi pakkujate sätteid Commerce Headquartersis.

1. Avage Commerce Headquartersis commerce’i **ühisparameetrite** leht.
1. Valige vahekaardil **Identiteedi pakkujad jaotises** Identiteedi **pakkujad rida,** kus väli **Tüüp** **Azure Active Directory** **on seatud ja väli Väljastaja osutab teie rentnikule.** Azure AD See säte deklareerib, et töötate koos tütarruudustikega, mis sisaldab teie rentnikule vastava ID pakkujaga seotud Azure AD andmeid.
1. Valige jaotises **Sõltuvad osapooled** suvand **Lisa**, et rida lisada.
1. Seadistage järgmised väljad.

    - **ClientId: sisestage** kohandatud CPOS-rakenduse **rakenduse (kliendi) ID**[väärtus, mille lõite jaotises Kohandatud CPOS-rakenduse Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) häälestamine.
    - **Tüüp** – valige **avalik**.
    - **UserType** – valige **töötaja**.

1. Valige rida, mille lisate. Jaotise **Toetudvad osapooled** **ressursi** ID-d näitavad jaemüügiserveri rakenduse ID-sid, mille saate kasutada rakendusele, mille valisite toetudesolevate osapoolte ruudustikus.**·**
1. Valige jaotises **Serveri ressursi ID-d** **suvand** Lisa rea lisamiseks.
1. Sisestage **serveri ressursi ID** väljale kohandatud jaemüügiserveri rakenduse URI **väärtus**, [mille lõite jaotises Häälestage kohandatud jaemüügiserveri Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) rakendus.

    > [!IMPORTANT]
    > Kõik eelnevas etappides kirjeldatud väljad on case-tundlikud. Sisestadavad väärtused peavad täpselt ühtima halduskeskuses konfigureeritud Azure AD väärtustega.

1. Minge jaemüügi **ja äri IT jaotusgraafikusse \>** ja käivitage **1110 (** globaalne **konfiguratsioon**) töö.

Nüüd saate CPOS-seadmeid aktiveerida oma rakenduse Azure AD abil.

## <a name="additional-resources"></a>Lisaressursid

[Müügikoha (POS) seadme aktiveerimine](dev-itpro/retail-device-activation.md)

[Aktiveerimiskontode haldamine ja seadmete kinnitamine](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
