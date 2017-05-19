---
title: "Laotöö juhtimine töömallide ja asukohadirektiividega"
description: "Selles artiklis kirjeldatakse, kuidas kasutada töömalle ja asukoha korraldust määramaks, kuidas ja kus laos tööd tehakse."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e90741b9151f19c70923685fdf1edb2552296a08
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Laotöö juhtimine töömallide ja asukohadirektiividega

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse, kuidas kasutada töömalle ja asukoha korraldust määramaks, kuidas ja kus laos tööd tehakse.

Juhised, mille laotöötajad mobiilsesse seadmesse saavad, määravad töömallid, mille seadistate teenuses Microsoft Dynamics 365 for Operations, et määratleda erinevaid laoprotsesse ja ülesandeid. Töömallid määravad, kuidas igas laoprotsessis tööd tehakse. Linkides töömallidega asukohakorralduse, saate tagada, et töö toimub ladude kindlatel füüsilistel aladel.

## <a name="work-templates"></a>Töömallid
Leht **Töömallid** võimaldab teil määratleda tööüksuse toimingud, mida tuleb laos teha. Tavaliselt koosnevad lao tööüksuse toimingud paarist tegevusest: laotöötaja komplekteerib ühes kohas vaba kaubavaru ja viib komplekteeritud kaubavarud teise kohta. 

Töömallid koosnevad päisest ja seostatud ridadest. Iga töömall on kindlale *töö tellimuse tüübile*. Paljud töötellimuse tüübid on seotud lähtedokumentidega, nagu ostu- või müügitellimused. Kuid muud töötellimuse tüübid esindavad eraldiseisvaid laoprotsesse, nagu tsükliline inventuur. *Töökausta ID *võimaldab tööd gruppidesse korraldada. 

Töö päise määratluses olevaid sätteid saab kasutada selleks, et määrata, millal tuleb luua uus tööüksus. Näiteks saate määrata komplekteerimisridade maksimaalse arvu ja maksimaalse eeldatava komplekteerimisaja. Kui müügitellimuse komplekteerimisprotsessi töö ületab kummgi nendest väärtustest, jaotatakse see töö kaheks tööüksuseks. 

Tööread näitavad füüsilisi ülesandeid, mis on töö jätkamiseks nõutavad. Näiteks väljamineva laoprotsessi jaoks võib olla töörida kaupade komplekteerimise kohta laos ja teine rida nende kaupade panemise kohta koondusalale. Seal võib olla täiendav rida kaupade komplekteerimise kohta koondusalalt ja teine rida kaupade laadimisest autosse osana laadimisprotsessist. Saate määrata töömallide ridadele *korralduse koodi *. Korralduse kood lingitakse asukohakorraldusega ja see aitab seega tagada, et laotööd töödeldakse laos õiges kohas. 

Saate seadistada päringu, et juhtida, millal konkreetset töömalli kasutatakse. Näiteks saate määrata piirangu, nii et kindlat malli saab kasutada ainult kindlas laos töötamisel. Teise võimalusena võib teil olla mitu malli, mida kasutatakse töö loomiseks väljamineva müügitellimuse töötlemisel olenevalt müügi allikast. Süsteem kasutab välja **Seerianumber** saadaolevate töömallide hindamise järjekorra määramiseks. Seega kui teil on väga konkreetne päring kindla töömalli kohta, andke sellele väike järjekorranumber. Seda päringut hinnatakse siis muudest, üldisematest päringutest enne. 

Tööprotsessi lõpetamiseks või peatamiseks saate kasutada töörea sätet **Peata töö**. Sellisel juhul ei pea tööd tegev töötaja läbima järgmist töörea etappi. Järgmise etapi juurde liikumiseks peab see või mõni teine töötaja uuesti töö valima. Samuti saate erldada ülesanded tööüksuses, kasutades töömalliridadel erinevat *tööklassi ID-d*.

## <a name="location-directives"></a>Asukoha korraldus
Asukoha korraldused on reeglid, mis aitavad tuvastada komplekteerimise ja mahapanemise asukohti varude liigutamisel. Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kuhu komplekteeritud kaubad maha pannakse. Asukoha korraldus koosneb päisest ja seotud ridadest ning loote need lehel **Asukoha korraldus**. 

Päises peab iga asukoha korraldus olema seotud *töö tellimuse tüübiga*, mis määrab laokande tüübi, mille jaoks korraldust kasutatakse, nt müügitellimused, täiendamine või toormaterjalide komplekteerimine. *Töö tüüp *määrab, kas asukoha korraldust kasutatakse töö komplekteerimiseks või mahapanekuks või mõneks muuks laoprotsessiks, nagu inventuur või varude oleku muutmine. Peate määrama ka *koha *ja *lao*. Päises määratavat *korralduse koodi *saab kasutada asukoha korralduse linkimiseks ühe või mitme töömalliga. 

Töömallide puhul saate seadistada päringu, et määrata, millal kindlat asukoha korraldust kasutatakse. Näiteks saate määrata, et kui e-kaubandus on müügitellimuse allikas, tuleb varud komplekteerida lao spetsiaalsel alal. Süsteem kasutab välja **Seerianumber** saadaolevate asukohakorralduste hindamise järjekorra määramiseks. 

Asukohakorralduse read seavad asukoha leidmise reeglite rakendusele lisapiiranguid. Saate määrata minimaalse ja maksimaalse koguse, millele korraldus vastama peab, ja saate määrata, et korraldus on kindlale laoühikule. Näiteks kui mõõtühikuks on kaubaalused, saab määratud asukohta maha panna ainult kaubaalustel kaupu. Samuti saate määrata, kas kogust saab mitme asukoha vahel jagada. Nagu asukohakorralduse päisel, on ka asukohakorralduse real seerianumber, mis määrab ridade hindamise järjekorra. 

Asukohakorraldustel on veel üks üksikasjade tase: *asukohakorralduse toimingud*. Saate määratleda igale reale mitu asukoha korralduse tegevust. Järjekorranumbrit kasutatakse selleks, et määrata tegevuste järjekord. Sellel tasemel saate seadistada päringu määratlemaks, kuidas leida laos parim asukoht. Saate kasutada ka eelmääratletud sätteid **Strateegia**, et leida optimaalne asukoht.

### <a name="example-of-the-use-of-location-directives"></a>Asukoha korralduste kasutamise näide

Selle näite puhul kaalume ostutellimuse protsessi, kus asukoha korraldus peab leidma laos äsja vastuvõtudokis ragistreeritud laokaupade jaoks vaba ruumi. Esiteks püüame leida vaba ruumi laos, konsolideerides olemasoleva vaba kaubavaruga. Kui konsolideerimine ei ole võimalik, soovime leida tühja asukoha. 

Selle stsenaariumi jaoks peame määratlema kaks asukoha korralduse tegevust. Esimene tegevus järjekorras peab kasutama strateegiat **Konsolideeri** ja teine strateegiat **Tühi asukoht sissetuleva tööta**. Kui me ei määratle kolmandat tegevust ületäitmise stsenaariumi käsitlemiseks, on võimalikud kaks tulemust, kui laos ei ole enam ruumi: töö saab luua isegi kui asukohti ei määratleta või töö loomise protsess võib nurjuda. Tulemuse määrab lehe **Asukoha korralduse tõrked** seadistus, kus saate otsustada, kas valida suvand **Peata töö asukoha korralduse tõrke korral** igale töö tellimuse tüübile.




