---
title: Lao partii tõrkeotsing ja seeria reserveerimise hierarhiad
description: Selles teemas kirjeldatakse, kuidas lahendada reserveerimise hierarhiatega töötamisel tekkivaid probleeme, mis kasutavad partii või seeria dimensioone.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022542"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Lao partii tõrkeotsing ja seeria reserveerimise hierarhiad

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada reserveerimise hierarhiatega töötamisel tekkivaid probleeme, mis kasutavad partii või seeria dimensioone.

Lisateavet vt [Paindlik dimensiooni broneerimise poliitika laotasemel](flexible-warehouse-level-dimension-reservation.md).

Kauba broneerimishierarhia dikteerib nõuded salvestusmõõtmetele, mis peavad olema täidetud nõudetellimuse asukoha määramiseks. Neid dimensioone saab kirjeldada kui *asukohast ülalpool dimensioone* kõikide dimensioonide puhul, mis peavad olema täidetud enne asukoha määramist, ja *dimensioonid allpool asukohta* dimensioonide puhul, mida saab eraldada pärast asukoha määramist nõudlustellimusele. Neid reserveerimishierarhiaid nimetatakse ka *partii-ülevaks* ja *partii-aluseks* reserveerimishierarhiaks või reserveerimishierarhiate *ülaseeriaks* ja *alaseeriaks*.

Laovarusid saab edukalt eraldada ainult juhul, kui asukohaülestes dimensioonides ei ole erinevusi. Näiteks reserveerimishierarhias *partiiülese* puhul saab eeldada, et nõudetellimusel tuleb määrata **piirkonna**, **lao** ja **partiinumbri** dimensioonid. Kui mõni neist dimensioonidest puudub, siis eraldusprotsess nurjub. Vastandina võib *partiialuses* või *seeriaaluses* reserveerimishierarhias määrata nõudlustellimusel partii- või seerianumbri, kuid eraldamisprotsess seda ei nõua.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Kuvatakse järgmine tõrketeade: "Kui soovite määrata voo, peavad koorma read määrama dimensioonid asukoha kohal. Nende dimensioonide määramiseks broneerige ja looge uuesti koorma rida."

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kasutate kaupa, millel on *partii eespool* broneerimise hierarhia, ei tööta lehekülje **Koormuse planeerimise töökoht** käsk **Väljasta laole**, kui üritada väljastada koormat osalise kogusega. Te saate selle tõrketeate ja ükski töö ei ole loodud osalise koguse jaoks.

Kui aga kasutate kaupa, millel on *partii allpool* broneerimise hierarhia, saate väljastada osalise kogusega koormat lehelt **Koormuse planeerimise töökoht**.

### <a name="issue-cause"></a>Väljastamise põhjus

Kui broneerimise hierarhias on dimensioon **Asukoha** dimensioonist ettepool, peab see olema määratud enne lattu väljastamist. Osalisi koguseid ei saa väljastada, kui ühe või mitme dimensiooni **Asukoht** on määramata.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Partii numbri automaatse broneerimise viip käivitatakse, isegi kui inventar on saadaval.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kasutate kaupa, mille reserveerimishierarhia on laos *partiiülene*, kus pole lubatud laoprotsessid ja automaatne reserveerimine on lubatud, kuvatakse partiinumbri automaatse reserveerimise viip isegi siis, kui komplekteerimiseks on saadaval ainult üks partii.

Kuid kui kasutate sama kaupa laos, kus laoprotsessid on lubatud, ei kuvata automaatse reserveerimise viipa.

### <a name="issue-cause"></a>Väljastamise põhjus

Kui reserveerimishierarhia on määratletud *partiiülese* või *seeriaülesena*, peab viidatud dimensioon (**partiinumber** või **seerianumber**) alati olema määratud nõudlustellimustel. Laoprotsessid võivad teabe lõpule viia, kui saadaval on üks partii- või seerianumber. Kuna ladu ei ole laoprotsesside jaoks lubatud, peab kasutaja alati määrama kõik **asukohast** ülalnimetatud dimensioonid.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Pesade mallid, mille puhul on kriteerium Arvesta vaba pesa, ei arvesta partiiga lubatud kaupade praegust vaba kaubavaru.

Lisateavet vt teemast [Laoruumi leidmine](warehouse-slotting.md).

### <a name="issue-description"></a>Probleemi kirjeldus

Pesade mallid, mille puhul on kriteerium *Arvesta vaba* pesa, ei arvesta *partiiüleste* kaupade praegust vaba kaubavaru. Nad arvestavad seda ainult juhul, kui partiinumber on müügitellimuse real määratud.

Kui kasutate aga *partiialuseid* kaupu, loetakse praegune vaba kaubavaru nii nagu on.

### <a name="issue-cause"></a>Väljastamise põhjus

Pesastatud malli päise saab määrata nõudetrateegiatele *Tellitud*, *Reserveeritud* või *Välja antud*. *Tellitud* nõudlusstrateegia puhul kehtivad samad reserveerimishierarhia nõuded, mis rakenduvad reserveeringutele või laoprotsesside väljaandmisele. Seetõttu peab *partiialuse* või *seeriaaluste* kaupade puhul, mille reserveerimise hierarhiad on partii- või seerianumbrid määratud nõudlustellimusel (müük või ülekanne). Teise võimalusena saab nõudlusstrateegiat *Reserveeritud* kasutada partii või seerianumbri valimiseks enne lao täitmisnõudluse loomist.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
