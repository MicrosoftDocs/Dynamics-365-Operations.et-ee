---
title: "Koostööd Hankijad hankija portaali abil"
description: "See teema kirjeldab, kuidas ostuagendid saavad kasutada hankija portaali ostutellimuse kinnitamise protsessi käigus väliste hankijatega koostöö tegemiseks. See teave kehtib ainult veebruar 2016 &amp;Dynamics AX mai 2016 versioonid."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: e6c731109dddb7dd47595126c4bf5f1f09425a7d
ms.lasthandoff: 03/31/2017


---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Koostööd Hankijad hankija portaali abil

See teema kirjeldab, kuidas ostuagendid saavad kasutada hankija portaali ostutellimuse kinnitamise protsessi käigus väliste hankijatega koostöö tegemiseks. See teave kehtib ainult veebruar 2016 &amp;Dynamics AX mai 2016 versioonid.

Selles teemas sisalduv teave kehtib ainult Dynamics AX-i 2016. aasta veebruari ja 2016. aasta mai versioonide puhul. Hankija portaali funktsionaalsus on asendatud laiendatud hankija koostööfunktsioonide Dynamics 365 toiminguid versiooni 1611. Uue hankija koostööfunktsioonide kohta lisateabe saamiseks vaadake [kasutades töötada välistarnijate hankija koostöö](vendor-collaboration-work-external-vendors.md).  

Hankija portaal on mõeldud hankijatele, kellel puudub ostutellimuse (PO) teabe vahetamiseks Microsoft Dynamics AX-iga elektrooniliste andmete vahetus (EDI). Portaal võimaldab ostuagentidel saata hankijale ostutellimuse ja saada siis kinnitava või tagasilükkava vastuse otse Dynamics AX-is.  

Protsessi on võimalik konfigureerida nii, et hankija kinnitus kinnitab tellimuse automaatselt. Sellisel juhul on järeltegevust vaja ainult aeg-ajalt, kui tellimus lükatakse tagasi või kui hankija kinnitus on registreeritud vastusena, kuid ostutellimuse olekut ei ole värskendatud väärtusele **Kinnitatud** kinnitusprotsessi probleemi tõttu.

## <a name="po-confirmation-and-rejection"></a>Ostutellimuse kinnitamine ja tagasilükkamine
Ostutellimused koostatakse Dynamics AX-is. Kui teil on ostutellimus olekuga **kinnitatud**, saab saata selle hankijale, luues kinnitustaotluse. Kui soovite juhtida hankija tähelepanu uuele ostutellimusele, võite ostutellimuse saatmiseks meiliga kasutada prindihalduse süsteemi. Ostutellimus ilmub hankija portaali ning sisaldab valikut, mille kaudu hankija saab tellimuse kinnitada või selle tagasi lükata. Hankija saab lisada ka kommentaare teabe (nt ostutellimuse muudatuste) edastamiseks.  

Hankija portaalis saab hankija vaadata tellimuse ridu. Nendel ridadel on teave nagu väline tootekood, dimensioonid, hinnateave, kogus, tarnekuupäev ning tarneaadress. Hankija saab luua aruande, millel on näha ostutellimuse teave ja hind kokku. Hankijat puudutavad tasud kuvatakse, kui hankija klõpsab päises või ridadel nuppu **Tasud**. Hankijad saavad ostutellimuse teabe oma süsteemi importida, kasutades funktsiooni **Excelisse eksportimine**.  

Järgmises tabelis näidatakse tavapärast teabevahetust, mis oleneb sellest, kuidas hankija vastab, kui saadate talle kinnitamiseks ostutellimuse.

