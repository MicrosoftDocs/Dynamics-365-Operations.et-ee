---
title: Osakondade loomine ja nende kaasamine osakonnahierarhiasse
description: Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala. Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid. Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks. Osakonnad võivad vastutada kasumi ja kahjumi eest.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 14e0acb2ea16641eecb81bcf23c8b7d778b2b208
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304036"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Osakondade loomine ja nende kaasamine osakonnahierarhiasse

[!include [banner](includes/banner.md)]

Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala. Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid. Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks. Osakonnad võivad vastutada kasumi ja kahjumi eest.

Osakond võib sisaldada kulukeskuste gruppi. Ametikohti saab määrata osakondadele. Osakonna loomiseks klõpsake valikuid **Inimressursid** &gt; **Osakonnad** &gt; **Osakonnad**. Järgmises tabelis on kirjeldatud saadaolevaid välju.

| Väli               | Kirjeldus                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nimi                | Sisestage osakonnale nimi.                                                                                                                                                                                  |
| Osakonna number   | Vaikeväärtus võidakse luua automaatselt, kui viitele **Organisatsiooni kood** lehel **Numbriseeriad** määratakse numbriseeria kood.                                                 |
| Otsingunimi         | Sisestage nimi või lühend, mida osakonna otsimiseks kasutada.                                                                                                                                            |
| Memo                | Sisestage kogu lisateave siia.                                                                                                                                                                            |
| Hierarhias        | Valitud ruut näitab, et osakond on lisatud osakonnahierarhiasse. Lisateavet osakonna lisamise kohta osakonnahierarhiasse vt järgnevat artikli teavet. |
| DUNS-number         | DUNS tähendab andmete universaalset nummerdussüsteemi. See on üheksakohaline number, mille väljastab Dun & Bradstreet.                                                                                                     |
| Juhataja             | Sisestage isik, kes osakonda juhib.                                                                                                                                                                    |
| Aadressid           | Lisage osakonna aadress. Näiteks lisage hoone postiaadress, kus osakond asub.                                                                          |
| Kontaktteave | Lisage osakonna kontakkteave. Näiteks lisage osakonna kasutajatoe telefoninumber.                                                                                           |

Osakonna lisamiseks osakonnahierarhiasse toimige järgmiselt.

1.  Klõpsake valikuid **Inimressursid** &gt; **Osakonnad** &gt; **Osakonnahierarhia**.
2.  Klõpsake suvandit **Redigeeri** ja valige seejärel organisatsioon, mille alla peaks osakond kuuluma.
3.  Klõpsake suvandit **Sisesta** ja valige loendist suvand **Osakond**.
4.  Valige ilmuvast osakondade loendist hierarhiasse lisatav osakond.
5.  Salvestage muudatused. Saate teate, et loodud on hierarhia mustandversioon.
6.  Kui olete lõpetanud, klõpsake hierarhiakujundajas valikut **Avalda**. Saate sisestada jõustumiskuupäeva, mis näitab, millal hierarhia avaldada. Näiteks uue osakonna lisamiseks järgmise kalendriaasta alguses määrake jõustumiskuupäevaks uue kalendriaasta 1. jaanuar. Muudatused hierarhias jüustuvad sel kuupäeval.

## <a name="steps-for-creating-a-department"></a>Osakonna loomise juhised
Uue osakonna loomise etapiviisilise protseduuri leiate teemast [Uute osakondade määratlemine](../fin-and-ops/hr/tasks/define-new-departments.md). 
