---
title: Globaalse aadressiraamatu ja muude aadressiraamatute plaanimine
description: Selles teemas kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui globaalse aadressiraamatu ning mis tahes täiendava aadressiraamatu seadistate ja konfigureerite.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a0613b944d0446e339480a71fa890702190ed53
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559961"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="65ddf-103">Plaan globaalse aadressiraamatu ja muude aadressiraamatute jaoks</span><span class="sxs-lookup"><span data-stu-id="65ddf-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65ddf-104">Selles teemas kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui globaalse aadressiraamatu ning mis tahes täiendava aadressiraamatu seadistate ja konfigureerite.</span><span class="sxs-lookup"><span data-stu-id="65ddf-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="65ddf-105">Mõned otsused nõuavad toote mõnes muus valdkonnas (nt organisatsiooni hierarhia) tehtud otsuste kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="65ddf-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="65ddf-106">Globaalne aadressiraamat</span><span class="sxs-lookup"><span data-stu-id="65ddf-106">Global address book</span></span>

<span data-ttu-id="65ddf-107">Enne kui alustate tööd globaalse aadressiraamatuga, peate määratlema selle jaoks vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="65ddf-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="65ddf-108">Neid vaikeväärtusi kasutatakse siis kõigi täiendavate aadressiraamatute puhul, mille loote.</span><span class="sxs-lookup"><span data-stu-id="65ddf-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="65ddf-109">**Otsused**</span><span class="sxs-lookup"><span data-stu-id="65ddf-109">**Decisions**</span></span>

- <span data-ttu-id="65ddf-110">Millises järjekorras tuleks nimed kuvada osapoolekirjete puhul tüübiga **Isik**?</span><span class="sxs-lookup"><span data-stu-id="65ddf-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="65ddf-111">Näiteks üks järjekord oleks perekonnanimi, teine eesnimi ja eesnimi.</span><span class="sxs-lookup"><span data-stu-id="65ddf-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="65ddf-112">Kas osapoolekirjed tuleks aadressiraamatust kustutada, kui rolli kirje kustutatakse?</span><span class="sxs-lookup"><span data-stu-id="65ddf-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="65ddf-113">Näiteks kui kliendi kirje kustutatakse, kas osapoole kirje tuleks samuti kustutada?</span><span class="sxs-lookup"><span data-stu-id="65ddf-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="65ddf-114">Kas uue kirje loomisel tuleks kasutajaid teavitada, kui globaalsest aadressiraamatust leitakse topeltkirje?</span><span class="sxs-lookup"><span data-stu-id="65ddf-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="65ddf-115">Kas osapoole kirje andmetesse tuleks lisada andmete universaalse nummerdussüsteemi (DUNS) number?</span><span class="sxs-lookup"><span data-stu-id="65ddf-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="65ddf-116">Kui DUNS-number on osapoole kirjele lisatud, kas siis tuleks kontrollida numbri kordumatust?</span><span class="sxs-lookup"><span data-stu-id="65ddf-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="65ddf-117">Kas soovite globaalses aadressiraamatus osapoole kirje loomisel kasutada osapoole tüübi, isiku või organisatsiooni vaikeväärtust?</span><span class="sxs-lookup"><span data-stu-id="65ddf-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="65ddf-118">Millistel kasutajarollidel peaks olema juurdepääs osapoole kirjete era-aadressidele ja kontaktandmetele?</span><span class="sxs-lookup"><span data-stu-id="65ddf-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="65ddf-119">Täiendavad aadressiraamatud</span><span class="sxs-lookup"><span data-stu-id="65ddf-119">Additional address books</span></span>

<span data-ttu-id="65ddf-120">Pärast globaalse aadressiraamatu loomist, saate luua vajaduse järgi täiendavaid aadressiraamatuid, näiteks eraldi aadressiraamatu iga ettevõtte jaoks oma organisatsioonis või iga tegevusala jaoks.</span><span class="sxs-lookup"><span data-stu-id="65ddf-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="65ddf-121">Näiteks Fabrikam on rahvusvaheline organisatsioon, millel on mitu ettevõtet ja mitu tegevusala.</span><span class="sxs-lookup"><span data-stu-id="65ddf-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="65ddf-122">Fabrikam plaanib luua iga tegevusala jaoks aadressiraamatu.</span><span class="sxs-lookup"><span data-stu-id="65ddf-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="65ddf-123">Tegevusaladele, millel on mitu asukohta (nt pneumaatiliste tööriistade äri), plaanib Fabrikam luua iga asukoha jaoks aadressiraamatu.</span><span class="sxs-lookup"><span data-stu-id="65ddf-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="65ddf-124">Chris, Fabrikami IT-juht, on loonud järgmise loendi vajalikest aadressiraamatutest.</span><span class="sxs-lookup"><span data-stu-id="65ddf-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="65ddf-125">Selles loendis kirjeldatakse ka osapoole kirjeid, mida iga aadressiraamat peab sisaldama.</span><span class="sxs-lookup"><span data-stu-id="65ddf-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="65ddf-126">**Avaliku sektori lepingud (PubSC)** – kõigi Fabrikami sõlmitud avaliku sektori lepingute kõigi osapoolte kirjed.</span><span class="sxs-lookup"><span data-stu-id="65ddf-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="65ddf-127">**Erasektori lepingud (PriSC)** – kõigi Fabrikami sõlmitud erasektori lepingute kõigi osapoolte kirjed.</span><span class="sxs-lookup"><span data-stu-id="65ddf-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="65ddf-128">**Elektroonilised tööriistad (ET)** – kõigi elektrooniliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-Japan pakutavate või ostetavate elektrooniliste tööriistadega kokku puutuvad.</span><span class="sxs-lookup"><span data-stu-id="65ddf-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="65ddf-129">**Pneumaatilised tööriistad (andmete universaalse nummerdussüsteem)** – kõigi pneumaatiliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-Japan pakutavate või ostetavate pneumaatiliste tööriistadega kokku puutuvad.</span><span class="sxs-lookup"><span data-stu-id="65ddf-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="65ddf-130">**Pneumaatilised tööriistad (PTUSA)** – kõigi pneumaatiliste tööriistade ostu või müügiga seotud osapoolte või selliste osapoolte kirjed, kes muul viisil Fabrikamile firmas Fabrikam-US pakutavate või ostetavate pneumaatiliste tööriistadega kokku puutuvad.</span><span class="sxs-lookup"><span data-stu-id="65ddf-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="65ddf-131">**Otsus.**</span><span class="sxs-lookup"><span data-stu-id="65ddf-131">**Decision:**</span></span>

- <span data-ttu-id="65ddf-132">Mitu täiendavat aadressiraamatut loote?</span><span class="sxs-lookup"><span data-stu-id="65ddf-132">How many additional address books will you create?</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]