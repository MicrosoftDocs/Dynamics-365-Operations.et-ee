---
title: Varude nähtavuse rakendus
description: See artikkel kirjeldab, kuidas kasutada varude nähtavuse rakendust.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306169"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility rakenduse kasutamine

[!include [banner](../includes/banner.md)]


See artikkel kirjeldab, kuidas kasutada varude nähtavuse rakendust.

Varude nähtavus annab visualiseerimiseks mudelipõhise rakenduse. Rakendus sisaldab kolme lehekülge: **Konfiguratsioon**, **Operatiivne nähtavus** ja **Varude kokkuvõte**. Sellel on järgmised funktsioonid.

- See annab kasutajaliidese (UI) vaba kaubavaru konfigureerimiseks ja esialgse reserveerimise konfigureerimiseks.
- See toetab reaalajas vaba kaubavaru päringuid eri dimensioonide kombinatsioonide kohta.
- See annab kasutajaliidese reserveerimistaotluste sisestamiseks.
- See annab toodetele kohandatud vaba kaubavaru vaate koos kõigi dimensioonidega.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist installige ja seadistage Inventory Visibility lisandmoodul, nagu on kirjeldatud jaotises [Inventory Visibility installimine ja seadistamine](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Avage Inventory Visibility rakendus

Rakenduse Inventory Visibility avamiseks logige oma Power Apps keskkonda sisse ja avage **Inventory Visibility**.

## <a name="configuration"></a><a name="configuration"></a>Konfiguratsioon

Leht **Konfiguratsioon** aitab teil seadistada Inventory Visibility rakenduse konfiguratsiooni ja esialge reserveerimise konfiguratsiooni. Pärast lisandmooduli installimist sisaldab vaikekonfiguratsioon Microsoft Dynamics 365 Supply Chain Management vaikeseadistust (`fno` andmeallikas). Vaikesätet on võimalik üle vaadata. Edaspidi vastavalt teie äritegevuse nõuetele ja välise süsteemi lao sisestusnõuetele saate muuta konfiguratsiooni lahenduses, et ühtlustada viisi, kuidas saab erinevates süsteemides varude muudatusi sisestada, korraldada ja nende kohta päringuid esitada.

Lahenduse konfigureerimise täielikud üksikasjad leiate jaotisest [Inventory Visibility konfigureerimine](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Töö nähtavus

Leht **Töö nähtavus** annab reaalajas vaba kaubavaru päringu tulemused, põhinedes mitmete dimensioonide kombinatsioonidele. Kui funktsioon *OnHandReservation* on sisse lülitatud, saate sisestada reserveerimistaotlusi ka lehelt **Töö nähtavus**.

### <a name="on-hand-query"></a>Vaba kaubavaru päring

Vahekaardil **Vaba kaubavaru päring** kuvatakse reaalajas vaba kaubavaru päringu tulemused.

Kui valite vahekaardi **Vaba kaubavaru päring**, küsib süsteem teie mandaate, nii et see saaks juurdepääsuloa, mis on Varude nähtavuse teenuse päringuteks nõutav. Võite juurdepääsuloa lihtsalt väljale **Juurdepääsuluba** kleepida ja dialoogiboksi sulgeda. Seejärel saate sisestada vaba kaubavaru päringu taotluse.

Kui juurdepääsuluba ei kehti või kui see on aegunud, peate kleepima väljale **Juurdepääsuluba** uue loa. Sisestage õiged **Kliendi ID**, **Rentniku ID**, **Kliendi saladuse** väärtused ja valige **Värskenda**. Süsteem saab automaatselt uue kehtiva juurdepääsuloa.

Vaba kaubavaru päringu sisestamiseks sisestage päring päringu sisusse. Kasutage mustrit, mida on kirjeldatud jaotises [Päring sisestusmeetodi abil](inventory-visibility-api.md#query-with-post-method).

![Vaba kaubavaru päringu seaded](media/inventory-visibility-query-settings.png "Vaba kaubavaru päringu seaded")

### <a name="reservation-posting"></a>Reserveeringu sisestamine

Kasutage vahekaarti **Reserveeringu sisestamine** reserveerimistaotluse sisestamiseks. Enne kui saate reserveerimistaotluse sisestada, peate lülitama sisse funktsiooni *OnHandReservation*. Selle funktsiooni kohta lisateabe saamiseks vt jaotist [Varude nähtavuse reserveeringuid](inventory-visibility-reservations.md).

Reserveerimistaotluse sisestamiseks peate väärtuse taotluse sisusse. Kasutage mustrit, mida kirjeldatakse jaotises [Ühe reserveerimissündmuse loomine](inventory-visibility-api.md#create-one-reservation-event). Seejärel valige **Sisesta**. Taotluse vastuse üksikasjade vaatamiseks valige suvand **Kuva üksikasjad**. Samuti saate `reservationId` väärtuse vastuse üksikasjadest.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Varude kokkuvõte

Varude **kokkuvõtte leht** annab koos kõigi dimensioonidega toodete lao kokkuvõtte. See on kohandatud vaade varude vaba *summa üksuse* jaoks. Lao koondandmed sünkroonitakse perioodiliselt laovarude nähtavuse väljalt.

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>Lubage varude kokkuvõte ja määrake sünkroonimise sagedus.

Varude kokkuvõtte lehe **lubamiseks ja** sünkroonimise sageduse miseks järgige neid samme.

1. Avage lehekülg **Konfiguratsioon**.
1. Avage vahekaart **Funktsioonihaldus >** Sätted.
1. Seadke funktsiooni **OnHandMostSpecificBackgroundService tumblerlüliti** väärtusele *Jah*.
1. Kui see funktsioon on lubatud, **·** **muutub teenuse konfigureerimise jaotis kättesaadavaks ja sisaldab rida OnHandMostSpecificBackgroundService’i** funktsiooni konfigureerimiseks. See säte võimaldab teil valida sageduse, millega lao koondandmed sünkroonitakse. Kasutage veeru **Väärtus** nuppu **üles** ja **alla,** et muuta sünkroonimiste vahelist aega (mis võib olla kuni 5 minutit alla). Seejärel valige nupp **Salvesta**.
1. Valige **kõigi muudatuste** salvestamiseks suvand Värskenda konfiguratsiooni.

![OnHandMostSpecificBackgroundService’i säte](media/inventory-visibility-ohms-freq.PNG "OnHandMostSpecificBackgroundService’i säte")

> [!NOTE]
> Funktsioon *OnHandMostSpecificBackgroundService* jälgib ainult toote vaba kaubavaru muudatusi, mis ilmnesid pärast funktsiooni sisse lülitamist. Nende toodete andmeid, mis pole muutunud, kuna te funktsiooni sisse lülitasite, ei sünkroonita laoteenuse vahemälust keskkonda Dataverse. Kui teie **varude** kokkuvõtte leht ei näita kogu eeldatavat vaba laoseisu teavet, **minge varude haldusse > Perioodilised ülesanded >** Varude nähtavuse integreerimine, keelake pakett-töö ja lubage see uuesti. See käivitab algse tõuke ja kõik andmed sünkroonitakse *üksusega Laovaru Vaba summa järgmise* 15 minuti pärast. Kui soovite seda funktsiooni kasutada, **on soovitatav see enne vaba kaubavaru muudatuste tegemist sisse lülitada ja lubada varude nähtavuse integreerimise pakett-töö**.

### <a name="work-with-the-inventory-summary"></a>Tööta lao kokkuvõttega

Kasutades **Täpsemat filtrit**, mida Dataverse pakub, saate luua isikliku vaate, mis näitab teie jaoks olulisi ridu. Täpsema filtri võimalused lasevad teile luua mitmesuguseid vaateid, lihtsatest keerulisteni. Samuti võimaldavad nad filtritele lisada grupeeritud ja pesastatud tingimusi. Lisateabe saamiseks **Täpsema filtri** kohta, vt jaotist [Isiklike vaadete redigeerimine või loomine täpsemate ruudustiku filtrite abil](/powerapps/user/grid-filters-advanced).

Kohandatud vaate ülaosas on kolm välja: **Vaikedimensioon**, **Kohandatud dimensioon** ja **Mõõde**. Nende väljade abil saate määrata, millised veerud on nähtavad.

Saate valida veeru päise, et praeguseid tulemusi filtreerida või sortida.

Kohandatud vaate allosas kuvatakse selline teave nagu "50 kirjet (29 valitud)" või "50 kirjet". See teave viitab praegu laaditud kirjetele **Täpsema filtri** tulemusest. Tekst "29 valitud" viitab kirjete arvule, mis on laaditud kirjete veeru päise filtri abil valitud.

Vaate allosas on nupp **Laadi veel**, mille abil saate laadida rohkem Dataverse'i kirjeid. Vaikimisi on laaditud kirjete arv 50. Kui valite **Laadi rohkem**, laaditakse vaatesse järgmised 1000 saadaolevat kirjet. Number nupul **Laadi veel** näitab praegu laaditud kirjeid ja **Täpsema filtri** tulemuste kõigi kirjete arvu.

![Varude kokkuvõte](media/inventory-visibility-onhand-list.png "Varude kokkuvõte")
