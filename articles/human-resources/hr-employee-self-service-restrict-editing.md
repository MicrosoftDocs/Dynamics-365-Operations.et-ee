---
title: Isikuandmete redigeerimise piiramine
description: Siin saate töötajate jaoks piirata kontaktteabe redigeerimist rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503032"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="da74b-103">Isikuandmete redigeerimise piiramine</span><span class="sxs-lookup"><span data-stu-id="da74b-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="da74b-104">Selles teemas kirjeldatakse, kuidas piirata töötajatel kontaktandmete redigeerimist rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="da74b-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="da74b-105">Vahel tekib vajadus takistada töötajatel redigeerida kindlaid kontaktandmeid, nt nende töökoha asukohta või meiliaadressi.</span><span class="sxs-lookup"><span data-stu-id="da74b-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="da74b-106">Selle funktsiooni kasutamiseks peate esmalt funktsioonihalduses lubama funktsiooni **(Eelversioon) Piirake töötajatel aadressi- ja kontaktteabe lisamist või redigeerimist kindlal otstarbel**.</span><span class="sxs-lookup"><span data-stu-id="da74b-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="da74b-107">Lisateavet funktsioonide eelversioonide lubamise kohta vt [Funktsioonide haldamine](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="da74b-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="da74b-108">![Luba eelvaatefunktsioon](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="da74b-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="da74b-109">Valige teave, mida töötaja saab lisada või redigeerida</span><span class="sxs-lookup"><span data-stu-id="da74b-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="da74b-110">Valige Human Resourcesis **Personalihaldus**, valige **Lingid** ja seejärel valige **Human Resourcesi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="da74b-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Avage Inimressursside parameetrid](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="da74b-112">Valige lehel **Inimressursside parameetrid** vahekaart **Töötaja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="da74b-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Valige Töötaja iseteenindus](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="da74b-114">Tühjendage vahekaardil **Töötaja iseteenindus** kõik jaotises **Aadress ja kontaktandmed** olevad andmed, mida töötaja ei peaks ise lisama ega redigeerima.</span><span class="sxs-lookup"><span data-stu-id="da74b-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="da74b-115">Selles näites oleme tühjendanud kontaktandmete valiku **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="da74b-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Ettevõtte kontaktteabe redigeerimise piiramine](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="da74b-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="da74b-117">Select **Save**.</span></span>

   ![Salvesta muudatused](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="da74b-119">Töötaja vaade</span><span class="sxs-lookup"><span data-stu-id="da74b-119">Employee experience</span></span>

<span data-ttu-id="da74b-120">Pärast seda, kui olete töötajatel keelanud kontaktandmeid lisada või redigeerida, saavad nad seda teavet vaadata, kuid mitte muuta.</span><span class="sxs-lookup"><span data-stu-id="da74b-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="da74b-121">Selles näites on töötajatel keelatud redigeerida **ettevõtte** kontaktteavet, kuid töötaja iseteeninduses saavad nad seda teavet siiski vaadata:</span><span class="sxs-lookup"><span data-stu-id="da74b-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Kuva ettevõtte kontaktteave](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="da74b-123">Kui töötaja valib ettevõtte kontaktteabe, kuvatakse paan **Aadressi redigeerimine** kirjutuskaitstuna ja ta ei saa ühegi välja teavet muuta.</span><span class="sxs-lookup"><span data-stu-id="da74b-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Ettevõtte kontaktteave kuvatakse kirjutuskaitstuna](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="da74b-125">Kui töötaja valib uue aadressi lisamiseks **Lisa**, ei saa ta ripploendist **Eesmärk** valida väärtust **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="da74b-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Töötaja ei saa ettevõtte aadressi lisada](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="da74b-127">Sama olukord avaneb töötajale ka siis, kui ta valib lehel **Isikuandmed** käsu **Kontakti üksikasjad** ja lisab uue aadressi.</span><span class="sxs-lookup"><span data-stu-id="da74b-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="da74b-128">Ripploendis **Eesmärk** kuvatakse ainult seda tüüpi teave, mida töötajal on õigus lisada.</span><span class="sxs-lookup"><span data-stu-id="da74b-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Töötaja ei saa valida eesmärgi ripploendist ettevõtet](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="da74b-130">Vaate **Kontakti üksikasjad** ruudustikus on nüüd kuvatud **Eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="da74b-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Kontakti üksikasjade ruudustikus on kuvatud eesmärk](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="da74b-132">Vt ka</span><span class="sxs-lookup"><span data-stu-id="da74b-132">See also</span></span>

[<span data-ttu-id="da74b-133">Töövõtja ja juhataja iseteeninduskeskuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="da74b-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="da74b-134">Human Resourcesi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="da74b-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="da74b-135">Isiklike andmete muutmine</span><span class="sxs-lookup"><span data-stu-id="da74b-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)