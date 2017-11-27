---
title: "Digitaalallkirja ülevaade"
description: "Selles artiklis antakse ülevaade elektronallkirjadest ja kirjeldatakse nende kasutust Microsoft Dynamics 365 for Finance and Operationsis."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 698b938e515ff4755c2f111279cda244577ac9f3
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="electronic-signature-overview"></a><span data-ttu-id="dae71-103">Digitaalallkirja ülevaade</span><span class="sxs-lookup"><span data-stu-id="dae71-103">Electronic signature overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dae71-104">Selles artiklis antakse ülevaade elektronallkirjadest ja kirjeldatakse nende kasutust Microsoft Dynamics 365 for Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="dae71-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-an-electronic-signature"></a><span data-ttu-id="dae71-105">Mis on elektronallkiri?</span><span class="sxs-lookup"><span data-stu-id="dae71-105">What is an electronic signature?</span></span>
--------------------------------

<span data-ttu-id="dae71-106">Elektronallkiri kinnitab isiku, kes käivitab või kinnitab protsessi.</span><span class="sxs-lookup"><span data-stu-id="dae71-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="dae71-107">Mõnes tööstuses on elektronallkiri juriidiliselt sama siduv kui käsitsi kirjutatud allkiri.</span><span class="sxs-lookup"><span data-stu-id="dae71-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> 

<span data-ttu-id="dae71-108">Elektronallkirjad on määrustele vastavuse nõue mitmes reguleeritud tööstusharus, nt farmaatsia-, toiduainete- ja joogi-, ja lennundus ja kaitsetööstuses.</span><span class="sxs-lookup"><span data-stu-id="dae71-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="dae71-109">Need on vajalikud ka vastavuse tagamiseks USA toiduainete ja -ravimiameti väljastatud määruste CFR-i 21. ptk osaga 11.</span><span class="sxs-lookup"><span data-stu-id="dae71-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span> 

<span data-ttu-id="dae71-110">**Märkus.** Elektrooniline allkiri pole sama mis digitaalallkiri.</span><span class="sxs-lookup"><span data-stu-id="dae71-110">**Note:** An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="dae71-111">Elektrooniline allkiri asendab lihtsalt käsitsi kirjutatud allkirja, samal ajal, kui digitaalallkirjaga kaasnevad ka täiendavad turvameetmed.</span><span class="sxs-lookup"><span data-stu-id="dae71-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="dae71-112">Digitaalallkirja abil saab tuvastada kas teine kasutaja või protsess on andmeid rikkunud.</span><span class="sxs-lookup"><span data-stu-id="dae71-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="dae71-113">Digitaalallkirja saab ka kinnitada ja omanik, kellele andmete allkirjastamise sertifikaat kuulub, ei saa seda ümber lükata.</span><span class="sxs-lookup"><span data-stu-id="dae71-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="dae71-114">Nagu allpool kirjeldatud, on Microsoft Dynamics 365 for Finance and Operationsi elektronallkirjadel sisseehitatud digitaalallkirja funktsioon.</span><span class="sxs-lookup"><span data-stu-id="dae71-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="dae71-115">Elektronallkirjad Dynamics 365 for Finance and Operationsis</span><span class="sxs-lookup"><span data-stu-id="dae71-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="dae71-116">Finance and Operationsis saate kasutada tähtsateks äriprotsessideks elektronallkirju.</span><span class="sxs-lookup"><span data-stu-id="dae71-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="dae71-117">Mõnedel protsessidel on sisseehitatud elektronallkirja võimalused.</span><span class="sxs-lookup"><span data-stu-id="dae71-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="dae71-118">Igale andmebaasi tabelile või väljale saate luua ka allkirjanõuded.</span><span class="sxs-lookup"><span data-stu-id="dae71-118">You can also create custom signature requirements for any database table and field.</span></span> 

