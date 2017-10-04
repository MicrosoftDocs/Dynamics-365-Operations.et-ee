---
title: "Krediidi ja võlanõuete seadistamine"
description: "See artikkel selgitab, kuidas sissenõuete funktsiooni seadistada."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1982e495f740d6061b9574aa9f40f38180e8d110
ms.openlocfilehash: 76937aacbc1925603766299168ec2d4090bd161b
ms.contentlocale: et-ee
ms.lasthandoff: 08/03/2017

---

# <a name="set-up-credit-and-collections"></a>Krediidi ja võlanõuete seadistamine

[!include[banner](../includes/banner.md)]


See artikkel selgitab, kuidas sissenõuete funktsiooni seadistada.

<a name="set-up-aging-period-definitions"></a>Aegumisperioodide definitsioonide häälestamine
-------------------------------

Aegumisperioodide definitsiooni seadistamine. Aegumisperioodi definitsioon määratleb veerud, mis kuvatakse loendilehtedel **Aegunud saldod**, **Sissenõuete tegevused** ja **Sissenõuete juhtumid**. Samuti määratleb see perioodid, mis kuvatakse lehel **Sissenõuded**. Kui kliendikaust on seadistatud, kasutatakse kausta aegumisperioodi definitsiooni. Kui kaustu ei ole seadistatud, kasutatakse vaikimisi aegumisperioodi määratlust, mis on määratud lehel **Müügireskontro parameetrid**. Kui ühtegi vaikimisi aegumisperioodi definitsiooni ei ole määratud, kasutatakse esimest aegumisperioodi määratlust lehel **Aegumisperioodi määratlused**.

## <a name="create-an-aging-snapshot"></a>Aegumise hetktõmmise loomine
Looge aegumise hetktõmmise kirjed kõigile klientidele või kliendikausta klientidele. Aegumise hetktõmmise teave kuvatakse loendilehel **Aegunud saldod** ja lehel **Sissenõuded**. Enne kui saate loendilehte kasutada, peate looma aegumise hetktõmmise. Loendilehel kuvatakse teavet vaid püsiklientidele, kelle jaoks on aegumise hetktõmmis loodud.

## <a name="optional-set-up-customer-pools"></a>Valikuline: saate häälestada kliendikaustu
Saate seadistada kliendikaustad kliendigruppide esindamiseks. Saate kasutada kliendikaustu loendilehtedel **Sissenõuded** lehel **Sissenõuded** kuvatava klienditeabe filtritena või aegumise hetktõmmiste loomisel.

## <a name="optional-create-a-collections-team"></a>Valikuline: sissenõuete töörühma loomine
Kui mitu inimest teie organisatsioonis töötab sissenõuetega, saate seadistada sissenõuete töörühma. Saate valida töörühma lehelt **Müügireskontro parameetrid**. Kui te ei loo sissenõuete töörühma, luuakse töörühm automaatselt, kui seadistate inkassaatoreid lehel **Inkassaator**.

## <a name="set-up-a-collections-case-category"></a>Saate seadistada sissenõuete juhtumikategooria
Kui korraldate oma sissenõuete töö juhtumeid kasutades, seadistage juhtumikategooria kategooriatüübiga **Sissenõuded**. Seda seadistust on vaja ainult siis, kui soovite kasutada juhtumi funktsiooni lehel **Sissenõuded**.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Töölehe nimede seadistamine (tasakaalustus, mahakandmine ja NSF)
Saate seadistada töölehenimed, mida kasutatakse kannete töötlemisel lehel **Sissenõuded**. See töötlemine hõlmab kande tasakaalustamist, kande mahakandmist ja ebapiisavate vahenditega (NSF) makse töötlemist.

| Kirjeldus | Töölehe tüüp     |
|-------------|------------------|
| Tasakaalustus  | Kliendi makse |
| Mahakandmine   | Kord päevas            |
| NSF         | Kliendi makse |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Mahakandmiskannete jaoks põhjusekoodi seadistamine
Saate seadistada põhjuse vaikekoodi, mida kasutatakse kannete mahakandmisel lehel **Sissenõuded**. Saate koodi mahakandmise protsessi käigus muuta.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Saate seadistada e-posti manuste kausta ja luua e-kirjade mallid
Kui saadate lehelt **Sissenõuded** meilisõnumeid, millel on Microsoft Exceli manused, saate luua neile sõnumitele soovi korral meilimalle.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Sissenõuete müügireskontro parameetrite seadistamine
Saate seadistada müügireskontro parameetreid, mis kuvatakse vahekaardil **Sissenõuded**.

