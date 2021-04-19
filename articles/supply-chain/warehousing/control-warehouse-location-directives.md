---
title: Laotöö juhtimine töömallide ja asukohadirektiividega
description: Selles teemas kirjeldatakse, kuidas kasutada töömalle ja asukohakorraldust määramaks, kuidas ja kus laos tööd tehakse.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91c8df8a111132d75ec02b79912c66e02aef4ea6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831310"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Laotöö juhtimine töömallide ja asukohadirektiividega

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada töömalle ja asukohakorraldust määramaks, kuidas ja kus laos tööd tehakse.

Juhised, mille laotöötajad mobiilsesse seadmesse saavad, määravad töömallid, mille seadistate Dynamics 365 Supply Chain Managementis, et määratleda erinevad laoprotsessid ja ülesanded. Töömallid määravad, kuidas igas laoprotsessis tööd tehakse. Linkides töömallidega asukohakorralduse, saate tagada, et töö toimub ladude kindlatel füüsilistel aladel.

## <a name="work-templates"></a>Töömallid

Leht **Töömallid** võimaldab teil määratleda tööüksuse toimingud, mida tuleb laos teha. Tavaliselt koosnevad lao tööüksuse toimingud paarist tegevusest: laotöötaja komplekteerib ühes kohas vaba kaubavaru ja viib komplekteeritud kaubavarud teise kohta. 

Töömallid koosnevad päisest ja seostatud ridadest. Iga töömall on kindlale *töö tellimuse tüübile*. Paljud töötellimuse tüübid on seotud lähtedokumentidega, nagu ostu- või müügitellimused. Kuid muud töötellimuse tüübid esindavad eraldiseisvaid laoprotsesse, nagu tsükliline inventuur. *Töökausta ID* võimaldab tööd gruppidesse korraldada. 

Kasutage tööpäise määratluses olevaid sätteid, et määrata, millal tuleb luua uus tööüksus. Näiteks saate määrata komplekteerimisridade maksimaalse arvu ja maksimaalse eeldatava komplekteerimisaja. Kui müügitellimuse komplekteerimisprotsessi töö ületab kummgi nendest väärtustest, jaotatakse see töö kaheks tööüksuseks.

Kasutage nuppu **Tööpäise piirid**, et määrata, millal süsteem peaks looma uusi tööpäiseid. Näiteks, et luua tööpäis igale _tellimuse numbrile_, valige toimingupaanil **Redigeeri päringut** ja siis lisage väli **Tellimuse number** päringuredaktoris vahekaardile **Sortimine**. Välju, mis on lisatud **Sortimise** vahekaardile, saab valida *grupeerimisväljadena*. Grupeerimisväljade määramiseks valige toimingupaanil **Tööpäise piirid** ja seejärel valige märkige iga välja puhul, mida soovite kasutada grupeerimisväljana, märkeruut veerus **Grupeeri selle välja järgi**.

Tööread näitavad füüsilisi ülesandeid, mis on töö jätkamiseks nõutavad. Näiteks väljamineva laoprotsessi jaoks võib olla üks rida kaupade komplekteerimise kohta laos ja teine rida nende kaupade ladustamise kohta vaheasukohas. Siis võib olla täiendav rida kaupade komplekteerimise kohta vaheasukohas ja teine rida kaupade ladustamiseks veoautosse osana laadimisprotsessist. Saate määrata töömallide ridadele *korralduse koodi*. Korralduse kood lingitakse asukohakorraldusega ja see aitab seega tagada, et laotööd töödeldakse laos õiges kohas.

Saate seadistada päringu, et juhtida, millal konkreetset töömalli kasutatakse. Näiteks saate määrata piirangu, nii et kindlat malli saab kasutada ainult kindlas laos töötamisel. Teise võimalusena võib teil olla mitu malli, mida kasutatakse töö loomiseks väljamineva müügitellimuse töötlemisel olenevalt müügi allikast. Süsteem kasutab välja **Seerianumber** saadaolevate töömallide hindamise järjekorra määramiseks. Seega kui teil on väga konkreetne päring kindla töömalli kohta, andke sellele väike järjekorranumber. Seda päringut hinnatakse siis enne teisi, üldisemaid päringuid.