<span data-ttu-id="dae71-119">Elektronallkirjadel on sisseehitatud digitaalallkirja funktsioon.</span><span class="sxs-lookup"><span data-stu-id="dae71-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="dae71-120">Iga dokumenti allkirjastav kasutaja peab hankima kehtiva krüptograafilise serdi.</span><span class="sxs-lookup"><span data-stu-id="dae71-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="dae71-121">Dokumendi allkirjastamisel kinnitatakse sertifikaadiga seostuv privaatvõti.</span><span class="sxs-lookup"><span data-stu-id="dae71-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="dae71-122">Finance and Operations salvestab elektronallkirja teabe kontrolljälje pakkumiseks logisse.</span><span class="sxs-lookup"><span data-stu-id="dae71-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="dae71-123">Teavet elektrooniliste allkirjade seadistamise kohta vt teemast [Elektrooniliste allkirjade seadistamine (tegevuse juhis)](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="dae71-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="dae71-124">Kasutajad, kes vajavad juurdepääsu elektronallkirjadele</span><span class="sxs-lookup"><span data-stu-id="dae71-124">Users who require access to electronic signatures</span></span>
<span data-ttu-id="dae71-125">Kolme tüüpi kasutajad vajavad tavaliselt turvapääsu digitaalallkirjadele: digitaalallkirja administraatorid, allkirjastajad ja digitaalallkirja audiitorid.</span><span class="sxs-lookup"><span data-stu-id="dae71-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="dae71-126">Digitaalallkirja administraator</span><span class="sxs-lookup"><span data-stu-id="dae71-126">Electronic signature administrator</span></span>

<span data-ttu-id="dae71-127">Elektroonilise allkirja administraator seadistab allkirjanõuded, üldised parameetrid ja kinnitajad ning saab allkirja kinnitamise nurjumisel märguandeid.</span><span class="sxs-lookup"><span data-stu-id="dae71-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="dae71-128">Kasutajal, kes kuulub turberolli **Infotehnoloogiajuht**, on vaikimisi õigus elektronallkirju administreerida.</span><span class="sxs-lookup"><span data-stu-id="dae71-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="dae71-129">Allkirjastaja</span><span class="sxs-lookup"><span data-stu-id="dae71-129">Signer</span></span>

<span data-ttu-id="dae71-130">Allkirjastaja annab digitaalallkirjad nendele dokumentidele ja protsessidele, mis nõuavad allkirju.</span><span class="sxs-lookup"><span data-stu-id="dae71-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="dae71-131">Kasutajal, kes kuulub turberolli **Süsteemi kasutaja**, on vaikimisi õigus dokumente elektrooniliselt allkirjastada.</span><span class="sxs-lookup"><span data-stu-id="dae71-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span> 

<span data-ttu-id="dae71-132">**Märkus.** Allkirjastaja võib vajada lisaõigusi, enne kui allkirjastatava dokumendi või protsessiga seotud andmetele antakse juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="dae71-132">**Note:** The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="dae71-133">Kasutaja, kes muudab andmeid ja peab seejärel need muudatused allkirjastama, peab omama andmete muutmise õigust.</span><span class="sxs-lookup"><span data-stu-id="dae71-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="dae71-134">Kasutaja, kes allkirjastab teise kasutaja nimel, ei pruugi vajada andmetele juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="dae71-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="dae71-135">Näiteks selline kasutaja on juhendaja, kes allkirjastab töötaja muudatusi.</span><span class="sxs-lookup"><span data-stu-id="dae71-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="dae71-136">Digitaalallkirja audiitor</span><span class="sxs-lookup"><span data-stu-id="dae71-136">Electronic signature auditor</span></span>

<span data-ttu-id="dae71-137">Elektronallkirja audiitor vaatab üle andmebaasilogi ja andmebaasis oleva allkirja ülevaatelogi.</span><span class="sxs-lookup"><span data-stu-id="dae71-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="dae71-138">Kasutajal, kes kuulub turberolli **Infotehnoloogiajuht**, on vaikimisi õigus elektronallkirju kontrollida.</span><span class="sxs-lookup"><span data-stu-id="dae71-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span> 

<span data-ttu-id="dae71-139">Kui kasutate muud rolli kui **Infotehnoloogiajuht**, siis veenduge, et rollile oleksid määratud järgmised õigused.</span><span class="sxs-lookup"><span data-stu-id="dae71-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

-   <span data-ttu-id="dae71-140">Elektroonilise allkirja tõrgete kuvamine</span><span class="sxs-lookup"><span data-stu-id="dae71-140">View electronic signature failures</span></span>
-   <span data-ttu-id="dae71-141">Andmebaasilogi kuvamine</span><span class="sxs-lookup"><span data-stu-id="dae71-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="dae71-142">Dokumentide elektrooniline allkirjastamine</span><span class="sxs-lookup"><span data-stu-id="dae71-142">Signing documents electronically</span></span>
### <a name="get-a-certificate"></a><span data-ttu-id="dae71-143">Sertifikaadi hankimine</span><span class="sxs-lookup"><span data-stu-id="dae71-143">Get a certificate</span></span>

<span data-ttu-id="dae71-144">Enne dokumentide elektroonilist allkirjastamist Finance and Operationsis peab taotlema serti.</span><span class="sxs-lookup"><span data-stu-id="dae71-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span> 

<span data-ttu-id="dae71-145">**Märkus.** Finance and Operations kasutab sertide loomiseks ja elektroonilise allkirjastamise võimaldamiseks Microsoft SQL Serveri funktsioone.</span><span class="sxs-lookup"><span data-stu-id="dae71-145">**Note:** Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="dae71-146">Muid sertifikaate ega avaliku võtme infrastruktuure (PKI) pole vaja.</span><span class="sxs-lookup"><span data-stu-id="dae71-146">No additional certificate or public key infrastructure (PKI) is required.</span></span> 

<span data-ttu-id="dae71-147">Sertifikaadi taotlemisel luuakse teie jaoks rakenduse Finance and Operationsi andmebaasi avalik võti ja privaatvõti.</span><span class="sxs-lookup"><span data-stu-id="dae71-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="dae71-148">Privaatvõti krüptitakse ainult teile teadaolevat parooli kasutades.</span><span class="sxs-lookup"><span data-stu-id="dae71-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="dae71-149">Dokumendi elektroonsel allkirjastamisel kinnitatakse teie identiteet parooli sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="dae71-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span> 

<span data-ttu-id="dae71-150">Serdi taotlemiseks klõpsake lehe **Suvandid** vahekaardil **Kontod** käsku **Hangi sert**.</span><span class="sxs-lookup"><span data-stu-id="dae71-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span> 

<span data-ttu-id="dae71-151">Peate sisestama ja kinnitama allkirjastamiseks kasutatava parooli.</span><span class="sxs-lookup"><span data-stu-id="dae71-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="dae71-152">Parooli kasutatakse teie privaatvõtme kaitsmiseks ja sertifikaadi kasutamise volituseks.</span><span class="sxs-lookup"><span data-stu-id="dae71-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="dae71-153">Parooli ei salvestata andmebaasis ja see ei ole teistele (isegi mitte Finance and Operationsi administraatorile) kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="dae71-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span> 

<span data-ttu-id="dae71-154">Serdiga seotud parooli unustamisel peab serdi lähtestama.</span><span class="sxs-lookup"><span data-stu-id="dae71-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="dae71-155">Serdi lähtestamine ei mõjuta dokumente, mille eelmise serdi abil allkirjastasite.</span><span class="sxs-lookup"><span data-stu-id="dae71-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="dae71-156">Serdi lähtestamiseks klõpsake lehel **Suvandid** käsku **Lähtesta sert**.</span><span class="sxs-lookup"><span data-stu-id="dae71-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="dae71-157">Dokumendi digitaalselt allkirjastamine</span><span class="sxs-lookup"><span data-stu-id="dae71-157">Sign a document electronically</span></span>

<span data-ttu-id="dae71-158">Vorm **Dokumendi allkirjastamine** kuvatakse siis, kui teete muudatuse, mis nõuab elektroonilist allkirja.</span><span class="sxs-lookup"><span data-stu-id="dae71-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1.  <span data-ttu-id="dae71-159">Klõpsake lehel **Dokumendi allkirjastamine** vahekaarti **Dokument** dokumendi muudatuste ülevaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="dae71-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2.  <span data-ttu-id="dae71-160">Valige vahekaardilt **Allkiri** põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="dae71-160">On the **Signature** tab, select a reason code.</span></span>
3.  <span data-ttu-id="dae71-161">Sisestage kommentaar, kui see on vajalik.</span><span class="sxs-lookup"><span data-stu-id="dae71-161">Enter a comment, if a comment is required.</span></span>
4.  <span data-ttu-id="dae71-162">Kui teie kasutaja ID-d väljal **Allkirjastaja** ei kuvata, siis valige see loendist.</span><span class="sxs-lookup"><span data-stu-id="dae71-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5.  <span data-ttu-id="dae71-163">Sisestage oma asukoht, kui see teave on vajalik.</span><span class="sxs-lookup"><span data-stu-id="dae71-163">Enter your location, if this information is required.</span></span>
6.  <span data-ttu-id="dae71-164">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="dae71-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="dae71-165">Teise kasutaja muudatuste allkirjastamine</span><span class="sxs-lookup"><span data-stu-id="dae71-165">Sign for another user's changes</span></span>

<span data-ttu-id="dae71-166">Mõnikord on vaja kasutajal teise kasutaja muudatusi allkirjastada.</span><span class="sxs-lookup"><span data-stu-id="dae71-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="dae71-167">Näiteks peab ülemus allkirjastama töötaja tehtud koosluse (BOM) muudatused.</span><span class="sxs-lookup"><span data-stu-id="dae71-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="dae71-168">Kasutage seda protseduuri rakenduse Finance and Operations kasutaja määramiseks allkirjastajaks teise allkirjastaja asemel.</span><span class="sxs-lookup"><span data-stu-id="dae71-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span> 

<span data-ttu-id="dae71-169">**Märkus.** Kui üks kasutaja allkirjastab teise kasutaja muudatuse, peab muudatuse teinud kasutaja andma allkirja tööjaamas.</span><span class="sxs-lookup"><span data-stu-id="dae71-169">**Note:** When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="dae71-170">Kasutaja ei saa muudatust salvestada enne, kui allkiri on antud.</span><span class="sxs-lookup"><span data-stu-id="dae71-170">The user can't save the change until the signature has been provided.</span></span> 

<span data-ttu-id="dae71-171">Kinnitajate määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="dae71-171">To designate approvers, follow these steps.</span></span>

1.  <span data-ttu-id="dae71-172">Klõpsake lehe **Suvandid** vahekaardil **Kontod** valikut **Määra kinnitaja**.</span><span class="sxs-lookup"><span data-stu-id="dae71-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2.  <span data-ttu-id="dae71-173">Valige väljal **Kinnitaja kasutaja ID** selle kasutaja ID, kes peab teise kasutaja tehtud muudatuse allkirjastama.</span><span class="sxs-lookup"><span data-stu-id="dae71-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3.  <span data-ttu-id="dae71-174">Valige väljal **Allkirjastatava kasutaja ID** selle kasutaja ID, kelle muudatustele peab alla kirjutama.</span><span class="sxs-lookup"><span data-stu-id="dae71-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>





