---
title: Väljalaadimiskulu aruanded
description: See teema selgitab, kuidas leida ja kasutada erinevat tüüpi aruandeid, mis on saadaval moodulis Väljalaadimiskulu.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: cb0ea44c0924fc5d2c295a9285701d1f678c3473
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571733"
---
# <a name="landed-cost-reports"></a>Väljalaadimiskulu aruanded

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Laekumata arved

Laekumata arvete aruanne sisaldab kõigi erinevate reisiga seotud kulutasemete tasumata arvete loendit. Seda kasutatakse reisi ja reisikulude regulaarseks vastavusseviimiseks koos pearaamatu kannete loendiga. Pärast üldkulu arveldamist eemaldatakse see aruandest.

Laekumata arvete aruande loomiseks toimige järgmiselt.

1. Avage **Väljalaadimiskulu \> Aruanded \> Jälgimine \> Laekumata arved**.
1. Määrake kuupäev dialoogiboksi **Laekumata arved** väljal **Seisuga**. Väljundisse kaasatakse kõik sel kuupäeval või enne seda laekumata arved.
1. Valige suvandi **Kuva** alt üks järgmistest suvanditest.

    - **Arveldamata kulu** – kaasake arveldatud saadetiste kulud, millel on eeldatava omahinna väärtus, kuid tegelik kulu puudub.
    - **Arveldamata varud** – kaasake kulud, mis on arveldatud, kuid mille jaoks ostutellimust pole veel vastu võetud.
    - **Kõik arveldamata** – kaasatakse nii suvandi **Arveldamata kulu** kui ka suvandi **Arveldamata varud** tulemid.

1. Seadke suvandi **Kaasa uued kulud** väärtuseks *Jah*, et kaasata kulud, millel ei ole veel tegelikku kulu ja mille jaoks varusid pole vastu võetud. Kui määrate väärtuseks *Ei*, sisaldab aruanne ainult arveldatud kulusid.
1. Lubage jaotises **Vaade** iga üksikasjatüüp, mille soovite aruandesse kaasata.
1. Aruande väljundvormingu valimiseks kasutage kiirkaarti **Sihtkoht**, nagu teete lahenduse Microsoft Dynamics 365 Supply Chain Management muude aruandetüüpide korral.
1. Aruandesse kaasatavate kirjete täpsemaks piiramiseks kasutage kiirkaarti **Kaasatavad kirjed**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruande loomiseks valige **OK**.

## <a name="activityprovider-analysis-reports"></a>Tegevuse/pakkuja analüüsiaruanded

Tegevuse/pakkuja analüüsiaruanded lasevad teil üle vaadata iga pakkuja kohta tehtud ajaprognooside täpsuse.

Tegevuse/pakkuja analüüsiaruande loomiseks toimige järgmiselt.

1. Sõltuvalt sellest, millist tüüpi aruannet soovite luua, tehke üks järgmistest toimingutest.

    - Avage **Väljalaadimiskulu \> Aruanded \> Tegevuse/pakkuja analüüs tegevuse järgi**. Sel juhul grupeeritakse ajaprognoosid tegevuse kaupa.
    - Avage **Väljalaadimiskulu \> Aruanded \> Tegevuse/pakkuja analüüs pakkuja järgi**. Sel juhul grupeeritakse ajaprognoosid pakkuja kaupa.

    Kuvatakse dialoogiboks **Tegevuse/pakkuja analüüs tegevuse järgi** või dialoogiboks **Tegevuse/pakkuja analüüs pakkuja järgi**. Mõlemas dialoogiboksis on samad suvandid.

1. Aruande väljundvormingu valimiseks kasutage kiirkaarti **Sihtkoht**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruandesse kaasatavate kirjete täpsemaks piiramiseks kasutage kiirkaarti **Kaasatavad kirjed**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruande loomiseks valige **OK**.

## <a name="voyage-costing-reports"></a>Reisi kuluarvutuse aruanded

Reisi kuluarvutuse aruanded näitavad kaupade kulu ja impordikulusid foolio, saatmiskonteineri või reisi kohta, sõltuvalt aruande loomisel valitud suvanditest. Iga reisi kuluarvestuse aruanne võimaldab teil vaadata reisi eeldatavat omahinda võrreldes tegeliku kuluga ja seda saab esitada mitme teguri järgi.

Reisi kuluarvutuse aruande loomiseks toimige järgmiselt.