> [!NOTE]
> Et takistada süsteemil automaatselt töömalli *järjekorranumbrite* ülekirjutamist, lülitage pärast malli kustutamist sisse funktsioon *Säilita kustutamisel töömalli järjekorranumbrid* [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tööprotsessi lõpetamiseks või peatamiseks saate kasutada töörea sätet **Peata töö**. Sellisel juhul ei pea tööd tegev töötaja läbima järgmist töörea etappi. Järgmise etapi juurde liikumiseks peab see või mõni teine töötaja uuesti töö valima. Samuti saate erldada ülesanded tööüksuses, kasutades töömalliridadel erinevat *tööklassi ID-d*.

## <a name="location-directives"></a>Asukoha korraldus

Asukoha korraldused on reeglid, mis aitavad tuvastada komplekteerimise ja mahapanemise asukohti varude liigutamisel. Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kuhu komplekteeritud kaubad maha pannakse. Asukoha korraldus koosneb päisest ja seotud ridadest ning loote need lehel **Asukoha korraldus**.

Päises peab iga asukoha korraldus olema seotud *töö tellimuse tüübiga*, mis määrab laokande tüübi, mille jaoks korraldust kasutatakse, nt müügitellimused, täiendamine või toormaterjalide komplekteerimine. *Töö tüüp* määrab, kas asukoha korraldust kasutatakse töö komplekteerimiseks või mahapanekuks või mõneks muuks laoprotsessiks, nagu inventuur või varude oleku muutmine. Peate määrama ka *koha* ja *lao*. Päises määratavat *korralduse koodi* saab kasutada asukoha korralduse linkimiseks ühe või mitme töömalliga. 

Töömallide puhul saate seadistada päringu, et määrata, millal kindlat asukoha korraldust kasutatakse. Näiteks saate määrata, et kui e-kaubandus on müügitellimuse allikas, tuleb varud komplekteerida lao spetsiaalsel alal. Süsteem kasutab välja **Seerianumber** saadaolevate asukohakorralduste hindamise järjekorra määramiseks.

Asukohakorralduse read seavad asukoha leidmise reeglite rakendusele lisapiiranguid. Saate määrata minimaalse ja maksimaalse koguse, millele korraldus vastama peab, ja saate määrata, et korraldus on kindlale laoühikule. Näiteks kui mõõtühikuks on kaubaalused, saab määratud asukohta maha panna ainult kaubaalustel kaupu. Samuti saate määrata, kas kogust saab mitme asukoha vahel jagada. Nagu asukohakorralduse päisel, on ka asukohakorralduse real seerianumber, mis määrab ridade hindamise järjekorra.

Asukohakorraldustel on veel üks üksikasjade tase: *asukohakorralduse toimingud*. Saate määratleda igale reale mitu asukoha korralduse tegevust. Järjekorranumbrit kasutatakse selleks, et määrata tegevuste järjekord. Sellel tasemel saate seadistada päringu määratlemaks, kuidas leida laos parim asukoht. Saate kasutada ka eelmääratletud sätteid **Strateegia**, et leida optimaalne asukoht.

Lisateavet asukohakorralduste loomise ja konfigureerimise kohta leiate jaotisest [Asukohakorralduse loomine](create-location-directive.md).

### <a name="how-location-directives-work"></a>Kuidas asukohakorraldused töötavad?

Asukohakorraldused määravad, *kus* tuleb kaubad komplekteerida ja *kuhu* need tuleb ladustada. Süsteem hindab asukohakorraldust iga töörea korral ja seejärel valib asukoha, võttes aluseks töörea üksikasjad. Süsteem leiab kõigepealt kõik asukohakorraldused, mis vastavad kindlale tööreale (nt need on õige lao jaoks ja vastavad päringule). Seejärel hindab see leitud korraldusi järjekorras.

> [!NOTE]
> On erijuhtumeid, kus komplekteerimise või ladustamise asukoht on eelnevalt valitud. Näiteks _ostu registreerimisel_ toimub esimene komplekteerimine alati asukohas, kus registreerimine toimub. Teine näide on *varude liigutamine malli alusel*, kus laotöötaja valib komplekteerimise asukoha ning asukohakorralduste kaudu leitakse ainult ladustamiskohad.

## <a name="additional-resources"></a>Lisaressursid

- Video: [laohalduse konfiguratsiooni üksikasjalik juhis](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Spikriteema: [asukohakorralduste loomine](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]