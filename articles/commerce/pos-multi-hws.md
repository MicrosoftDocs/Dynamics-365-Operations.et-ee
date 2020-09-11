---
title: Sihtotstarbelised makseterminalid ja printeri ja sularahasahtli viibad
description: See teema annab teavet sihtotstarbelise makseterminali omamise võimaluse kohta ja palub kasutajal valida sularahasahtli ja kviitungiprinteri.
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 03cb68ede82668523e6970d33df676738e65fd83
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719210"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Sihtotstarbelised makseterminalid ja printeri ja sularahasahtli viibad

[!include [banner](includes/banner.md)]

See teema annab teavet sihtotstarbelise makseterminali omamise võimaluse kohta ja palub kasutajal valida sularahasahtli ja kviitungiprinteri.

## <a name="overview"></a>Ülevaade

Kaasaegsed jaemüüjad otsivad võimalusi kaupluse ostukogemuse täiustamiseks. Hiljutised suundumused paberivaba ostlemise suunas elektrooniliste makseviiside kaudu ei aita mitte üksnes muuta ostukogemust sujuvamaks, vaid vähendavad ka vajadust igale poemüüjale kättesaadavate välisseadmete täiskomplekti järele.

Microsoft Dynamics 365 Commerce toetab nimetatud suundumusi, võimaldades kasutada kassaseadet, mis on igal ajal varustatud sihtotstarbelise makseterminaliga, kuid millel puuduvad kviitungiprinter ja sularahasahtel. Kui poemüüjad peavad printima kviitungi või võtma vastu sularahamakse, siis saavad nad valida riistvarajaama, kus antud seadmed on konfigureeritud.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Registreerimine | Üksus, mida kasutatakse kassaaparaadi eksemplari konfigureerimiseks. |
| Seade | Kassaaparaadi füüsilise eksemplari ja sellele määratud rakenduse Modern POS kujutis. |
| Sihtotstarbeline riistvarajaam | Riistvarajaama äriloogika, mis on integreeritud rakendustesse Modern POS Windowsile ja Modern POS Androidile. |
| Sahtli avamise (d/k) port | Tavaline meetod sularahasahtli ühendamiseks kviitungiprinteriga. |
| Võrgu välisseadmed | Võrgutoega makseterminalide, kviitungiprinterite ja sularahasahtlite sisseehitatud tugi. |

## <a name="supported-pos-clients-and-devices"></a>Toetatud kassa kliendid ja seadmed

Selles teemas kirjeldatud funktsionaalsust toetavad kassa klientidele mõeldud rakendused Modern POS Windowsile ja Modern POS Androidile.

See funktsionaalsus toetab võrgutoega makseterminale ja kviitungiprintereid. Te võite pakkuda ka sularasahtli tuge, ühendades sularahasahtli d/k pordi kaudu võrgutoega kviitungiprinteriga.

