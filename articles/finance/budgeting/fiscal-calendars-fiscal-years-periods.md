---
title: Rahanduskalendrid, rahandusaastad ja -perioodid
description: Selles artiklis käsitletakse rahanduskalendreid, rahandusaastaid ja -perioode ning seda, kuidas neid kasutada juriidiliste isikute, põhivara ja eelarvestamise puhul.
author: aprilolson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: roschlom
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7179b2d14025ca2ec32d3dabc8eea42edda473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822053"
---
# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Rahanduskalendrid, rahandusaastad ja -perioodid

[!include [banner](../includes/banner.md)]

Selles artiklis käsitletakse rahanduskalendreid, rahandusaastaid ja -perioode ning seda, kuidas neid kasutada juriidiliste isikute, põhivara ja eelarvestamise puhul.

Rahanduskalendrid annavad organisatsiooni finantstegevusele raamistiku. Iga rahanduskalender sisaldab ühte või mitut rahandusaastat ja iga rahandusaasta sisaldab mitut perioodi. Rahanduskalender võib põhineda kalendriaastal 1. jaanuarist 31. detsembrini või teie valitud kuupäevadel. Näiteks mõnes organisatsioonis valitakse rahanduskalender, mis algab 1. juulil ja lõpeb järgneva aasta 30. juunil. 

Rahanduskalendrite arv, mida saate luua, on piiramatu ja piiramatu on ka rahanduskalendri jaoks loodavate rahandusaastate arv. Iga rahanduskalender on teie ettevõttest sõltumatu ja seda saab kasutada mitme juriidilise isiku jaoks organisatsioonis. Näiteks on organisatsioonis kaheksa osakonda ja iga osakond on eraldi juriidiline isik. Viis neist jagavad sama rahanduskalendrit ja kolm kasutavad erinevaid rahanduskalendreid. Saate luua ühe rahanduskalendri nende viie juriidilise isiku jaoks, kes sama rahanduskalendrit jagavad, ja eraldi rahanduskalendri teistele juriidilistele isikutele.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Rahanduskalendrite, rahandusaastate ja perioodide loomine
Saate luua ja kustutada rahanduskalendreid, rahandusaastaid ja -perioode lehel Rahanduskalendrid. Saate jagada ka olemasolevaid perioode ja luua rahandusaasta sulgemiseks kasutatavaid sulgemisperioode. 

Sulgemisperioodi kasutatakse pearaamatukannete eraldamiseks, mis luuakse, kui majandusaasta on suletud. Kui sulgemiskanded on ühes rahandusperioodis, on lihtsam luua finantsaruandeid, mis sisaldavad või jätavad välja eri liiki sulgemiskandeid. Kui rahandusaasta on jaotatud 12 rahandusperioodiks, on sulgemise periood tavaliselt 13. periood. Siiski saab luua sulgemisperioodi igast perioodist, mille olek on Avatud. 

Sulgemisperioodi loomisel saate valida perioodi, mille olek on Avatud ja millel on kuupäevad, mida soovite kasutada. Uus sulgemisperiood kopeerib algus- ja lõppkuupäevad olemasolevast perioodist. Esialgne periood on jätkuvalt olemas. Näiteks valite perioodi 12, mis on majandusaasta viimane periood, ja mille kuupäevad on 1. august kuni 31. august. Sisestate sulgemisperioodi nime, näiteks Sulgemine. Pärast uue sulgemisperioodi loomist on teil nüüd esialgne periood ja sulgemisperiood. Mõlemal on kuupäevad, mis algavad 1. augustil ja lõpevad 31. augustil.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Rahanduskalendrite valimine pearaamatute, põhivarade ja eelarvetsüklite jaoks
Rahanduskalendreid kasutatakse põhivara kulumi, finantskannete ja eelarvetsüklite puhul. Rahanduskalendri loomisel saate kasutada seda mitmeks otstarbeks. Saate valida rahanduskalendri põhivararaamatule, muutes selle põhivarakalendriks. Saate valida rahanduskalendri pearaamatule, muutes selle pearaamatukalendriks. Ning saate valida rahanduskalendri eelarvetsüklile, muutes selle eelarvekalendriks. Saate kasutada sama rahanduskalendrit kõigis nendes olukordades.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Rahanduskalendri valimine juriidilise üksuse jaoks

Valige rahanduskalender, mida soovite kasutada oma juriidilise isiku pearaamatu puhul, vormilt Pearaamat. Lehel Pearaamat peab iga juriidilise isiku jaoks olema valitud rahanduskalender. Pärast rahanduskalendri valimist saate seadistada perioodi olekuid ja lube lehel Pearaamatukalender mis tahes perioodi jaoks, mis on majandusaasta osa.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Rahanduskalendri valimine põhivara jaoks

Saate valida rahanduskalendri põhivararaamatu jaoks ja seda rahanduskalendrit kasutavad põhivarad, mis vastavat raamatut kasutavad. Saate valida ükskõik millisest lehel Rahanduskalendrid määratletud rahanduskalendrist.

### <a name="define-budget-cycle-time-spans"></a>Eelarvetsükli perioodide määratlemine

Eelarvetsüklid on ajavahemik, mille jooksul eelarvet kasutatakse. Eelarvetsüklid võivad hõlmata osa rahandusaastast või mitut rahandusaastat, näiteks iga kahe aasta järel aset leidev kaheaastane eelarvetsükkel või iga kolme aasta järel aset leidev kolmeaastane eelarvetsükkel. Eelarvetsükli periood määratleb eelarvetsüklis sisalduvate perioodide arvu. Eelarvetsükli perioodi määramiseks kasutage lehte Eelarvetsükli perioodid.

## <a name="maintain-periods-for-your-organization"></a>Organisatsiooni perioodide haldamine
Võite kasutada lehte Pearaamatukalender oma organisatsiooni rahanduskalendri, rahandusaastate ja perioodide üksikasjade vaatamiseks. Samuti saate perioodide olekut muuta ja valida, millised kasutajad saavad perioodidele raamatupidamiskandeid sisestada. Näiteks uue perioodi alguses võite soovida, et mõni kasutajagrupp lõpetaks finantskannete sisestamise eelnevasse perioodi, samas kui teised grupid töötavad ainult uues perioodis.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]