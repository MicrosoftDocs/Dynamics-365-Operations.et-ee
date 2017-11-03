---
title: "SEPA otsekorralduse ülevaade"
description: "Ühtse euromaksete piirkonna (SEPA) on määranud Euroopa Komisjon, kelle korraldusel tuleb kõiki elektroonilisi makseid käsitleda kodumaistena, olenemata riigist/piirkonnast, kus üksikisik, ettevõte või organisatsioon ja pank asuvad. Riiklike ja riikidevahelistel maksetel pole mingit vahet. SEPA hõlmab 28 Euroopa Liidu liikmesriiki ning samuti Islandit, Liechtensteini, Norrat, Šveitsi, Monacot ja San Marinot. SEPA aitab Euroopa majanduspiirkonnas (EMP) luua maksekannete jaoks ühtse turu. Lõppkokkuvõttes eeldatakse, et SEPA vähendab maksevormingute arvu, millega pangad, ettevõtted ja üksiksikud peavad tegelema."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bf4ad99938eb3da5e72afbad9a5440df16854606
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="sepa-direct-debit-overview"></a>SEPA otsekorralduse ülevaade

[!include[banner](../includes/banner.md)]


Ühtse euromaksete piirkonna (SEPA) on määranud Euroopa Komisjon, kelle korraldusel tuleb kõiki elektroonilisi makseid käsitleda kodumaistena, olenemata riigist/piirkonnast, kus üksikisik, ettevõte või organisatsioon ja pank asuvad. Riiklike ja riikidevahelistel maksetel pole mingit vahet. SEPA hõlmab 28 Euroopa Liidu liikmesriiki ning samuti Islandit, Liechtensteini, Norrat, Šveitsi, Monacot ja San Marinot. SEPA aitab Euroopa majanduspiirkonnas (EMP) luua maksekannete jaoks ühtse turu. Lõppkokkuvõttes eeldatakse, et SEPA vähendab maksevormingute arvu, millega pangad, ettevõtted ja üksiksikud peavad tegelema.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Mis on SEPA otsedeebetite eesmärk?
---------------------------------------

SEPA otsedeebet võimaldab kreeditoril koguda kliendi pangakontolt vahendeid eeldusel, et klient on kreeditorile andnud allkirjastatud loa. Klient allkirjastab loa, mis autoriseerib kreeditori koguma makseid ja annab kliendi pangale korralduse kogutud maksed tasuda. 

SEPA otsekorraldused loovad esmakordselt maksevahendi, mida saab 32 SEPA riigis/piirkonnas kasutada nii riiklike kui ka piiriüleste eurodes tehtavate otsekorralduste puhul. 

Saadaval on kaks skeemi: SEPA otsekorralduste tuumskeem ja SEPA ettevõtetevaheline (B2B) otsekorraldusskeem. Mõlemad skeemid kasutavad sama failivormingut.