1. Sõltuvalt sellest, millist tüüpi aruannet soovite luua, tehke üks järgmistest toimingutest.

    - Avage **Väljalaadimiskulu \> Aruanded \> Kuluarvutus \> Reisi kuluarvutus üksikkulu järgi**. Sellisel juhul näitab üksikkulu suvand impordikulusid kuluala ja kulutüübi koodi kohta.
    - Avage **Väljalaadimiskulu \> Aruanded \> Kuluarvutus \> Reisi kuluarvutus aruandluskategooria järgi**. Sellisel juhul esitatakse impordikulud mitmesuguste aruandluskategooriate kaupa. Kulutüübid grupeeritakse aruandluskategooriate alusel.

    Kuvatakse dialoogiboks **Reisi kuluarvutus üksikkulu järgi** või dialoogiboks **Reisi kuluarvutus aruandluskategooria järgi**. Need dialoogiboksid on sarnased. Kõik erinevused on ülejäänud protseduuris välja toodud.

1. Kui avasite dialoogiboksi **Reisi kuluarvestus aruandluskategooria järgi**, valige väljal **Kulu** üks järgmistest väärtustest.

    - **Kulu väärtus** – väärtus arvutatakse automaatsete kulude abil või luuakse kulualas käsitsi.
    - **Eeldatav** – pärast kaupade kättesaamist seatakse eeldatav omahind.
    - **Tegelik** – pärast tellimuse arveldamist seatakse tegelikuks kuluks arvel toodud kulu.
    - **Parim** – süsteem kasutab eespool nimetatud kolmest suvandist seda, mis on parasjagu kõige täpsem. (Soovitame teil valida selle suvandi.)

1. Seadke suvandi **Kauba kohta** väärtuseks *Jah*, et näidata iga kauba kulu. Seadke väärtuseks *Ei*, et kuvada kulud reisi kohta.
1. Valige jaotises **Vaade** kategooriad, mille alusel kulusid esitada.
1. Jaotises **Dimensioonid** valige dimensioonid, mida aruandesse kaasata.
1. Aruande väljundvormingu valimiseks kasutage kiirkaarti **Sihtkoht**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruandesse kaasatavate kirjete täpsemaks piiramiseks kasutage kiirkaarti **Kaasatavad kirjed**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruande loomiseks valige **OK**.

## <a name="shipping-container-receipts-list"></a>Saatmiskonteinerite sissetulekute loend

Saatmiskonteinerite sissetulekute loend sisaldab kõiki saabumata koguseid, mis peaksid saabuma eeldatud kuupäeval või enne seda. Laopersonal saab selle aruande abil tuvastada saatmiskonteineris eeldatavasti sisalduvad kaubad. Samuti saab seda kasutada kaupade käsitsi kinnitamiseks vastavalt nende vastuvõtmisele saatmiskonteinerist.

Saatmiskonteinerite sissetulekute loendi loomiseks tehke järgmist.

1. Avage **Väljalaadimiskulu \> Aruanded \> Jälgimine \> Saatmiskonteinerite sissetulekute loend**.
1. Määrake kuupäev dialoogiboksi **Saatmiskonteinerite sissetulekute loend** väljal **Eeldatav kuupäev**. Väljundisse kaasatakse kõik sel kuupäeval või enne seda saabumata kogused.
1. Jaotises **Dimensioonid** valige dimensioonid, mida aruandesse kaasata.
1. Aruande väljundvormingu valimiseks kasutage kiirkaarti **Sihtkoht**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruandesse kaasatavate kirjete täpsemaks piiramiseks kasutage kiirkaarti **Kaasatavad kirjed**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruande loomiseks valige **OK**.

## <a name="expected-delivery-report"></a>Eeldatava tarne aruanne

Eeldatava tarne aruanne sisaldab põhiteavet reisi, saatmiskonteineri, foolio, kaupade ja eeldatava tarnekuupäeva kohta.

Eeldatava tarne aruande loomiseks toimige järgmiselt.

1. Avage **Väljalaadimiskulu \> Aruanded \> Jälgimine \> Eeldatav tarne**.
1. Valige dialoogiboksi **Eeldatav tarne** väljal **Eeldatav kuupäev** see kuupäev, millal eeldatakse kaupade tarnimist lõplikku sihtlattu. Väljundisse kaasatakse kõik reisiread, millel on eeldatav kuupäev või mis on enne seda kuupäeva ja mida pole veel vastu võetud.
1. Valikuline: ainult kindla hankija tarnete kaasamiseks valige soovitud hankija konto väljal **Hankija konto**.
1. Jaotises **Dimensioonid** valige dimensioonid, mida aruandesse kaasata.
1. Aruande väljundvormingu valimiseks kasutage kiirkaarti **Sihtkoht**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruandesse kaasatavate kirjete täpsemaks piiramiseks kasutage kiirkaarti **Kaasatavad kirjed**, nagu teete lahenduse Supply Chain Management muude aruandetüüpide korral.
1. Aruande loomiseks valige **OK**.
