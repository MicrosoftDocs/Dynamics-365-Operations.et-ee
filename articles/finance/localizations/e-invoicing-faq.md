---
title: Elektroonilise arvelduse KKKd
description: Selles teemas antakse teavet korduma kippuvate küsimuste kohta seoses elektroonilise arveldamisega.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1ba1a6c5542c10306d4b7494d33e7ff04504fa95
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893774"
---
# <a name="electronic-invoicing-faq"></a>Elektroonilise arvelduse KKKd

[!include [banner](../includes/banner.md)]

Selles teemas antakse vastused korduma kippuvate küsimustele elektroonilise arveldamise kohta. Elektrooniline arveldamine laiendab elektroonilise arveldamise võimalusi, mis on olemas Dynamics 365 Finance, Dynamics 365 Supply Chain Management ja Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Mis on elektroonilise arveldamise puhul oluline ja miks peaks see olema minu organisatsioonile oluline?

Tegevus keerukus ja riski kasvamine jätkub, kui organisatsioonid kasvavad globaalselt ja laiendavad oma tegevusi kõikides piirkondades. Vastavuse haldamine ja regulatsioonide sagedaste muudatustega kohanemine on kasvav väljakutse ning on eriti oluline arvete koostamisel. Arvete koostamine on ajalooliselt olnud kallis ja vigadele kalduv, sest firmad loodavad paberdokumentidele ja käelist tööd nõudvatele protsessidele.  

Organisatsioonid on alustanud paberarvelt eemaldumist, et vähendada kulusid ja kiirendada tervikprotsessi. Valitsusedki pöörduvad üha rohkem elektroonilise arveldamise poole, mis on maksude digitaliseerimise põhikomponent. Nõudes organisatsioonidelt, et need esitaks maksuteavet maksuametile reaalajas ja digitaalselt, saavad valitsused vähendada maksudest kõrvalehiilimist ja manipulatsioone ning vähendada pettuset. 

Maailm liigub paberivaba dokumenditöötluse suunas ja ilma elektroonilist arveldust rakendamata riskivad kliendid vastavuse probleemide, mittevajalike kulude ja konkurentsidet mahajäämisega. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Kas finantsid, Supply Chain Management ja Project Operations ei sisalda juba elektroonilist arveldamise funktsiooni? Millist väärtust see mulle kliendina pakub? 

Elektrooniline arveldamine laiendab elektroonilise arvelduse võimalusi, mis on olemas finantsides, Supply Chain Management -is ja Project Operations -is. Funktsioonid lihtsustavad ka uusimate elektrooniliste arveldusstandardite kinnipidamist ja tagab elektroonilise arve töötlemise ja vahetuse erinevatest geograafidest saadud kogemused. Elektroonilise arveldamise võimalused vabastavad soodustuste massiivi, sealhulgas: 

   - Kiirem ja lihtsam riigi-/piirkonnapõhiste nõuete kasutuselevõtt.
   - E-arve lahenduse rakenduste rakenduste standartimine. 
   - Täiustatud e-arve töötlemise jälitatavus.  
   - Lihtsam hooldus vastamaks muutuvatele seaduslike nõuetele ja kohalikele äritavadele. 
   - Lihtsustatud lahenduse pakend.
   - Suure hulga esitatud dokumentide mahu skaleerimise tulemuseks on kiirem ringlus.
   - Võime oma lahendusi teiste ettevõtetega jagada.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Kas elektrooniline arveldamine toetab kohapealset finantside ,Supply Chain Management -i ja Project Operations -i installeerimist? 

Praegune platvorm ei luba kasutada kohapealset versiooni ja seda ei plaanita tulevikus toetada.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Kas elektroonilise arveldamise liides koos hankija impordi automatiseerimise funktsiooniga?

Ei. Selle liidese jaoks on plaane, kuid planeeritud ajajoont pole. Kui see on planeeritud, siis kuupäevad teatatakse [Väljaandmise kavas](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Kuidas elektroonilise arveldamine tegeleb faili manustega elektroonilisel arvel? Kas SharePoint -i serverit on vaja PDF failide kaasamiseks XML failidesse?

Elektroonilise arvega seotud faile käsitsetakse XML-elemendis kaasatud kahendandmetena. SharePoint -i serverit ei ole vaja PDF failide kaasamiseks, aga manus peab olema salvestatud  finantside, Supply Chain Management -i ja Project Operations -i dokumendihaldussüsteemi.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Kas elektrooniline arveldamine on saadaval vastavalt minu riigi/regiooni määrustele?

Elektrooniline arveldamine on mikroteenuste platvorm, mis on globaalselt saadaval.

Microsoft plaanib avaldada elektroonilise arve vormingud ja integratsioonid riikidesse, mille Microsoft on funktsioonilt lokaliseerinud. Lisateavet vt teemast [Elektroonilise arveldamise funktsioonide saadavus](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Kui teie riigi/regiooni elektroonilist arveldusvormingut pole loendis, pakub platvorm seda stsenaariumi tulevikus toetada. Elektroonilise arveldamise konfiguratsioonivõimalustest on siiski kasu ja elektroonilise arveldamise vormingut saate ise konfigureerida või saate töötada partneri/ISV-ga nende konfigureerimiseks teie organisatsiooni jaoks.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Kas Dynamics 365 for Regulatory Services on uus moodul nagu Inimressursid või Project Operations, mis on seotud finantside või Supply Chain Management -iga? Kas selle eest on lisakulusid?

Dynamics 365 Regulatory Services (RCS) on pilveteenus globaliseerimisressursside konfigureerimiseks. RCS on tasuta kõigile finantside, Supply Chain Management -i ja Project Operations -i litsentsiomanikele.

RCS-i registreerimiseka minge <https://marketing.configure.global.dynamics.com/>.

Lisateavet vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Kas ma pean end registreerima, et saada elektroonilist arveldamist või lülitan selle lihtsalt funktsioonihalduses sisse?

Kui teil on finants-, Supply Chain Management -i ja Project Operations -i litsents, vaadake [Alusta elektroonilise arveldamise lisandmooduli teenuse administreerimisega](e-invoicing-get-started-service-administration.md) et registreerida elektroonilisele arveldusele.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Kas elektrooniline arveldamine töötab järguga 1 virtuaalmasinates? Milline on minimaalne nõutav keskkond?

Elektroonilise arveldamisega integreerimine nõuab vähemalt 2. järgu virtuaalmasinat finants- või Supply Chain Management -i hostimiseks. Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Kas elektroonilisel arveldamisel on testrežiim arve esitamise testimiseks?

Selle saab saavutada konfiguratsiooni abil. Arve esitamise testimiseks saate ühendada finantside või Supply Chain Management -i vormi kasutaja kinnitamiskatse (UAT) keskkonnast ja esitada testarved. Elektrooniline arveldamine toetab test-digitaalsete sertifikaadide konfigureerimist ja kui e-arved nõuavad digitaalset kinnitust, siis url-i seadistus test-veebiteenustest, mille on avaldatnud maksuamet.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Kas on olemas dokumentatsiooni valmis riigipõhiste elektroonilise arveldamise funktsioonide kohta?

Jah. Teavet elektroonilise arveldamise funktsioonide saadavuse ja nende toetatud vormingute kohta vaadake [Elektrooniliste arveldus funktsioonide saadavus](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Kui te ei leidnud otsitavat vastust, saatke e-kiri oma küsimusega tootearenduse töörühma <D365EInvoicePreview@microsoft.com>. Me kas võtame ühendust või parandame seda KKK-d.