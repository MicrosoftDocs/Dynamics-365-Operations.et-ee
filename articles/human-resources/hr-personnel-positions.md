---
title: Ametikohad
description: See teema kirjeldab kontseptuaalseid elemente, mida ametikoht võib sisaldada. See pakub ka näiteid, mis näitavad, kuidas te saate neid elemente oma organisatsioonis kasutada.
author: twheeloc
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0b11458ac5d41d08a245a1f5aa48fb4633ae075
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534297"
---
# <a name="positions"></a>Ametikohad


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema kirjeldab kontseptuaalseid elemente, mida ametikoht võib sisaldada. See pakub ka näiteid, mis näitavad, kuidas te saate neid elemente oma organisatsioonis kasutada.

Enne ametikoha loomist tuleb seadistada töö. Mõned ametikoha üksikasjad, nt kompensatsioonipiirkond, töötaja määramine, positsiooni kestus ja aruandlussuhe, on kehtivuskuupäevad.

## <a name="general-information"></a>Üldteave

Ametikoha loomisel, peate valima töö. Järgmine teave sisestatakse automaatselt valitud tööst:

- Kirjeldus
- Pealkiri
- Täistööaja vaste
- Tööpere

Ametinimetust kasutatakse töötaja ametinimetustele viitamiseks. (Töötajal loetletud pealkirja ei kasutata.) Seetõttu tuleks ametinimetused standardiseerida nii palju, kui võimalik.

> [!NOTE]
> Töötajat ei saa ametikohale määrata kuupäeval, mis on varasem määramise saadaolevast kuupäevast.
>
> Parameeter **Positsioonid** vahekaardil **Inimressursside jagatud parameetrite** lehel juhib töötaja määramise käitumist. Valige üks järgmistest väärtustest.
>
> - **Alati** – ametikohtade loomisel saate töötajaid uutele ametikohtadele määrata. Ametikohtade loomisel seatakse valiku **Määramiseks saadaval** kuupäev ja kellaaeg lehe **Ametikoht** vahekaardil **Üldine** automaatselt loomise kuupäevale ja kellaajale.
> - **Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata. Kui valite selle suvandi, peate avama lehekülje **Ametikoht** iga uue ametikoha jaoks, kui see muutub kättesaadavaks. Seejärel sisestage **Üldine** vahekaardil **määramise jaoks** töötaja määramise lubamiseks kuupäeva. Kui valite selle suvandi, seatakse töötaja määramise kuupäevaks vaikimisi **mitte kunagi** kui proovite töötajat määrata.

## <a name="position-duration"></a>Positsiooni kestus

Iga ametikoht kehtib teatud aja jooksul, mida nimetatakse kestuseks. Näiteks võib suviste ametikohtade kestus olla 1. maist 2021 kuni 31. augustini 2021. Aktiveerimiskuupäev on kuupäev, mil ametikoht on süsteemis aktiivne. Lõpetamise kuupäev on kuupäev, millest ametikoht pole süsteemis enam aktiivne.

Pange tähele, et saadaolev määramise kuupäev ega töötaja määramise kuupäev ei saa olla enne aktiveerimiskuupäeva. Ametikoht ei loeta aktiivseks enne aktiveerimiskuupäeva saavutatud. Töötajamäärang ei saa ametikoha lõpetamise kuupäevast edasi minna.

## <a name="reports-to-position"></a>Millisele ametikohale annab aru

Ametikohad on organisatsioonihierarhia madalama taseme olulised elemendid. Lehel **Ametikoht** saate määrata positsiooni, millele see ametikoht aru annab. Kui määrate töötaja ametikohale, mis annab aru teisele ametikohale, loote neile kahele ametikohale määratud töötajate vahel aruandlusseose. Näiteks annab 000220 aru ametikohale 000300. Kim Akers on määratud ametikohale 000220 ja Sanjay Patel amekohale 000300. Seetõttu esitab Kim Akers aruandeid Sanjay Patelile.

> [!TIP]
> Positsioonile aruandeid kasutatakse kogu süsteemis, et määrata, kes on töötaja ülemus. Eelnevas näites, kui halduri roll on määratud süsteemis Sanjay Patelile, näeb ta Kim Akersi juhataja iseteeninduskeskuses otse aruandena. Aruandlussuhet saab kasutada ka töövoo protsessireeglite ja kontroll-loendi ülesannete loomisel.

## <a name="relationships"></a>Seosed

Kui teie organisatsioon kasutab maatrikshierarhiat või muud kohandatud hierarhiat, saate seadistada ametikoha hierarhiatüübid. Seejärel saate lisada aruandlusseosed ametikohtadele iga seadistatud hierarhiatüübi puhul. Näiteks on Lori Penor Adventure Worksi üldjuhataja ja määratud ametikohale **üldjuht**. Lori haldab tööriistade puhastamiseks kasutatava toote arendust. Ta palub raamatupidajalt abi oma finantsidega. Seetõttu palkas ta Kim Akersi oma raamatupidajaks. Kim annab otse aru Sanjay Patelile, kuid ta töötab ka Lori Penorile seoses tööriistapuhasti arendusfinantsidega.

Eelmise näite puhul peate täitma järgmised ülesanded, et seadistada tööseos Kim Akers and Lori Penori vahel:

1. Looge kohandatud ametikohahierarhia tüüp nimega **Tööriist**, et luua hierarhia, mis sisaldab tööriistapuhastustootega seotud tööde eest vastutatavaid ametikohti.
2. Määrake **üldjuhi** ametikoht ametikohaks, millele Kimi ametikoht aru annab **Tööriista** hierarhias.
3. Ametikohahierarhia abil saate vaadata ametikohtade aruandlusstruktuuri. Kui teil on mitu ametikohahierarhiat, saate vaadata ametikohahierarhia iga hierarhiatüübi hierarhiat. Samuti saate otsida ametikohta ametikoha ID või ametikohale määratud töötaja nime järgi. Ametikohahierarhia on organisatsioonihierarhia.

## <a name="labor-union"></a>Ametiühing

Saate kirjendada, kas ametikoha jaoks on nõutav ametiühinguleping ja millist ametiühingut kasutatakse. Saate lepingu seostada ka juriidilise isikuga.

## <a name="financial-dimensions"></a>Finantsdimensioonid

Kui loote ametikohale finantsdimensiooni, peate määrama juriidilise isiku. Vaikedimensioone saate valida iga dimensiooni puhul eraldi. Teise võimalusena saate vaikedimensioonide automaatseks täitmiseks valida jaotusmalli. Jaotusmall pakub ka võimalust eraldada summasid mitme dimensiooniväärtuse vahel.