Valmiskujul funktsionaalsusele pakub tuge [Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Teised makseterminalid võivad olla aga varustatud Commerce'i maksete jaoks mõeldud tarkvaraarenduse komplekti toega. Toetatavad kviitungiprinterid on näiteks Star Micronicsi ja Epsoni võrgutoega kviitungiprinterid.

Star Micronicsi kviitungiprinteri ülesseadmiseks kasutage seadme konfigureerimiseks Star Micronics printeri utiliiti, et seda saaks kasutada võrgus. Utiliit annab seadmele ka IP-aadressi.

Epsoni printerite ülesseadmiseks kasutage Epson ePOS-Print utiliiti, et seadistada seade kasutama võrguprotokolle.

Lisateavet võrguseadmete seadistamiseks vt teemast [Võrgu välistoe ülevaade](https://go.microsoft.com/fwlink/?linkid=2129965).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Sihtotstarbelise makseterminali ja printeri ja sularahasahtli viiba seadistamine

### <a name="set-up-hardware-profiles"></a>Riistvaraprofiilide häälestamine

Vajate kaht tüüpi riistvaraprofiili. Esimene on määratud kassale. Teine on määratud kaupluse tasandil riistvarajaamale ja seda kasutatakse võrgusiseste kviitungiprinterite ja sularahasahtlite loogiliseks grupeerimiseks.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Kassa riistvaraprofiili seadistamine

Kassale määratud riistvaraprofiili seadistamiseks toimige järgmiselt.

1. Leidke rakenduses Dynamics 365 Commerce suvand **Riistvara profiil**.
2. Valige suvand **Uus**.
3. Määrake riistvaraprofiili number ja seejärel sisestage kirjeldus. See riistvaraprofiil lisatakse kassale endale. Seega piisab, kui panna kirjelduseks **Sihtotstarbeline koos varuga**.
4. Seadistage erinevate seadmetüüpide kiirkaartidel järgmised seadmetüübid.

    | Seade | Tüüp | Seadme nimi | Täiendavad üksikasjad |
    |---|---|---|---|
    | Printer | Taane | *Mõni* | Seadme nimi on tõstutundlik. **Kviitungiprofiili ID** peaks olema sama, mis kanali tasandil riistvarajaamale määratud riistvaraprofiilis seadistatud võrguprinteriga vastendatud **Kviitungiprofiili ID**. |
    | Sularahasahtel | Taane | *Mõni* | Seadme nimi on tõstutundlik. Valige suvandi **Kasuta ühist vahetust** sätteks **Jah**. |
    | Elektroonilise ülekande (EFT) teenus | Adyen | Pole kohaldatav | Valmiskujul Adyeni konnektori seadistamise kohta lisateabe saamiseks vt teemat [Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Teised makseterminalid võivad olla varustatud [Commerce'i maksete jaoks mõeldud tarkvara arenduse komplekti toega](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension). |
    | PIN-klahvistik | Võrk | **MicrosoftAdyenDeviceV001** | Puudub. |

5. Leidke rakenduses Dynamics 365 Commerce suvand **Kassad**.
6. Valige kassanumbri järgi kassa ning seejärel **Redigeeri**.
7. Määrake kassale, mis peaks kasutama sihtotstarbelist makseterminali, äsja loodud riistvaraprofiil. Kassale vastendatud seade peab kasutama rakendust Modern POS Windowsile või rakendust Modern POS Androidile.
8. Valige käsk **Salvesta**.
9. Toimingupaanil vahekaardil **Kassad** valige suvand **Konfigureeri IP-aadressid**.
10. Sisestage kiirkaardil **PIN-klahvistik** makseterminali IP-aadress. Lisateavet selle kohta, kuidas saada Adyen konnektori abil makseterminali IP-aadress, vt teemast [Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).
11. Valige käsk **Salvesta**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Kviitungiprinteri ja sularahasahtli riistvaraprofiili seadistamine

Võrgusisese kviitungiprinteri ja sularahasahtli grupeerimiseks kasutatava riistvaraprofiili seadistamiseks toimige järgmiselt.

1. Leidke rakenduses Dynamics 365 Commerce suvand **Riistvara profiil**.
2. Valige suvand **Uus**.
3. Määrake riistvaraprofiili number ja seejärel sisestage kirjeldus. Riistvaraprofiili kasutatakse kviitungiprinteri ja sularahasahtli grupeerimiseks. Seega piisab, kui panna kirjelduseks **Võrgusisene printer ja sularahasahtel**.
4. Seadistage erinevate seadmetüüpide kiirkaartidel järgmised seadmetüübid.

    | Seade | Tüüp | Kirjeldus | Täiendavad üksikasjad |
    |---|---|---|---|
    | Printer | Võrk | **Epson** või **Star** | Seadme nimi on tõstutundlik. **Kviitungiprofiili ID** peaks olema sama, mis kassale määratud riistvaraprofiilis seadistatud võrguprinteriga vastendatud **Kviitungiprofiili ID**. |
    | Sularahasahtel | Võrk | **Epson** või **Star** | Seadme nimi on tõstutundlik. Valige suvandi **Kasuta ühist vahetust** sätteks **Jah**. |

5. Valige käsk **Salvesta**.

### <a name="set-up-hardware-stations"></a>Riistvarajaamade seadistamine

Teil peab olema kaks riistvarajaama. Esimene on vastendatud kassale. Teine valitakse vastavalt sellele, kas tuleb printida kviitung või avada sularahasahtel.

#### <a name="register-a-hardware-station"></a>Riistvarajaama registreerimine

1. Leidke rakenduses Dynamics 365 Commerce suvand **Kõik poed**.
2. Valige **Jaemüügikanali ID** alusel kauplus ja seejärel **Redigeeri**.
3. Valige kiirkaardil **Riistvarajaamad** käsk **Lisa**.
4. Määrake välja **Riistvarajaama tüüp** väärtuseks **Sihtotstarbeline**.
5. Sisestage kirjeldus, kuid ärge määrake riistvarajaamale muid väärtusi. Seda riistvarajaama kasutatakse kassas kogu aeg. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Kviitungiprinteri ja sularahasahtli riistvarajaama seadistamine

1. Leidke rakenduses Dynamics 365 Commerce suvand **Kõik poed**.
2. Valige **Jaemüügikanali ID** alusel kauplus ja seejärel **Redigeeri**.
3. Valige kiirkaardil **Riistvarajaamad** käsk **Lisa**.
4. Määrake välja **Riistvarajaama tüüp** väärtuseks **Sihtotstarbeline**.
5. Sisestage kirjeldus. Riistvarajaama kasutatakse kviitungiprinteri ja sularahasahtli jaoks.
6. Valige väljal **Riistvara profiil** riistvara profiil, mille olete eelnevalt kviitungiprinteri ja sularahasahtli jaoks loonud.
7. Valige käsk **Salvesta**.
8. Samal ajal kui kviitungiprinteri ja sularahasahtli riistvarajaam on veel valitud olekus, valige **Konfigureeri IP-aadressid**.
9. Hankige printeri IP-aadress ja sisestage see nii kviitungiprinteri kui sularahasahtli IP-aadressina.
10. Valige käsk **Salvesta**
11. Otsige suvandit **Jaotusgraafikud**.
12. Valige jaotusgraafik **1090** ja seejärel **Käita kohe**.
13. Valige jaotusgraafik **1070** ja seejärel **Käita kohe**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Seadistage süsteem selliselt, et vastavalt vajadusele rakendatakse kviitungiprinteri või sularahasahtli valikut

1. Sulgege toetatud kassa kliendis praegune vahetus, kui vahetus on avatud.
2. Logige sisse ja valige **Sahtliga mitteseotud sahtli toimingud**.
3. Kasutage riistvarajaama sisse lülitamiseks suvandit **Riistvarajaamade haldamine**.
4. Riistvarajaama aktiveerimiseks valige kassa jaoks loodud riistvarajaam.
5. Logige kassast välja ning uuesti sisse ja avage vahetus.

Nüüd on makseterminalile määratud riistvaraprofiil alati aktiivne ning teile antakse teada, kui kviitungiprinteri või sularahasahtli kasutamine on vajalik.

Paljud antud funktsiooni taotlenud kaupmehed soovivad vähendada jäätmete teket, pakkudes meilikviitungeid ja soodustades elektroonilisi makseid. Kassa konfiguratsioonist sõltuvalt palutakse poemüüjatel valida kviitungiprinteri või sularahasahtli kasutamise võimalus vaid juhul, kui klient soovib füüsilist kviitungit või tahab maksta sularahas.

Kaupluse töötajad peavad valima riistvarajaama tehingu jooksul vaid ühe korra, välja arvatud juhul, kui tuleb printida kviitung või maksmiseks kasutatakse sularaha, kuid esialgselt valitud riistvaraprofiil ei hõlma mõlemat seadet. Sel juhul palutakse poemüüjal teha uus valik ja valida riistvarajaam, mida saab kasutada tehingu lõpetamiseks.

## <a name="related-articles"></a>Seotud artiklid

- [Rakenduse POS Hybrid seadistamine Androidis ja iOS-is](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [Võrgu välistoe ülevaade](https://go.microsoft.com/fwlink/?linkid=2129965)
