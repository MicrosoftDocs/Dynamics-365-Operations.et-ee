---
title: Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil
description: See protseduur selgitab kaupade registreerimist, kasutades kauba saabumise töölehte täpsemate laohaldusprotsesside kasutamisel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea8b5e03282aa21aa9dfa486b1deaced6af4601c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426406"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil

[!include [banner](../../includes/banner.md)]

See protseduur selgitab kaupade registreerimist, kasutades kauba saabumise töölehte täpsemate laohaldusprotsesside kasutamisel. Seda teeb üldjuhul vastuvõtuametnik. 

Saate seda protseduuri käitada demoettevõtte USMF andmetega või oma andmetega. Enne selle juhendi käivitamist peate olema kinnitanud avatud ostutellimuse reaga ostutellimuse. Rea kaup peab olema ladustatav ja see ei tohi kasutada tootevariante ja sellel ei tohi olla jälgimisdimensioone. Samuti peavad kaubad olema seostatud laoala dimensioonigrupiga, mille puhul on laohaldusprotsessid lubatud. Kasutatav ladu peab olema laohaldusprotsesside jaoks lubatud ja vastuvõtmiseks kasutatav asukoht peab olema litsentsiplaadiga juhitav. USMF-i kasutamisel saate ostutellimuse loomisel kasutada ettevõtte kontot 1001, ladu 51 ja kaupa M9200. 

Märkige üles loodava ostutellimuse number ning ostutellimuse rea jaoks kasutatav kaubakood ja tegevuskoht.


## <a name="create-an-item-arrival-journal-header"></a>Kauba saabumise töölehe päise loomine
1. Minge jaotisse Kauba saabumine.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
    * Kui kasutate USMF-i, saate sisestada WHS-i. Kui kasutate muid andmeid, peavad töölehel, mille nime valite, olema järgmised atribuudid: Kontrolli komplekteerimiskohta peab olema seatud valikule Ei ja Vahelao haldus peab olema seatud valikule Ei.  
4. Sisestage väärtus väljale Arv.
5. Sisestage väärtus väljale Koht.
    * Valige tegevuskoht, mida kasutasite oma ostutellimuse rea puhul. See toimib vaikeväärtusena kõigile töölehe ridadele. Kui kasutasite USMF-is ladu 51, valige tegevuskoht 5.  
6. Sisestage väärtus väljale Ladu.
    * Valige valitud tegevuskoha jaoks kehtiv ladu. See toimib vaikeväärtusena kõigile töölehe ridadele. Kui kasutate USMF-i näidisväärtusi, valige 51.  
7. Tippige väärtus väljale Asukoht.
    * Valige valitud lao jaoks kehtiv asukoht. Asukoht peab olema seotud litsentsiplaadiga juhitava asukohaprofiiliga. See toimib vaikeväärtusena kõigile töölehe ridadele. Kui kasutate USMF-i näidisväärtusi, valige Bulk-008.  
8. Paremklõpsake rippnoolt väljal Llitsentsiplaat ja valige suvand Kuva üksikasjad.
9. Klõpsake valikut Uus.
10. Sisestage väärtus väljale Litsentsiplaat.
    * Märkige väärtus üles.  
11. Klõpsake nuppu Salvesta.
12. Sulgege leht.
13. Sisestage väärtus väljale Litsentsiplaat.
    * Sisestage vastloodud litsentsiplaadi väärtus. See toimib vaikeväärtusena kõigile töölehe ridadele.  
14. Klõpsake nuppu OK.

## <a name="add-a-line"></a>Rea lisamine
1. Klõpsake käsku Lisa rida.
2. Sisestage väärtus väljale Kaubakood.
    * Sisestage ostutellimuse real kasutatav kaubakood.  
3. Sisestage arv väljale Kogus.
    * Sisestage kogus, mille soovite registreerida.  
    * Väli Kuupäev määratleb kuupäeva, millal selle kauba vaba kaubavaru kogus laos registreeritakse.  
    * Partii ID sisestab süsteem, kui esitatud teabe põhjal on võimalik see üheselt tuvastada. Vastasel juhul peate selle lisama käsitsi. See on kohustuslik väli, mis seob registreeringu kindla lähtedokumendi reaga.  

## <a name="complete-the-registration"></a>Registreerimise lõpule viimine
1. Klõpsake suvandit Kinnita.
    * See kontrollib, kas tööleht on sisestamiseks valmis. Kui kontrollimine nurjub, peate tõrked enne töölehe sisestamist kõrvaldama.  
2. Klõpsake nuppu OK.
    * Klõpsake OK ja kontrollige teadet. Kuvatama peaks teade, et tööleht on korras.  
3. Klõpsake valikut Sisesta.
4. Klõpsake nuppu OK.
    * Pärast OK klõpsamist kontrollige teateriba. Kuvatama peaks teade, et toiming on lõpule viidud.  
5. Sulgege leht.

