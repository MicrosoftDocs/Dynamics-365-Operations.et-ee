---
title: Kiirimport/-eksport
description: Kiirimpordi/-ekspordi eesmärk on lasta teil importida ja eksportida väiksema toimingute arvuga.
author: margoc
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: e57b75fc1a697958d6a6e739ad809952217d3b4f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744783"
---
# <a name="quick-import-export"></a><span data-ttu-id="33d7e-103">Kiirimport/-eksport</span><span class="sxs-lookup"><span data-stu-id="33d7e-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33d7e-104">Kiirimpordi/-ekspordi eesmärk on lasta teil importida ja eksportida väiksema toimingute arvuga.</span><span class="sxs-lookup"><span data-stu-id="33d7e-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="33d7e-105">Lisasime kiirimpordi/-ekspordi funktsiooni, et kasutajad saaksid importida või eksportida lihtsaid töid, mida nad soovivad kiiresti teha.</span><span class="sxs-lookup"><span data-stu-id="33d7e-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="33d7e-106">Ideaaljuhul kasutatakse seda funktsiooni stsenaariumides, milles fail vastendatakse automaatselt süsteemiga ja kasutaja ei pea tegelema täpsema vastendamisega ega looma korduvaid impordi- või eksporditöid.</span><span class="sxs-lookup"><span data-stu-id="33d7e-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="33d7e-107">See funktsioon toetab töötamise nii valmis kui ka kohandatud olemitega.</span><span class="sxs-lookup"><span data-stu-id="33d7e-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="33d7e-108">Saate failidest importida ja kui kasutate ODBC-andmeallikat, võite valida päringu, mida oma impordi määratlemiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="33d7e-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="33d7e-109">Peate olema eelnevalt määratlenud lähteandmete vormingud AX-ile või failile ja teadma, kus need asuvad.</span><span class="sxs-lookup"><span data-stu-id="33d7e-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="33d7e-110">Kiirimpordi/-ekspordi kasutamiseks pole vaja töötlemisrühma luua; see luuakse süsteemis automaatselt impordi- või eksporditöö käitamisel.</span><span class="sxs-lookup"><span data-stu-id="33d7e-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="33d7e-111">Saate valida ka kiirimpordi/-ekspordi ajaloo säilitamise.</span><span class="sxs-lookup"><span data-stu-id="33d7e-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="33d7e-112">Arvestage, et kiirimport/-eksport eeldab, et oleksite DIXF-i mõistetega kursis.</span><span class="sxs-lookup"><span data-stu-id="33d7e-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>





[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]