| Vastuse tüüp                                                                                                  | Tulemus                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hankija kinnitab tellimuse. Süsteem on konfigureeritud hankija kinnituse korral automaatselt ostutellimusi kinnitama.    | Tellimuse olekuks määratakse **Kinnitatud**. Kui miski takistab tellimuse värskendamist, salvestatakse hankija vastuseks ikkagi **Kinnitatud**, kuid ostutellimuse olekuks jääb **Välisel ülevaatamisel**.                                                                       |
| Hankija kinnitab tellimuse. Süsteem ei ole konfigureeritud hankija kinnituse korral automaatselt ostutellimusi kinnitama. | Hankija vastus salvestatakse kui **Kinnitatud**, kuid ostutellimus jääb olekusse **Välisel ülevaatamisel**.                                                                                                                                                                                      |
| Hankija lükkab tellimuse tagasi.                                                                                     | Hankija vastus salvestatakse kui **Tagasi lükatud** ja ostutellimus jääb olekusse **Välisel ülevaatamisel**. Tagasilükkamine saadakse koos põhjusega ja muutmise ettepanekuga (nt teine tarnekuupäev). Värskendate ostutellimuse ja saadate siis uue versiooni kinnitamiseks. |

## <a name="changes-to-a-po"></a>Muudatused ostutellimuses
Kui peate muutma juba kinnitatud ostutellimust, saate uue ostutellimuse hankijale hankija portaali kaudu. Uuel ostutellimusel on versiooni järelliide, mis näitab, et see on eelnevalt edastatud ostutellimuse muudetud versioon. Hankija portaali abil saavad hankijad iga tellimuse ajalugu jälgida. Ostutellimuse varem kinnitatud versioon jääb uue ostutellimuse kinnitamiseni kinnitatud ostutellimuste nimekirja.  

Ostutellimuse tühistamisel muudetakse olekuks uuesti **Kinnitatud**. Peate ostutellimuse hankija portaali kaudu hankijale tagasi saatma, et hankija saaks tühistamise kinnitada või tagasi lükata. Pärast tühistamise kinnitamist kuvatakse ostutellimus hankija kinnitatud ostutellimuste loendis olekuga **Tühistatud**.

## <a name="versions-status-transitions-and-change-management"></a>Versioonide, oleku üleminekute ja muudatuste haldamine
Kui ostutellimus hankijale saadetakse, registreeritakse see süsteemis ostutellimuse kindla versioonina ja oleku **Kinnitatud** asemel määratakse olekuks **Välisel ülevaatamisel**. Kui ostutellimust hiljem muudetakse, luuakse ostutellimusest uus versioon ja olekuks määratakse uuesti **Kinnitatud** (või **Mustand**, kui muudatuste haldamine on sisse lülitatud).  

Järgmises tabelis on näide oleku ja versiooni muudatuste kohta, mida ostutellimuses teha saab.

| Tegevus                                                   | Olek ja versioon                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Dynamics AX-is luuakse ostutellimuse algne versioon. | Olek on **Kinnitatud**.                                                                           |
| Ostutellimus saadetakse hankija portaali.                     | Versioon registreeritakse hankija portaalis ja olekuks määratakse **Välisel ülevaatamisel**.    |
| Teete mõningaid hankija soovitud muudatusi.  | Olekuks määratakse uuesti **Kinnitatud**.                                                            |
| Saadate ostutellimuse uue versiooni hankija portaali. | Uus versioon registreeritakse hankija portaalis ja olekuks määratakse **Välisel ülevaatamisel**. |
| Hankija kinnitab ostutellimuse uue versiooni.           | Olekuks määratakse **Kinnitatud**.                                                                |

PO versioonides, mis on saadetud hankija ja hankija vastuste vaatamiseks klõpsake **töölehtede**&gt;**kinnitus taotlused** : PO.  

Hankijale vastuse saamiseks saadetud tellimused, mille olek on **Välisel ülevaatamisel**, ilmuvad kas loendis **Ostutellimused on saadetud hankija portaali, oodatakse vastust** või **Ostutellimused on saadetud hankija portaali, vastus nõuab tegevust**. Kui muudate hankijale saadetud tellimust, nii et olekuks määratakse uuesti **Kinnitatud**, ei kuvata tellimust enam nendes loendites. On varem toimunud hankija tellimuse vastuseks vaatamiseks klõpsake **töölehtede**&gt;**taotlused kinnitust**.  

