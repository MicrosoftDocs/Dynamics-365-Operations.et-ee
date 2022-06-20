---
title: Topeltkirjutusprobleemide tõrkeotsing finants- ja äritoiminguterakendustes
description: See artikkel pakub tõrkeotsingu teavet, mis aitab teil lahendada probleeme topeltkirjutuse mooduliga finantside ja toimingute rakendustes.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 36f7969eb0bdbc64ade14a5bb97b4b708486d226
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864568"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Topeltkirjutusprobleemide tõrkeotsing finants- ja äritoiminguterakendustes

[!include [banner](../../includes/banner.md)]



See artikkel pakub tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning rakenduste vahel Dataverse. See annab teavet, mis aitab teil lahendada probleeme topeltkirjutuse **mooduliga** finantside ja toimingute rakendustes.

> [!IMPORTANT]
> Mõned küsimused, mida see artikkel käsitleb, võivad nõuda kas süsteemiadministraatori rolli või Microsofti Azure Active Directory (Azure AD) rentniku administraatori mandaate. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Finantside ja toimingute rakenduses ei saa topeltkirjutuse moodulit laadida.

Kui te ei saa avada lehte **Topeltkirjutus**, valides tööruumis **Andmehaldus** paani **Topeltkirjutus**, on andmete integratsiooni teenus tõenäoliselt maas. Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Tõrge uue tabeli vastenduse loomise katsel

**Probleemi lahendamiseks nõutav identimisteave:** sama kasutaja, kes topeltkirjutuse seadistas.

Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut tabelit topeltkirjutuse jaoks. Vastendust võib luua ainult kasutaja, kes seadistas topeltkirjutuse ühenduse.

*Vastuse oleku kood ei näita edu: 401 (autoriseerimata).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Tõrge topeltkirjutuse kasutajaliidese avamisel

Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.

*login.microsoftonline.com keeldus ühenduse loomisest.*

Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas. Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Tõrge keskkonna linkimisel topeltkirjutusega või uue tabeli vastendamisel

**Probleemi lahendamiseks on nõutav roll: süsteemiadministraator** nii finantside ja toimingute rakendustes kui ka rakenduses <a0/&Dataverse.

Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube. See tõrge võib ilmneda ka siis, kui teenuse Dataverse keskkond lähtestati ilma topeltkirjutuse linkimist tühistamata. Iga kasutaja, kellel on süsteemiadministraatori roll nii finantside kui ka toimingute rakendustes, Dataverse ja saab keskkondi linkida. Uusi tabeli vastendusi saavad lisada ainult kasutajad, kes seadistasid topeltkirjutuse ühenduse. Pärast seadistamist saab iga süsteemiadministraatori rolliga kasutaja olekut jälgida ja vastendusi redigeerida.

## <a name="error-when-you-stop-the-table-mapping"></a>Tõrge tabeli vastendamise peatamisel

Kui proovite peatada tabeli vastendust, võidakse kuvada järgmine tõrketeade.

*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*

See tõrge ilmneb siis, kui lingitud Dataverse'i keskkond ei ole saadaval.

Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet. Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Lubage paralleeltöötlus finantside ja toimingute rakendustes jõudluse parandamiseks.

Paralleeltöötluse lubamine võib vähendada aega, mis on vajalik andmete importimiseks Dynamics 365 Microsoft Dataverse kliendikogemuse rakendustest ja finantside ja toimingute rakendustesse. 

Finantside ja toimingute rakendustes paralleeltöötluse lubamiseks viige lõpule järgmised sammud.

1. Logige sisse oma finantside ja toimingute keskkonda.
2. Minge andmehalduse **> parameetritesse**.
3. Valige **Üksuse sätted ja** valige suvand **Konfigureeri üksuse käivitamise parameetrid**.
4. Lisage paralleeltöötluse parameetrid:
    - **Impordi piirmäära kirjete arv** – kirjete arv, mis tuleb enne paralleeltöötluse lubamist täita.
    - **Impordi ülesannete arv** – lõimede (ülesannete) arv, mis tuleb paralleelselt käitada.
5. Valige käsk **Salvesta**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Tabeli vastendamise alustamise katsel ilmnesid tõrked

### <a name="unable-to-complete-initial-data-sync"></a>Algset andmete sünkroonimist ei saa lõpetada

Andmete esialgse sünkroonimise käivitamisel võidakse kuvada järgmine tõrketeade:

*Esialgset andmete sünkroonimist ei saa lõpule viia. Tõrge: topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: topeltkirjutuse otsingu metaandmete koostamine pole võimalik. Tõrkeobjekti viide pole seatud objekti eksemplarile.*

Kui proovite seada vastenduse olekut väärtusele **Töötab**, võite saada järgmise tõrketeate. Selle tõrke parandus sõltub tõrke põhjusest:

+ Kui vastendusel on sõltuvaid vastendusi, siis veenduge, et selle tabeli vastendusest sõltuvad vastendused oleksid lubatud.
+ Vastendusel võivad puududa lähte- või sihtveerud. Kui finantside ja toimingute rakenduse veerg puudub [,](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) järgige kaartide väljaminek Puuduva tabeli veergude juhiseid. Kui veerg on teenuses Dataverse puudu, klõpsake vastendusel nuppu **Värskenda tabeleid**, et veerud täidetaks vastenduses automaatselt.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Versiooni lahknevuse tõrge ja topeltkirjutuslahenduste täiendamine

Tabeli vastendamise käivitamisel võidakse kuvada järgmised tõrketeated:

+ *Kliendigrupid (msdyn_customergroups) : topeltkirjutuse tõrge – Dynamics 365 for Sales lahendusel 'Dynamics365Company' on versiooniviga. Versioon: '2.0.2.10' Nõutav versioon: '2.0.133'*
+ *Dynamics 365 for Sales lahendusel 'Dynamics365FinanceExtended' on versiooni lahknevus. Versioon: '1.0.0.0' Nõutav versioon: '2.0.227'*
+ *Dynamics 365 for Sales lahendusel 'Dynamics365FinanceAndOperationsCommon' on versiooni lahknevus. Versioon: '1.0.0.0' Nõutav versioon: '2.0.133'*
+ *Dynamics 365 for Sales lahendusel 'CurrencyExchangeRates' on versiooni lahknevus. Versioon: '1.0.0.0' Nõutav versioon: '2.0.133'*
+ *Dynamics 365 for Sales lahendusel 'Dynamics365SupplyChainExtended' on versiooni lahknevus. Versioon: '1.0.0.0' Nõutav versioon: '2.0.227'*

Probleemide lahendamiseks värskendage topeltkirjutuslahendusi rakenduses Dataverse. Veenduge, et see täiendaks uusimale lahendusele, mis vastab nõutud lahenduse versioonile.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