## <a name="optional-set-up-collections-agents"></a>Valikuline: saate häälestada inkassaatoreid
Kui mitu inimest teie organisatsioonis töötab sissenõuetega, saate seadistada inkassaatorid. Inkassaator on töötaja, kes on seadistatud kasutajana lehel **Kasutaja seosed**. Saate määrata inkassaatoritele kliendikaustu (kliendipäringuid), et aidata inkassaatoritel oma tööd korraldada. Inkassaatorid lisatakse lehel **Müügireskontro parameetrid** valitud töörühma. Kui sellel lehel pole töörühma valitud, luuakse automaatselt uus töörühm nimega **Sissenõuded** ja inkassaatorid lisatakse sellesse töörühma.

## <a name="set-up-a-writeoff-account"></a>Mahakandmise konto seadistamine
Seadistage mahakandmiskonto, mida kasutatakse pearaamatu mahakandmiskandes, kui kanne kantakse maha. See konto salvestatakse kliendi sisestusreeglitesse.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Pangakonto NSF teabe seadistamine
Uuendage pangakontosid nii, et neil on õige tööleht, kui lehel **Sissenõuded** tuvastatakse NSF-maksed. Valige makse tööleht vahekaardil **Valuutahaldus** väljal **NSF-makse tööleht**.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Seadistage Outlooki seaded lehe Sissenõuded kasutajate jaoks
Enne, kui töötajad saavad lehe **Sissenõuded** abil tegevusi luua või meilisõnumeid saata, tuleb veenduda, et on valitud konfiguratsioonivõti **Microsoft Outlooki sünkroonimine** ja et nende töötajate puhul on seadistatud Outlooki sünkroonimine.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Sissenõuete kliendikontaktide e-posti ja aadressi seadete häälestamine
Seadistage kliendikontaktide e-posti aadressid, kui soovite saata meile neile kontaktidele lehelt **Sissenõuded**. Sissenõuete kontakti kasutatakse vaikimisi kontaktina lehel **Sissenõuded**. Saate seadistada kliendi väljavõtte aadressi, kui väljavõtete aadress peab erinema peamisest aadressist. 

Valige kliendi kiirkaardil **Krediit ja sissenõuded** väljal **Sissenõuete kontakt** kliendi organisatsioonis töötav inimene, kes teie inkassaatoriga koostööd teeb. Seda inimest kasutatakse vaikekontaktina lehel **Sissenõuded** ja meilisõnumid saadetakse talle. 

> [!NOTE] 
> Kui sissenõuete kontaktisik pole kliendi puhul määratud, kasutatakse kliendi peamist kontaktisikut. Kui peamist kontaktisikut pole määratud, saadetakse meilisõnumid esimesele lehel **Kontaktid** loetletud aadressile.

## <a name="set-up-email-settings-for-salespeople"></a>Saate seadistada müügitöötajate e-posti seaded
Seadistage müügitöötajate meiliaadressid, kui soovite saata meile müügitöötajatele lehelt **Sissenõuded**. Seadistage iga komisjonimüügi grupi iga müügiesindaja meiliaadress. Müügiesindaja, kelle puhul on ruut **Kontakt** valitud, on vaikimisi müügiesindaja, kellele meile saadetakse. 

Kui müügiesindaja on määramata, kasutatakse kliendi organisatsiooni peamist müügiesindajat. Kui peamist müügiesindajat pole määratud, saadetakse meilisõnumid esimesele lehel nimetatud müügiesindajale.


Lisateavet vt järgmistest teemadest:

 - [Märgukirjaseeria loomine](tasks/create-collection-letter-sequence.md)
 
 - [Märgukirjade töötlemine](tasks/process-collection-letters.md)
 
 - [Sissenõuete teabe ülevaatamine](tasks/review-collections-information.md)