Hankijad ei pea ostutellimust hankija portaalis kinnitama. Nad võivad saata ka meilisõnumi või teatama ostutellimuse vastuvõtmisest muude kanalite kaudu. Seejärel saate tellimuse Dynamics AX-is käsitsi kinnitada. Sellisel juhul saate hoiatuse, et tellimus on kinnitatud, kuigi hankijalt puudub vastus. Seejärel kuvatakse ostutellimus hankija portaali kinnitusajaloos avatud kinnitatud tellimusena, millel puuduvad vastused. Lisaks pole hankijal enam võimalust ostutellimuse kinnitamiseks ega tagasilükkamiseks.  

**Märkus:** Dynamics AX-is teistele protsessidele saadaolev ostutellimuse versioon on alati uusim versioon, isegi kui seda versiooni pole veel registreeritud.

### <a name="change-management"></a>Muudatuste haldamine

Kui olete lülitanud sisse ostutellimuse muudatuste halduse, läbib ostutellimus kinnitamise töövoo, et jõuda olekuni **Kinnitatud**. See protsess ei ole hankijale nähtav.  

Kui muudatuste haldus on ostutellimuse puhul sisse lülitatud, registreeritakse versioon ostutellimuse kinnitamisel, mitte siis, kui ostutellimus on hankijale saadetud või kinnitatud.  

Järgmises tabelis on näide oleku ja versiooni muudatustest, mida ostutellimusse teha võidakse, kui muudatuste haldamine on sisse lülitatud.

| Tegevus                                                                                                        | Olek ja versioon                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dynamics AX-is luuakse ostutellimuse algne versioon.                                                      | Olek on **Mustand**.                                                                                                                                                                                                                                                                                                                                                                    |
| Ostutellimus esitatakse kinnitusprotsessile. (See on sisemine protsess, millesse hankija ei ole kaasatud). | Olek **Mustand** muutub olekuks **Ülevaatamisel** ja siis olekuks **Kinnitamine**, kui ostutellimust kinnitamisprotsessi ajal tagasi ei lükata. Kinnitatud ostutellimus registreeritakse versioonina.                                                                                                                                                                                                                     |
| Ostutellimus saadetakse hankija portaali                                                                           | Versioon registreeritakse hankija portaalis ja olekuks määratakse **Välisel ülevaatamisel**.                                                                                                                                                                                                                                                                                        |
| Teete mõningaid hankija soovitud muudatusi.                                                       | Olekuks määratakse uuesti **Mustand**.                                                                                                                                                                                                                                                                                                                                                    |
| Ostutellimus esitatakse uuesti kinnitusprotsessile.                                                            | Olek **Mustand** muutub olekuks **Ülevaatamisel** ja siis olekuks **Kinnitamine**, kui ostutellimust kinnitamisprotsessi ajal tagasi ei lükata. Teise võimalusena saab süsteemi konfigureerida nii, et konkreetsete välja muudatuste jaoks ei ole vaja uuesti kinnitamist. Sellisel juhul määratakse olekuks kõigepealt **Mustand** ja seejärel automaatselt **Kinnitatud**. Kinnitatud ostutellimus registreeritakse uue versioonina. |
| Saadate ostutellimuse uue versiooni hankija portaali.                                                      | Uus versioon registreeritakse hankija portaalis ja olekuks määratakse **Välisel ülevaatamisel**.                                                                                                                                                                                                                                                                                    |
| Hankija kinnitab ostutellimuse uue versiooni.                                                                | Olekuks määratakse **Kinnitatud**, kas automaatselt või siis, kui saate hankijalt vastuse ja kinnitate siis ostutellimuse.                                                                                                                                                                                                                                                     |
<a name="see-also"></a>Vt ka
--------

[Hankija koostöö kasutajate turbe konfigureerimine](configure-security-vendor-portal-users.md)

[Hankija koostöö arve tööruum](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace)


