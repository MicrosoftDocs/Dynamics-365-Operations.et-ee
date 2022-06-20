---
title: Teenuse tellimused
description: See artikkel annab ülevaate, kuidas teenusetellimustega töötada.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 606a1e3df72f8a76dab477bb1dd961b6df16f3cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882369"
---
# <a name="service-orders"></a>Teenuse tellimused

[!include [banner](../includes/banner.md)]

Hooldustellimus näitab hooldustehniku külastust kliendi laoalasse konkreetsel kuupäeval. Iga teenuse tellimus koosneb ühest või mitmest teenuse tellimuse reast. Hooldustellimuse ridadel on toodud hooldustehniku töötunnid ning seotud kaubad, kulud ja tasud.

Hooldustellimuse reale saab lisada ülesandeid ja objekte. Seejärel saate grupeerida hooldustellimuse ridu ülesande või objekti järgi. Saate hooldustellimuste ridadele lisada ka laos loetletud kaupu.

## <a name="create-service-orders"></a>Hooldustellimuste loomine

Saate luua hooldustellimusi teenuseleppe ja selle leppe ridade alusel. Kuid saate luua teenuseleppega seotud hooldustellimusi vaid leppes määratud perioodi jooksul. Näiteks kui teenuselepe kehtib kalendriaasta 2011 kohta, saate luua hooldustellimusi leppe kohta alates 1. jaanuarist 2011 kuni 31. detsembrini 2011.

Saate hooldustellimusi luua ka eraldi, ilma nende määramiseta leppele. Neid hooldustellimusi saab kasutada plaanimata või ühekordsete teenusekülastuste haldamiseks. Näiteks märtsikuus soovib teie klient, et teenust tehtaks kahel masinal lisaks teenuseleppes määratud masinatele. Selle ülesande jaoks saate luua hooldustellimusi, kuid ärge seostage neid leppega.


> [!NOTE]
> Teenuseleppega mitte seostatud hooldustellimuste loomiseks peate valima märkeruudu **Luba teenuseleppeta** lehel **Teenuste halduse parameetrid**.

### <a name="scenario"></a>Stsenaarium

Järgmises stsenaariumis kirjeldatakse olukorda, kus on kasulik luua hooldustellimus, mida ei ole seostatud teenuseleppega.

Ettevõtte dispetšer võtab vastu telefonikõne, kus nõutakse lifti erakorralist teenust. Teenuseleppe ja teenuse jaoks projekti seadistamiseks pole aega. Seetõttu loob dispetšer hooldustellimuse otse lehel **Hooldustellimused**, lisab olemasolevale projektile hooldustellimuse ja loob hooldustellimuse read. Dispetšer loob ka olemasolevale hooldustellimusele tööülesande või objekti seose, et kirjendada teenuselepinguga mitte seotud töö. Lisateavet vt teemadest [Hooldustellimuste loomine käsitsi](create-service-orders-manually.md) ja [Hooldustoimingute seoste loomine](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Hooldustellimuste edenemise jälgimine

Hooldustellimuse edenemise jälgimiseks läbi eri meeskondade tööprotsesside saate seadistada hooldustellimustele etappide ja põhjusekoodide süsteemi. Iga etapi jaoks saate määrata lubatud toimingud. Lisateavet põhjusekoodide kohta vt teemast [Põhjusekoodide loomine](create-reason-codes.md).

### <a name="example"></a>Näide

Dispetšer kinnitab hooldustellimuse. Dispetšer värskendab hooldustellimuse etappi ja määrab põhjusekoodi, mis näitab, et hooldustellimus on väljastatud hooldustehnikule. Tehnik läheb kliendi laoalasse ja täidab teenuse.

## <a name="specify-item-requirements-for-service-orders"></a>Kaubavajaduse määramine hooldustellimuste jaoks

Saate määrata hooldustellimuste jaoks vajalikke laokaupu. Kuid hooldustellimus peab olema seotud projektiga. Teenusetellimuste kaubavajadusi töödeldakse projekti kaudu. 

### <a name="example"></a>Näide

Teenuseleppest loodud hooldustellimusi töötleb dispetšer. Esmasel hooldustellimusel tõdeb dispetšer, et hooldustehnikul on vaja olulist varuosa, mida laos eelnevalt pole. Seetõttu loob dispetšer varuosa kaubavajaduse otse hooldustellimusest.

## <a name="move-and-post-lines"></a>Ridade teisaldamine ja sisestamine

Hooldustehnik naaseb teenusekülastuselt ning muudab ja uuendab hooldustellimuste ridu. Teenusekülastuse ajal täitis tehnik teenusetööd, mis planeeriti järgmiseks teenusekülastuseks. Seetõttu teisaldab tehnik read järgmiselt teenusekülastuselt praegusele teenusekülastusele. Tehnik sisestab hooldustellimuse. Lisateavet vt teemast [Hooldustellimuse ridade teisaldamine](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Tühista teenuse tellimused

Üks jaanuariks loodud muudest hooldustellimustest muutub aegunuks, sest töö tühistati. Seetõttu tühistab dispetšer hooldustellimuse. Lisateavet vt teemast [Hooldustellimuste tühistamine](cancel-service-orders.md).

## <a name="post-from-projects"></a>Sisestamine projektidest

Iga nädala lõpus soovib dispetšer sisestada kõik konkreetsele projektile lisatud hooldustellimused. Seega määrab dispetšer asjakohase projekti asukoha lehel **Projektid** ja sisestab lõpetatud hooldustellimused. Lisateavet vt teemast [Hooldustellimuste sisestamine (klassi vorm)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Kustuta teenuse tellimused

Aasta teisel poolel otsustab teie klient, et teenusekülastused on liiga harvad. Peate looma uue, sagedasema teenusekülastuste seeria teenuselepingu allesjäänud ajaks. Seepärast peate kustutama olemasolevad hooldustellimused ja looma uued hooldustellimused. Lisateavet vt teemast [Hooldustellimuste kustutamine](delete-service-orders.md).

## <a name="see-also"></a>Vt ka

[Teenusetellimused (vorm)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]