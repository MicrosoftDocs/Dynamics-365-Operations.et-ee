---
title: Tagasimakse halduse parameetrid
description: See artikkel kirjeldab tagasimakse halduse parameetrite lehte. See leht sisaldab sätteid, mis mõjutavad sisestamist, oleku uuendusi, numbriseeriaid ja muid käitumist.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 218c54d97f3ac204e8613f5efdda0cc9d713ee04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895521"
---
# <a name="rebate-management-parameters"></a>Tagasimaksehalduse parameetrid.

[!include [banner](../includes/banner.md)]

Lehte **Tagasimakse halduse parameetrid** kasutatakse sätete määratlemiseks, mis kehtivad kogu **Tagasimakse haldus** moodulis. Need sätted mõjutavad sisestamist, oleku uuendusi, numbriseeriaid ja muid käitumist. Selle lehe seadistus on ühiskasutuses juriidiliste isikute vahel ja seda saavad muuta kasutajad, kellel on vastavad turvaõigused.

Lehe **Tagasimaksete halduse parameetrid** avamiseks minge jaotist **Allahindluse haldus \>Seadistamine \> Tagasimaksehalduse parameetrid**. Seejärel häälestage järgmistes alljaotistes kirjeldatud väljad.

## <a name="rebate-management-tab"></a>Tagasimaksehalduse vahekaart

Järgmine tabel kirjeldab välju, mis on saadaval lehe **Tagasimaksehalduse parameetrid** vahekaardil **Tagasimaksehaldus**.

| Field | Kirjeldus |
|---|---|
| Vaikeolek | Saate valida kõigi uute tehingute vaikeoleku. Saadavaloleva valikuna olekuväärtuste komplekti määratlemiseks kasutage [lehekülge **Tagasimakse olekud**](rebate-statuses.md). |
| Dimensioonidega töötlus | Valige, kas finantsdimensioon töötleb eraldise, tagasimakse ja mahakandmiskandeid. Kui see suvand on sisse lülitatud, kasutab süsteem finantsdimensioone lähtekannetest sihtkannetesse. |
| Kontrolli üle varasemat sisestust | <p>Valige süsteemi käitumine, kui sisestamata tagasimaksekandeid töödeldakse sama perioodi jooksul rohkem kui üks kord.</p><ul><li>**Hoiatus** – süsteem lubab kasutajatel algsed kanderead üle kirjutada, kuid vastavasisuline hoiatus kuvatakse.</li><li>**Tõrge** – süsteem takistab kasutajatel algsete kannete ridu üle kirjutada ja kuvatakse tõrketeade. |
| Töölehtede automaatne sisestamine | Saate valida, kas süsteem peaks soovitatud töölehed automaatselt sisestama. Need töölehed sisaldavad igapäevaseid töölehti, mida kasutatakse sätete ja kliendi mahaarvamiste jaoks, samuti müüja maksuarvete töölehti. |
| Vabas vormis arvete automaatne sisestamine | Saate valida, kas süsteem peaks vabas vormis arved automaatselt sisestama. See valik rakendub ainult vabas vormis arvetele, kus maksetüübiks on seatud *Maksuarve kliendi mahaarvamised*. |
| Tagasimakse kauba tellimuse viide | Valige tagasimakse protsessist loodud müügi- ja ostutellimustel kasutamiseks tagasimakse viide (*Puudub*, *Allahindluse halduse tehing*, *Allahindluse halduse number*, *Tagasimakse kande number* või *Dokumendi märkused*). |
| Nõude töötlemise kasutamine | <p>Nõuete töötlemise kasutamiseks määrake suvandi väärtuseks *Jah*. Sel viisil saate märkida kanded, mille tagasimaksehaldus loob, kas nõudel või lahtiütlusena, ja seejärel sisestada ainult nõudega kanded.</p><p>Näiteks arvutate tagasimakseid kuu kannete väärtuse kohta, kuid klient on jätnud kaks päeva väljanõudmata. Sel juhul luuakse tagastamata kanded uuesti järgmisel korral, kui käivitate järgmise perioodi funktsiooni *Töötle*.</p><p>Kui seate valiku väärtuseks *Ei*, sisestatakse kõik nõude kanded.</p> |
| Kaasa tellimuse tüübi tööleht | Tehingute või tehinguridade puhul, kus kande tüübiks on määratud *Tellimus*, määrab see valik, kas kaasata tuleks ka müügitellimus, mille tüüp on *Tööleht*. See pakub paindlikkust, kui neid tellimuste tüüpe kasutatakse stsenaariumites, kus tagasimakset veel ei tuleks rakendada. |

## <a name="number-sequences-tab"></a>Vahekaart Numbriseeriad

Kasutage lehe **Tagasimaksehalduse parameetrid** vahekaarti **Numbriseeriad** numbriseeriate määramiseks erinevatele numbriseeriatele, mida tagasimaksehaldus kasutab. Järgmine tabel kirjeldab kõigi nende numbriseeriate eesmärki. Lisateavet numbriseeriate kohta vt numbriseeriate [ülevaatest ja](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) selle seotud artiklitest.

| Viide | Kirjeldus |
|---|---|
| Tagasimakse halduse pakkumine | Numbriseeria määrab igale tagasimakse tehingule kordumatu võtmeväärtuse. Võtit kasutatakse tehingute loomisel. |
| Allahindluse halduse number | Numbriseeria määrab igale tagasimaksele kordumatu võtmeväärtuse. Seda võtit kasutatakse tagasimakseseoste tuvastamiseks. |
| Tagasimakse kande number | Numbriseeria määrab igale tagasimakse kandele kordumatu võtmeväärtuse. Seda võtit kasutatakse tagasimakse kannete tuvastamiseks. |
| Maksuarve | Numbriseeria määrab igale tagasimakse arvele kordumatu võtmeväärtuse. Võtit kasutatakse tagasimakse töölehtede automaatsel sisestamisel. |

## <a name="feature-visibility-tab"></a>Vahekaart Funktsioonide nähtavus

Tagasimaksehaldus lisab funktsioone (välju ja funktsioone) mitmele lahenduses Microsoft Dynamics 365 Supply Chain Management sageli kasutatavale lehele. Need leheküljed sisaldavad lehekülgi, mis on seotud müügitellimuste ja -tehingutega. Tagasimaksehalduse kasutamise korral peate need funktsioonid enne nende kasutamist kõigi jaoks nähtavaks tegema. Kui te ei kasuta tagasimaksehaldust, saate soovi korral funktsioonid peita.

Tagasimaksehalduse saadaolevate funktsioonide nähtavaks tegemiseks seadke lehe **Tagasimaksehalduse parameetrid** vahekaardil **Funktsioonide nähtavus** suvandi **Aktiveeri** väärtuseks *Jah*. Seadke väärtuseks *Ei*, et peita funktsioonid tavalehtedel väljaspool moodulit **Tagasimaksehaldus**. Ent isegi siis, kui suvandi väärtuseks on seatud *Ei*, jääb moodul ise, sh leht **Tagasimaksehalduse parameetrid**, kättesaadavaks kasutajatele, kellel on sellele juurdepääsemiseks õiged load.