## <a name="what-is-the-core-direct-debit-scheme"></a>Mis on otsekorralduse tuumskeem?
SEPA otsekorralduste tuumskeem on põhiskeem. Sellel on järgmised atribuudid.
-   Rahaülekanded tehakse eurodes (isegi kui pangakontol võib olla vahendeid muudes valuutades).
-   Nii kliendil kui ka kreeditoril peab olema konto krediidiasutusega, mis asub SEPA piires.
-   Klient peab kreeditorile andma allkirjastatud loa.
-   Luba aegub 36 kuud pärast viimati algatatud kogumist.
-   Kreeditor peab säilitama luba selle kehtivuse lõpuni ja vähemalt 14 kuud pärast viimast kogumist.
-   Skeemi võib kasutada ühekordseks või korduvaks otsekorralduse alusel kogumiseks.
-   Kliendil on kahtlematu õigus saada tagasimakse kuni kaheksa nädala jooksul pärast tema konto debiteerimist.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Mis on SEPA ettevõtetevaheline (B2B) otsekorraldusskeem?
SEPA B2B otsekorraldusskeem kehtib ettevõtetevahelistele kannetele ja selle aluseks on SEPA otsekorralduste tuumskeem. Peamised erinevused on järgmised.
-   SEPA B2B otsekorraldusskeem pole lubatud, kui klient on eraisik (tarbija).
-   Kliendil pole õigust saada autoriseeritud kande tagasimakset.
-   Kliendi pangad peavad veenduma, et kogumine on autoriseeritud, võrreldes kogumist loas oleva teabega. Kliendi pangad ja kliendid peavad nõustuma iga otsekorralduse puhul tehtava kontrolliga.
-   Skeem pakub lühemat ajaperioodi otsekorralduste esitamiseks ja vähendab tagastusperioodi.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Kas ma saan skeemi COR1 kasutada otsekorralduse lubade puhul?
Jah. Skeemi COR1 saab SEPA otsekorralduse mandaatide puhul kasutada Austrias, Belgias, Saksamaal, Prantsusmaal, Itaalias, Hispaanias ja Hollandis. Skeem pakub kreeditorile otsekorralduse kogumiseks lühemat eelteavitusaega.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Mis on rahvusvahelised pangakonto numbrid (IBAN) ja panga identifikaatorkoodid (BIC)?
Rahvusvahelist pangakonto numbrit (IBAN) ja panga identifikaatorkoodi (BIC) kasutatakse kõigi kontode tuvastamiseks 32 SEPA riigis/piirkonnas. Sisestage SWIFT-koodi väljale BIC ja IBAN-väljale IBAN. Mõlemad väljad asuvad lehe Pangakontod vahekaardi Pangakonto kiirkaardil Täiendav identifitseerimine. See on nii kreeditori pangakonto kui ka kliendi pangakonto puhul.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Kuhu pean sisestama kreeditori identifikaatorid (otsekorralduse ID-d)?
SEPA-s tuvastatakse iga kreeditor kreeditori ainuidentifikaatoriga. See identifikaator võimaldab kliendil ja kliendi pangal filtreerida iga otsekorraldust ja seejärel otsekorraldust töödelda või selle tagasi lükata vastavalt kliendi juhistele. Kreeditor peab identifikaatori taotlema oma panga kaudu. Sisestage see identifikaator juriidilise isiku väljale Otsekorralduse ID.

## <a name="what-are-mandates"></a>Mis on load?
Klient allkirjastab loa, mis autoriseerib kreeditori koguma makseid ja annab kliendi pangale korralduse kogutud maksed tasuda. Klient saab loa väljastada paberkandjal või elektrooniliselt. Vaikimisi aegub luba 36 kuud pärast otsekorralduse viimast algatamist.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Kus saan määrata SEPA otsekorralduse failivormingu (ISO-20022)?
SEPA andmevormingud põhinevad ISO-20022 sõnumistandarditel. Märgite ruudu Üldine elektrooniline aruandlus ja valite müügireskontro makseviiside konfigureerimisel ekspordivormingu konfiguratsioonina SEPA Directi otsedeebeti. Seda makseviisi saab kasutada maksefaili loomisel kliendi makse töölehel.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>Millistes failivormingutes saan luua SEPA otsekorralduse maksefaile?
SEPA otsekorralduste maksefaile saab luua järgmistes vormingutes.
-   Vormingus PAIN.008.001.02 XML Belgia, Saksamaa, Hispaania, Prantsusmaa, Itaalia ja Hollandi puhul.
-   SEPA otsekorralduse maksefaile vormingus PAIN.008.001.02 XML Austria ja vormingus PAIN.008.003.02 XML Saksamaa puhul.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Kuidas toimib SEPA otsekorraldustega tagasimaksmine ja tagastamine?
Mõlema SEPA otsekorraldusskeemi alusel on klientidel teatud õigused tagasimaksetele. Kliendil on lubatud kaheksa nädala jooksul pärast tähtaega mis tahes autoriseeritud kanne ilma selgitust andmata tagasi kutsuda. Autoriseerimata kannete korral pikendatakse perioodi 13 kuuni pärast tähtaega. Kõik tehtud maksed tühistatakse käsitsi, kasutades lehel Kliendi kanded olevat nuppu Tühista makse.






