---
title: Tehnilise muudatuse haldamise jaoks ühiste väärtuste loomine
description: Selles teemas kirjeldatakse, kuidas luua ühiseid väärtusi, mida kasutatakse tehnilise muudatuse haldamise eri osade parameetrite korral.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b46bc10f8b75a58b8baefd88aa6a0b79c59d6544
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005398"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Tehnilise muudatuse haldamise jaoks ühiste väärtuste loomine

[!include [banner](../includes/banner.md)]

Kui seadistate tehnilise muudatuse haldamist, tuleb teil kehtestada mitu väärtuste kogumit, mida kasutatakse ripploendite täitmiseks kasutajaliidse (UI) teistes osades. Peaksite määrama need väärtused vastavalt toodetavatele toodetele ja ettevõtte vajadustele.

## <a name="engineering-change-categories"></a>Tehnilise muutmise kategooriad

Saate kasutada tehnilise muudatuse kategooriaid, et organiseerida oma tehnilise muudatuse tellimusi, et neid oleks lihtsam hallata ja üle vaadata. Näiteks võib osutuda kasulikuks seadistada töövoog, kus sõltuvalt kategooriast peab konkreetne osakond läbi vaatama pakutud muudatused. Seetõttu sisaldab tehnilise muudatuse tellimus välja **Kategooria**.

Teie ettevõttes kasutatavate tehnilise muudatuse kategooriate kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse kategooriad**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

## <a name="engineering-change-priorities"></a>Tehnilise muutmise prioriteedid

Te kasutate tehnilise muudatuse prioriteete, et näidata tehnilise muudatuse tellimuse olulisust või kiireloomulisust. Need aitavad teil jälgida tehnilise muudatuse tellimuse olulisust, et saaksite hõlpsalt tuvastada, milliseid tellimusi tuleb esmalt töödelda ja kui kiiresti.

Teie ettevõttes kasutatavate tehnilise muudatuse prioriteetide kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse prioriteedid**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

## <a name="engineering-change-reasons"></a>Tehnilise muudatuse põhjused

Tehnilise muudatuse põhjused näitavad muudatuse tellimuses oleva muudatuse põhjust või olemust.

Teie ettevõttes kasutatavate tehnilise muudatuse põhjuste kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse põhjused**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

## <a name="material-disposal-codes"></a>Materjali likvideerimise koodid

Materjalilikvideerimiskoode kasutatakse selleks, et kategoriseerida materjale, mida kasutatakse teie valmis kaupades, või komponente, mis tuleb kindlal viisil likvideerida või mida tuleb töödelda, enne kui need saab lisada tavaprügisse. Kui lisate asjakohase toote tehnilise muudatuse tellimusele, saate muudatuse üksikasjade osana määrata likvideerimiskoodi.

Teie ettevõttes kasutatavate materjalilikvideerimiskoodide kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Materjalilikivideerimiskoodid**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

## <a name="received-customer-approval"></a>Saadud kliendi nõusolek

Kui kujundaute tooteid kindlale kliendile, tuleb kavand ja spetsifikatsioonid sageli enne toote valmis märkimist kinnitada. Väli **Saadud kliendi nõusolek** võimaldab teil näidata, kui kaugele on toode kliendi nõusolekprotsessis jõudnud ja/või kas nõusolek on saadud.

Teie ettevõttes kasutatavate saadud kliendi nõusolekuväärtuste kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Saadud kliendi nõusolek**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Tehniline muudatus – keskkonnatervise ja -ohutuse normid

Kui toote tootmise käigus tuleb arvestada standardseid keskkonnatervise ja -ohutusnõudeid või ettevõttes kehtivaid nõudeid või toiminguid, saate nende määratlemiseks kasutada keskkonnatervise ning -ohutuse norme. Saate tehnilise muudatuse tellimuses näidata, milliseid norme rakendatakse toote tootmisel, kui redigeerite mõjutatud toote üksikasju.

Teie ettevõttes kasutatavate tervise ja ohutusväärtuste kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Tehniline muudatus – keskkonnatervise ja -ohutuse normid**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

## <a name="engineering-change-severities"></a>Tehnilise muutmise raskusastmed

Tehnilise muudatuse raskusastmeid kasutatakse, et näidata mõju toodetele, mis on tehnilise muudatuse tellimuses.

Teie ettevõttes kasutatavate tehnilise muudatuse raskusastmete kogumi loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse raskusastmed**. Seejärel saate kasutada tegevuspaani nuppe, et lisada, eemaldada ja redigeerida väärtusi ning järjestada need nii, nagu need tuleks kuvada ripploendites.

Saate luua reeglid, mis rakenduvad iga raskusastme korral, mida loote. Lisateavet nende reeglite määramise kohta leiate järgmisest jaotisest.

## <a name="engineering-change-severity-rule-sets"></a>Tehnilise muutmise raskusastme reeglistikud

Tehnilise muudatuse raskusastmereeglistikke kasutatakse, et luua reeglite grupp, mida saate kasutada muudatuse tellimuse raskusastme automaatseks arvutamiseks, mis põhineb mõjutatud toodete muudatuste tüübil. Raskusastme reeglite kasutamiseks avage leht **Tehnilise muudatuse haldamise parameetrid** ja määrake välja **Raskusastme reegel** väärtuseks *Arvuta* või *Arvuta automaatselt*.

Kui süsteem hindab raskusastet, töötleb see reegleid järjestuses, milles nad lehel ülalt alla ilmuvad. Reegli valimiseks ja selle prioriteedi määramiseks peavad kõik reeglistiku reeglid olema täidetud.

Et seadistada reeglid, mis rakenduvad iga muudatuse raskusastme korral, mille olete määratlenud, minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse raskusastmereeglistik**. Seejärel järgige üht neist sammudest.

- Uue reeglistiku loomiseks valige toimingupaani nupp **Uus** ja seejärel seadistage väljad, nagu on kirjeldatud allpool.
- Olemasoleva reeglistiku redigeerimiseks valige see loendipaanilt, valige toimingupaanil nupp **Redigeeri** ja seejärel häälestage väljad nii, nagu on kirjeldatud allpool.
- Olemasoleva reeglistiku kustutamiseks valige see loendipaanil ja valige seejärel toimingupaanil nupp **Kustuta**.
- Reeglistike loendi ümberkorraldamiseks valige loendipaanilt soovitud reeglistik ja seejärel kasutage toimingupaanil nuppe **Üles** ja **Alla**, et see ümber paigutada.

Seadistage iga reeglistiku korral järgmine väli.

- **Raskusaste** – valige raskusaste, mille jaoks reeglid luuakse. Astmete loomiseks ja neile nime panemiseks saate kasutada lehte **Tehnilise muudatuse raskusastmed**. (Lisateavet leiate eelmisest jaotisest.)

Kasutage kiirkaardil **Reeglid** olevaid nuppe, et lisada või eemaldada reegel praeguse raskusastme sätte jaoks. Igal reeglil on väljad **Reegel** ja **Nimi**. Reeglid kehtestab süsteem ja need näitavad muudatuste tüüpe, mida toode võib hõlmata. Nimi näitab muudatuse tüüpi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]