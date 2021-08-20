---
title: Kinnipeetava maksu deklaratsioon Egiptuse jaoks
description: Käesolev teema kirjeldab, kuidas konfigureerida ja luua Egiptuse kinnipeetava maksu deklaratsioone.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 51f0ab8f76fe3bce91d6e4ed56bdfa8529c1aacbd326a8b4b3d80615f872f8c6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729547"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Kinnipeetava maksu deklaratsioon Egiptuse jaoks (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Ülevaade
See teema kirjeldab, kuidas seadistada ja luua kinnipeetava maksu deklaratsioone ning kinnipeetava maksu deklaratsiooni vorme 41 ja 11 Egiptuse juriidilistele isikutele 

Kõik Egiptuse üksused peavad ette valmistama vormi 41, mis võtab kokku kõik maksud, mis on kinnipeetud kohalikelt hankijatelt ja tarnijatelt. Lisaks vormile 41 tuleb luua vorm 11 kõigi välismaiselt pakkujatelt kinnipeetud maksu üksikasjade jaoks. 

Kinnipeetava **Maksu deklaratsiooni** aruanne sisaldab järgmisi Dynamics 365 Finance aruandeid:

- Deklaratsiooni vormi number. 41
- Deklaratsiooni vormi number. 11
    
    
## <a name="prerequisites"></a>Eeltingimused
Juriidilise isiku peamine aadress peab olema Egiptuses.
Tööruumis **Funktsioonide haldus**, lülitage sisse järgmised funktsioonid:

   - **Globaalne kinnipeetav maks**

