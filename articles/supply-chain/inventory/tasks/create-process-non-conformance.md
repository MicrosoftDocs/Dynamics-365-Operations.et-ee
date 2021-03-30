---
title: Vastavuse loomine ja töötlemine
description: Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef9c3a06aed1d26e7f5648427178a5638027ec04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218677"
---
# <a name="create-and-process-a-conformance"></a>Vastavuse loomine ja töötlemine

[!include [banner](../../includes/banner.md)]

Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal. Saate käivitada selle salvestise demoettevõttes USMF ja kasutada soovitatud väärtusi. Tavaliselt teostab selle protseduuri kvaliteediametnik.  Eeltingimusena täitke juhised jaotises [Kontrollige kaupade kvaliteeti](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md). Mittevastavuse kinnitamise töötlemiseks peab ülesandesalvestist käitavale kasutajale olema lehel Kasutajad määratud väärtus „Nimi”. Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.


## <a name="select-a-quality-order"></a>Kvaliteettellimuse valimine
1. Navigeerimispaanil avage **Moodulid > Varud > Perioodilised ülesanded > Kvaliteethaldus > Kvaliteettellimus**.
2. Valige loendist kvaliteettellimus, mis loodi jaotises [Kontrolli kaupade kvaliteeti](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Mittevastavuse loomine
1. Toimingupaanil valige **Päringud**.
2. Valige **Mittevastavused**.
3. Valige suvand **Uus**.
4. Rippmenüü väljal **Probleemi tüüp** valige probleem, mis leiti kontrollimise protsessi käigus.  
5. Valige nupp **OK**.

## <a name="approvereject-a-nonconformance"></a>Mittevastavuse kinnitamine/tagasilükkamine
1. Valige **Funktsioonid**.
2. Valige **Kinnita mittevastavus**. Selles näites kinnitage mittevastavus. Kinnitatud mittevastavusi saab seostada seotud toimingutega, et salvestada töö, mis on tehtud osana mittevastavusi käsitlemisest ja nagu selles teemas, paranduste käsitlemise töötlemisel.  
3. Valige **Jah**.

## <a name="create-a-correction-action"></a>Parandustegevuse loomine
1. Valige **Parandused**.
2. Valige suvand **Uus**.
3. Uue rea väljal **Personalinumber** valige rippmenüüst soovitud kirje.
4. Klõpsake **Vali**.
5. Valige **Manusta**. Looge paranduse kohta märkus. Selles näites on tegevuseks hankijaga ühenduse võtmine, et arutleda mittevastavuse juhtumit.  
6. Valige suvand **Uus**.
7. Valige **Märge**. Sõltuvalt aruande seadistusest saab eri dokumendi tüüpe printida aruannetele, mis on seotud mittevastavuse haldusega.  
8. Sisestage väärtus väljale **Kirjeldus**.
9. Sulgege leht.

## <a name="maintain-a-correction"></a>Paranduse haldamine
1. Valige **Märgi lõpuleviiduks**.
2. Valige nupp **OK**.
3. Sulgege leht.

## <a name="close-a-nonconformance"></a>Mittevastavuse sulgemine
1. Valige **Funktsioonid**.
2. Valige **Sulge mittevastavus**.
3. Valige **Jah**.
4. Sulgege lehed.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]