Lisateavet funktsioonide lubamise kohta, vaata [Funktsioonihalduse ülevaade.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. Avage **Maks** > **Seadistus** > **Parameetrid** > **Pearaamatu parameetrid** ja seejärel seadistage vahekaardil **Kinnipeetav maks** suvand **Luba globaalne kinnipeetav maks** olekusse **Jah**.
2. **Elektroonilise aruandluse** tööruumis importige hoidlast järgmised elektroonilise aruandluse vormingud:

    - WHT deklaratsioon Excel (EG)

    > [!NOTE]
    > Ülaltoodud vorming põhineb **maksudeklaratsiooni mudelil** ja kasutab **maksudeklaratsiooni mudeli vastendamist**. See lisakonfiguratsioon imporditakse automaatselt.

Lisateavet selle kohta, kuidas importida elektroonilise aruandluse konfiguratsioone, vaata [Elektrooniliste aruannete konfiguratsioonide allalaadimine Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine

Egiptuse deklaratsioonivormide rakendamine põhineb elektroonilise aruandluse (ER) konfiguratsioonil. Lisateavet konfigureeritava aruandluse võimaluste ja mõistete kohta vaata [Eektroonilisest aruandlusest](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Tootmise ja kasutaja aktsepteerimise testimiseks (UAT) keskkonnad järgige teema juhiseid, [Laadige alla elektroonilise aruandluse konfiguratsioonid Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Kinnipeetavate deklaratsioonide loomiseks Egiptuse juriidilises isikus, peate üles laadima järgmised konfiguratsioonid:

- Maksudeklaratsiooni model.version.82.xml või uuem versioon
- Maksudeklaratsioon model.version.82.xml või uuem versioon
- WHT deklaratsioon Excel (EG.version.82.21 või hilisem versioon)

Pärast ER-i konfiguratsioonide allalaadimist Lifecycle Services (LCS) või globaalsest hoidlast viige lõpule järgmised sammud.

1. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
1. Lehel **Konfiguratsioonid** valige tegevuspaanil **Vahetuskursi laadimine XML-failist**.
1. Laadige üles kõik failid eelmise täpi loendis toodud järjestuses. Pärast kõigi konfiguratsioonide üles laadimist peaks konfiguratsioonipuu olema finantsis.

## <a name="set-up-application-specific-parameters"></a>Seadistage rakenduspõhised parameetrid

Rakendusespetsiifiliste parameetrite valik võimaldab kasutajatel määrata kriteeriumid, kuidas maksukanded igal loodud aruande real klassifitseeritakse ja arvutatakse, sõltuvalt **kinnipeetava maksu kaubagrupi** konfiguratsioonist või muudest otsingu määratluse kriteeriumitest.

Kinnipeetava deklaratsiooni vorm 41 sisaldab konkreetset veergu, kus kinnipeetava maksu kanne tuleb klassifitseerida vastavalt maksuameti klassifikatsioonile nimega **Allahindluse koodi tüüp**. Selle asemel, et lisada need uued klassifikatsioonid kannete sisestamisel uuteks sisestusandmeteks, määratakse klassifikatsioonid konfiguratsioonides tehtud erinevate otsingute alusel, mida on tutvustatud **Konfiguratsioonid** > **Seadistage rakendusomased parameetrid** > **Seaded** nii, et need vastaksid Egiptuse kinnipeetavate aruannet nõuetele. 

Järgmist konfiguratsiooni kasutatakse kannete klassifitseerimiseks kinnipeetava deklaratsiooni vormis 41 aruandes:

- **DiscountTaxTypeLookup** -> veerg nr 18 

Viige lõpule järgmised sammud erinevate otsingute häälestamiseks, mida kasutatakse "Mis deklaratsioon ja seotud raamatute aruanded" loomiseks. 

1. **Elektroonilise aruandluse** tööruumis valige **konfiguratsioonide** > **Häälestus**, et seadistada reeglid kannete klassifitseerimise tuvastamiseks Deklaratsiooni aruandes. 
2. Valige praegune versioon ja valige **Otsingud** otsingunime kiirkaardil. Näiteks **DiscountTaxTypeLookup**. See otsing tuvastab maksuhalduri nõutavate allahindlustüüpide loendi.
3. Suvandis **Tingimused** valige kiirkaardil klassifikatsiooni veerus **Lisa** ja uuel real **Otsingu tulemused** veerus valige klassifikatsiooniga **18** seotud rida.
4. Veerus **Kinnipeetava maksu kaubagrupp** valige seotud kood, mida kasutatakse klassifikatsiooni tuvastamiseks. Näiteks **Lubatud allahindlus**.  
5. Korrake samme 3 ja 4 kõigi saadaval otsingute puhul.
6. Lõppkirje rea kaasamiseks klõpsake uuesti nuppu **Lisa** ja valige **otsingutulemuse** veerus suvand **Pole rakendatav**. 
7. Ülejäänud veergudes valige **Mitte tühi**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Seadistage pearaamatu parameetrid

WHT deklaratsioonivormi aruannete loomiseks Microsoft Excel, määratlege ER formaat **pearaamatu parameetrite** lehel.

1. Minge **Maksu** > **Seadistamise** > **pearaamatu parameetritesse**.
2. Vahekaardil **Kinnipeetav maks** väljal **WHT deklaratsiooni vormingu vastendamine** valige **WHT Deklaratsioon Excel (EG)**. Kui jätate selle välja tühjaks, luuakse standardne käibemaksuaruanne SSRS-vormingus.


![Deklaratsiooni vorm.](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Kinnipeetava deklaratsiooni vormide loomine
Konkreetse perioodi kinnipeetava deklaratsiooni vormi ettevalmistamine ja esitamine põhineb kinnipeetava maksu kannetel, mis sisestati tasakaalustamise ja maksemaksu sisestamise ajal. Lisateavet globaalse kinnipeetava maksu kohta vt [globaalsest kinnipeetavast maksust](../general-ledger/global-withholding-tax-overview.md).

Maksudeklaratsiooni aruande loomiseks viige lõpule järgmised sammud.

1. Minge **Maksu** > **Deklaratsioonidesse** > **Kinnipeetav maks** > **Kinnipeetava maksu makse*.
2. Valige tasakaalustusperiood ja seejärel valige aruande alguskuupäev. 
3. Sisestage makse kuupäev ja seejärel valige **OK**.
4. Avanev dialoogiboksis valige üks või mitu vormitüüpi **Vorm No 41**, **Vorm Nr 11** või **Pole**. Kui valite **Pole**, luuakse standardaruanne. 
5. Keele valimine. Kõik aruanded tõlgitakse **en-us** ja **ar-eg**.
6. Sisestage selle panga haru ja nimi, kus maksumakse tasutakse.
7. Valige ettevõtte tüüp ning seejärel sisestage tšeki- ja dokumendinumbrid. 
8. Vaadake üksuse tüüpi. 
9. Sisestage vormi määramiseks registreeritud isiku nimi ja valige **OK** aruande loomise kinnitamiseks. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
