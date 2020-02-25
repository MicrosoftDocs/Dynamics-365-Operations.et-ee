---
title: Tasu töötlemine
description: Tasu töötlemise abil saate arvutada omakapitali kohanduste, teenetel põhineva palgatõusu sihtväärtuste ja tulemuste põhjal töötajate uusi põhipalga summasid.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 05f7be778857380d40a73d068e2b0b4fc7d1d1f6
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008753"
---
# <a name="process-compensation"></a><span data-ttu-id="0ab2b-103">Tasu töötlemine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-103">Process compensation</span></span>

<span data-ttu-id="0ab2b-104">Tasu töötlemise abil saate arvutada omakapitali kohanduste, teenetel põhineva palgatõusu sihtväärtuste ja tulemuste põhjal töötajate uusi põhipalga summasid.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-104">Compensation processing allows you to calculate new base compensation amounts for your employees based on equity adjustments, merit increase targets, and performance.</span></span> <span data-ttu-id="0ab2b-105">See artikkel käsitleb tasude töötlemise põhivoogu põhipalga plaanide puhul ilma töötaja tulemusi arvesse võtmata.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-105">This article covers the basic flow of compensation processing for fixed compensation plans without factoring an employee's performance.</span></span>

## <a name="plan-the-new-compensation-amounts-and-budgets"></a><span data-ttu-id="0ab2b-106">Uute tasusummade ja eelarvete plaanimine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-106">Plan the new compensation amounts and budgets</span></span>
<span data-ttu-id="0ab2b-107">Töötajatele teenetel põhineva palgatõusu andmiseks peate seadistama igale osakonnale fikseeritud tõusu eelarve: Tasuhaldus > Lingid > Teenetel põhineva palgatõusu sihtmärgid.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-107">To give your employees a merit increase, you must set up a fixed increase budget for each of your Departments:  Compensation management > Links > Merit increase targets.</span></span> <span data-ttu-id="0ab2b-108">(Teine võimalus on avada see osakonna kaudu: Organisatsioon > Osakonnad.) Siin saate täiendavalt määrata, kas teatud ametiühingu või asukoha töötajad peaksid saama teistsuguse kasvuprotsendi.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-108">(Alternatively, you can open this form through the Department: Organization > Departments.) Here you can further specify whether employees in a certain labor union or location should get a different increase percent.</span></span> <span data-ttu-id="0ab2b-109">Väljad **Eelarve** ja **Valuuta** on informatiivsed ja neid saab kasutada eelarve jaoks valuutasumma märkimiseks.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-109">The **Budget** and **Currency** fields are informational and can be used to note a currency amount for the budget.</span></span>

## <a name="set-up-the-compensation-process"></a><span data-ttu-id="0ab2b-110">Tasuprotsessi seadistamine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-110">Set up the compensation process</span></span>
<span data-ttu-id="0ab2b-111">Protsessisündmus võimaldab määrata tasu töötlemise jaoks parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-111">A process event lets you specify the parameters for the compensation processing.</span></span> <span data-ttu-id="0ab2b-112">See hõlmab kuupäevaperioodi hüvitussummade kindlaksmääramiseks ja kuupäeva, millest uued hüvitussummad peavad jõustuma.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-112">This includes the date period to evaluate for determining the compensation amounts, and the date that the new compensation amounts should go into effect.</span></span>

<span data-ttu-id="0ab2b-113">Soovi korral võite lisada põhipalga proportsionaalse töölevõtmise kuupäeva, kui mõnes põhipalgaplaanis kasutatakse protsendi palkamisreeglit.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-113">Optionally you can include a fixed pay pro rated hire date if any of you fixed compensation plans use a hire rule of Percent.</span></span> <span data-ttu-id="0ab2b-114">Nende plaanide puhul saab inimene, kes palgati pärast tsükli alguskuupäeva ja enne põhipalga proportsionaalset palkamise kuupäeva, 100% oma arvutatud teenetel põhinevast tasust või üldisest palgatõusust.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-114">For those plans, anyone who was hired after the cycle start date and before the fixed pay pro rated hire date will receive 100% of their calculated merit or general increase.</span></span> <span data-ttu-id="0ab2b-115">Inimene, kes palgati pärast põhipalga proportsionaalset palkamise kuupäeva ja enne tsükli lõppkuupäeva, saab osa oma arvutatud palgatõusust selle põhjal, mitu päeva ta tsükli päevade koguarvust töötas.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-115">Anyone who was hired after the fixed pay pro rated hire date and before the cycle end date will receive a portion of their calculated increase based on how many days out of the total cycle days they were employed.</span></span> <span data-ttu-id="0ab2b-116">Näiteks kui tsükkel kestab 1. jaanuarist 31. detsembrini ja meil on põhipalga proportsionaalne palkamiskuupäev 1. aprill, saab töötaja, kes palgati märtsis, terve arvutatud palgatõusu, samas kui 1. juulil palgatud töötaja saab ligikaudu poole arvutatud palgatõusust.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-116">For example, if our cycle runs from January 1 through December 31 and we have a fixed pay prorated hire date of April 1, an employee who is hired in March will receive the full calculated increase while an employee hired on July 1 will receive approximately half of the calculated increase.</span></span>

<span data-ttu-id="0ab2b-117">Protsessisündmuse **Ajahetk** kuupäeva kasutatakse ainult teatud ergutussüsteemi plaanide töötlemiseks ja neid siin ei käsitleta.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-117">The process event **Point-in-time** date is used for processing only certain variable compensation plans and isn't covered here.</span></span> <span data-ttu-id="0ab2b-118">**Ülevaatamise tähtaeg** on kõigi soovituste esitamise tähtaeg, et uued tasusummad saaks töötaja kirjesse laadida.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-118">The **Review deadline** is the deadline to make all the recommendations so that the new compensation amounts can be loaded into the employee’s record.</span></span> <span data-ttu-id="0ab2b-119">Ülevaatamise kuupäev on ainult informatiivne.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-119">The review date is informational only.</span></span>

<span data-ttu-id="0ab2b-120">Kui protsessisündmuse parameetrid on salvestatud, võite klõpsata nuppu **Seadistus**, et näidata, millised plaanid tuleks sellesse protsessitsüklisse lisada ja milliseid põhipalga toiminguid iga plaani puhul teha.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-120">After the parameters of the process event have been saved, you can click the **Setup** button to indicate the plans to include when this process is run, and which fixed compensation actions to take for each plan.</span></span>

<span data-ttu-id="0ab2b-121">Klõpsake vahekaardil **Plaanid** nuppu **Lisa** tasuplaani lisamiseks protsessisündmusele.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-121">Click the **Add** button in the **Plans** tab to add a compensation plan to the process event.</span></span> <span data-ttu-id="0ab2b-122">Veergusid **Kasuta muud finantsvõimendust**, **Finantsvõimenduse tegur** ja **Finantsvõimenduse kirjeldus** kasutatakse ainult ergutussüsteemi plaanide jaoks ja neid selles artiklis ei käsitleta.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-122">The **Use other leverage**, **Leverage factor**, and **Leverage description** columns are used for variable compensation plans only and are not be covered in this article.</span></span>

<span data-ttu-id="0ab2b-123">Salvestage kirje ja klõpsake siis vahekaardil **Tegevused** nuppu **Lisa** põhipalga toimingute lisamiseks valitud plaani puhul.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-123">Save the record, then click the **Add** button in the **Actions** tab to add fixed compensation actions for the selected plan.</span></span> <span data-ttu-id="0ab2b-124">Kasutage valikut **Luba soovitus**, et sisestada muu summa peale tegevuse jaoks arvutatud kasvusumma.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-124">Use the **Enable recommendation** option to enter an amount that's different than the calculated guideline increase for the action.</span></span> <span data-ttu-id="0ab2b-125">Tegevuse arvutamiseks eelmise tegevuse tulemuse põhjal, et siduda mitu tasutegevust, märkige valik **Kasuta eelmist tulemust**. Põhipalga tegevused on tasuloogika tegevused, millele saate anda kirjeldavad nimed.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-125">To calculate  an action that's based on the result of the previous action to link multiple compensation actions, mark the **Use previous result** option, Fixed compensation actions are types of compensation logic that you can give descriptive names to.</span></span> <span data-ttu-id="0ab2b-126">Taseme ja palgaastmiku plaanide puhul saate lisada ainult järgmist tüüpi põhipalgategevusi.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-126">For Grade and Band plans, you can only add fixed compensation actions that are of the following Types:</span></span>

| <span data-ttu-id="0ab2b-127">Põhipalga tegevuse tüüp</span><span class="sxs-lookup"><span data-stu-id="0ab2b-127">Fixed compensationaction type</span></span> | <span data-ttu-id="0ab2b-128">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="0ab2b-128">Functionality</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab2b-129">Omakapital</span><span class="sxs-lookup"><span data-stu-id="0ab2b-129">Equity</span></span>                        | <span data-ttu-id="0ab2b-130">Omakapitali tegevused võrdlevad töötaja palgamäära tsükli lõpu seisuga madalaima võrdluspunktiga töötaja ametikohal näidatud taseme puhul.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-130">Equity actions will compare the employee’s rate of pay as of the cycle end date with the lowest reference point for the level indicated on the employee’s job.</span></span> <span data-ttu-id="0ab2b-131">Kui töötaja palgamäär on minimaalsest võrdluspunktist madalam, arvutatakse vajalik kasv töötaja viimiseks vahemiku miinimumpunkti.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-131">If the employee’s pay rate is less than the minimum reference point, the increase needed to bring the employee to the minimum point in the range will be calculated.</span></span>                                                                                |
| <span data-ttu-id="0ab2b-132">teene</span><span class="sxs-lookup"><span data-stu-id="0ab2b-132">Merit</span></span>                         | <span data-ttu-id="0ab2b-133">Teenetel põhinevad tegevused arvutavad kasvu töötaja palgamäära põhjal tsükli lõppkuupäeva seisuga ja töötaja osakonna, ametiühingu ning asukoha fikseeritud palgatõusu eelarves antud kasvuprotsendi alusel.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-133">Merit actions will calculate an increase based on the employee’s pay rate as of the cycle end date and the increase percent found in the fixed increase budget for the employee’s department, labor union, and location.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="0ab2b-134">Üldine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-134">General</span></span>                       | <span data-ttu-id="0ab2b-135">Üldised toimingud arvutavad palgatõusu protsendi põhjal või annavad töötajatele fikseeritud summa.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-135">General actions will calculate an increase based on either a Percent or give the employees a flat amount.</span></span> <span data-ttu-id="0ab2b-136">See määratakse vahekaardil **Üldine** olevate suvandi **Põhipalk** sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-136">This is determined based on the **Fixed compensation** settings on the **General** tab.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="0ab2b-137">Edutamine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-137">Promotion</span></span>                     | <span data-ttu-id="0ab2b-138">Edutamistegevused annavad nimelise koha, kus saate palgatõusu anda, seega märkige kindlasti valik **Luba soovitus**, et saaksite lisada edutatavate töötajate soovitusi.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-138">Promotion actions provide you with a named place where you can award increase so be sure to mark the **Enable recommendation** option so you can enter a recommendation for the employees who will receive promotions.</span></span>  <span data-ttu-id="0ab2b-139">Ilma soovitatud palgatõusuta töötajate põhipalga kirjetesse ei lisata tegevust **Edutamine**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-139">Employees without a recommended increase will not have the **Promotion** action added to their fixed compensation records.</span></span>                                                                       |
| <span data-ttu-id="0ab2b-140">Mõni teine taseme muutus</span><span class="sxs-lookup"><span data-stu-id="0ab2b-140">Other level change</span></span>            | <span data-ttu-id="0ab2b-141">Eelnevas näites on meie tegevusel **Põhipalk** tüübiga **Muu taseme muutus** nimi **Ametialandus**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-141">In the preceding example, **Demotion** is the name of our **Fixed compensation** action with a type of **Other level change**.</span></span> <span data-ttu-id="0ab2b-142">See loob 0 (nullmuutusega) juurdekasvu, et saaksite sisestada soovitusliku summa töötaja palgamäära korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-142">This generates a 0 (zero-change) guideline increase so you can enter a recommendation amount to adjust the employee’s pay rate.</span></span> <span data-ttu-id="0ab2b-143">(Märkige kindlasti valik **Luba soovitus**.) Ilma soovituseta töötajate puhul ei lisata seda tegevust nende põhipalga kirjetele.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-143">(Be sure to mark the **Enable recommendation** option.) Employees without a recommendation will not have this action added to their fixed compensation records.</span></span> |

<span data-ttu-id="0ab2b-144">Astmeplaani saab lisada ainult neid tegevusi **Põhipalk**, mille tüüp on Aste.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-144">You can only add **Fixed compensation** actions with a type of Step to a Step plan.</span></span>

| <span data-ttu-id="0ab2b-145">Põhipalga tegevuse tüüp</span><span class="sxs-lookup"><span data-stu-id="0ab2b-145">Fixed compensation action type</span></span> | <span data-ttu-id="0ab2b-146">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="0ab2b-146">Functionality</span></span>                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab2b-147">Etapp</span><span class="sxs-lookup"><span data-stu-id="0ab2b-147">Step</span></span>                           | <span data-ttu-id="0ab2b-148">Märkige vahekaardil Üldine, kas see astmetegevus peaks viima töötajad edasi 0 astme, 1 astme või kahe astme võrra.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-148">On the General tab, indicate whether this Step action should move the employees forward 0 steps, 1 step, or two steps.</span></span>                                                                                  |
|                                | <span data-ttu-id="0ab2b-149">**0 astet** – töötaja saab selle astme palgamäära, millel ta praeg on.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-149">**0 steps** - The employee will receive the pay rate for the current step they are on.</span></span>                                                                                                                      |
|                                | <span data-ttu-id="0ab2b-150">**1 aste** – süsteem kontrollib, kas töötaja on juba oma taseme viimases võrdluspunktis.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-150">**1 step** - The system will check whether the employee is already at the last reference point for their level.</span></span>                                                                                             |
|                                | <span data-ttu-id="0ab2b-151">**2 astet** – süsteem viib töötaja praegusel tasemel kaks astet edasi.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-151">**2 steps** - The system will move the employee forward two steps on their current level.</span></span> <span data-ttu-id="0ab2b-152">Süsteem võib liigutada töötajat ühe või nulli astme võrra, kui töötaja on jõudnud oma taseme viimasesse võrdluspunkti.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-152">The system might only move the employee one or zero steps if they reach the last reference point for their level.</span></span> |

## <a name="run-the-compensation-process"></a><span data-ttu-id="0ab2b-153">Tasuprotsessi käitamine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-153">Run the compensation process</span></span>
<span data-ttu-id="0ab2b-154">Pärast protsessisündmuse seadistamist vajalike kuupäevaväljade, plaanide ja tegevustega võite klõpsata lehel **Protsessisündmus** valikut **Käivita protsess**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-154">After the process event has been set up with the necessary date fields, plans and actions you can click **Run process** on the **Process event** page.</span></span> <span data-ttu-id="0ab2b-155">Selle tagajärjel avaneb dialoog **Käivita tasu protsessisündmused**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-155">Doing so opens the **Run compensation process events** dialog.</span></span> <span data-ttu-id="0ab2b-156">Selles dialoogis võite klõpsata valikut **Töötlemise tulemuste näitamine**, et näha, kuidas iga töötaja puhul tasusummad arvutati.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-156">Within this dialog, you can click the **Show processing results** option to seen how the compensation amounts were calculated for each employee.</span></span> <span data-ttu-id="0ab2b-157">Nupu **OK** klõpsamisel käivitatakse tasuprotsess kõigi töötajate kohta, kes on tsükli lõppkuupäeva seisuga valitud tasuplaanides.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-157">Clicking **OK** will run the compensation process for all employees who in the selected compensation plans as of the cycle end date.</span></span>

## <a name="view-the-process-results"></a><span data-ttu-id="0ab2b-158">Protsessi tulemuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-158">View the process results</span></span>
<span data-ttu-id="0ab2b-159">Protsessi tulemuste kuvamiseks avage leht **Protsessi tulemused**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-159">To view the process results, open the **Process results** page.</span></span> <span data-ttu-id="0ab2b-160">Iga kord, kui protsessisündmus käivitatakse, luuakse uus tasusündmus.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-160">A new compensation event will be created each time the process event is run.</span></span> <span data-ttu-id="0ab2b-161">Sel viisil saate teha proovitsükleid, korrigeerida ja käivitada tasusündmuse mitu korda, et näha, kuidas mitmesugused muudatused töötaja tasu mõjutavad.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-161">In this way, you can do trial runs, make adjustments, and run the compensation event multiple times to see how various changes impact employee compensation.</span></span>

<span data-ttu-id="0ab2b-162">Lehel **Protsessi tulemused** on teave protsessi tsükli kohta, sh tsükli toimumise aeg, kasutaja, kes protsessi käivitas, ja kas protsessi käitamisel ilmnes tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-162">The **Process results** page contains information about the process run including when the run occurred, the user who ran the process, and whether any errors occurred when the process was run.</span></span> <span data-ttu-id="0ab2b-163">Võite märkida ka valiku **Lukustatud** nupu **Laadi tasu** keelamiseks ja vältige nii tasusündmuste laadimist töötaja kirjetesse.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-163">You can also mark the **Locked** option to disable the **Load compensation** button and prevent anyone from loading the compensation events to the employee records.</span></span> <span data-ttu-id="0ab2b-164">Nupu **Töötajate tulemused** klõpsamisel kuvatakse tsüklis sisalduvate töötajate loend.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-164">Clicking the **Employees results** button will display the list of employees included in the run.</span></span>

<span data-ttu-id="0ab2b-165">Suvandis **Töötaja tulemused** on näidatud teave protsessi enda kohta, samuti kõik protsessis tehtud tasutegevused.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-165">The **Employee results** option shows information about the process itself, as well as any compensation actions performed in the process.</span></span> <span data-ttu-id="0ab2b-166">Jaotis **Põhipalk** sisaldab kirjet iga tegevuse kohta, mis on tasuplaani protsessisündmusse kaasatud.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-166">The **Fixed compensation** section will contain a record for each action included in the process event for the compensation plan.</span></span> <span data-ttu-id="0ab2b-167">Veergudes **Praegune juhend** ja **Soovitus** on kuvatud lisateave jaotises **Põhipalk** valitud tegevuse kohta.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-167">The **Current Guideline** and **Recommendation** columns will display more information for the action selected in the **Fixed compensation** section.</span></span> <span data-ttu-id="0ab2b-168">Kui tegevuse puhul on märgitud valik **Luba soovitused**, siis saab soovituse välju redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-168">If **Enable recommendations** was marked for the action, the Recommendation fields will be editable.</span></span> <span data-ttu-id="0ab2b-169">See võmialdab töötaja summasid käsitsi korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-169">This will let you manually adjust the amounts for the employee.</span></span> <span data-ttu-id="0ab2b-170">Pange tähele, et kui märkisite protsessisündmuses tegevuse puhul valiku **Kasuta eelmist tulemust**, peate sõltuvate tegevuste summasid käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-170">Note that if you marked **Use previous result** for the action on the process event, you must manually update the amounts for any dependent actions.</span></span>

<span data-ttu-id="0ab2b-171">Kui töötaja tasusummad on üle vaadatud ja soovitud väärtused korrigeeritud, võite muuta väärtust **Olek** real **Töötaja sündmus** selleks et näidata, kas sündmus on kinnitatud või seda tuleks eirata.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-171">When the compensation amounts have been reviewed for an employee and any adjustments to the recommended values have been made, you can change the **Status** on the **Employee event** line to indicate whether the event has been approved or should be ignored.</span></span> <span data-ttu-id="0ab2b-172">Soovi korral võite töötaja soovituses tehtud muudatused kustutada, klõpsates nuppu **Arvuta ümber**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-172">Optionally, you can erase any changes made to the employee’s recommendation by clicking the **Recalculate** button.</span></span> <span data-ttu-id="0ab2b-173">Sellisel juhul märgitakse olemasolev töötaja sündmus olekuga Eira ja luuakse uus ümberarvutatud väärtustega töötaja sündmus.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-173">This will mark the existing employee event with a status of Ignore and create a new employee event with recalculated values.</span></span>

## <a name="loading-approved-compensation-changes"></a><span data-ttu-id="0ab2b-174">Kinnitatud tasumuudatuste laadimine</span><span class="sxs-lookup"><span data-stu-id="0ab2b-174">Loading approved compensation changes</span></span>
<span data-ttu-id="0ab2b-175">Kui vähemalt ühe töötaja olek on muutunud olekuks Kinnitatud, saab need laadida töötaja põhipalga kirjetesse.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-175">When one or more employee events have had their status updated to Approved, they can be loaded to the employees’ fixed compensation records.</span></span> <span data-ttu-id="0ab2b-176">Seda saab teha, valides ühekaupa kõik töötaja sündmused ja klõpsates lehel **Töötaja tulemused** nuppu **Laadi töötaja tasu** või klõpsates nuppu **Laadi tasu** lehel **Protsessi tulemused** kõigi kinnitatud töötaja sündmuste korraga laadimiseks.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-176">This can be done either by selecting each employee event one at a time and clicking the **Load employee compensation** button on the **Employee results** page, or by clicking **Load compensation** on the **Process results** page to load all approved employee events at once.</span></span>

<span data-ttu-id="0ab2b-177">Kui klõpsata nuppu **OK** dialoogis **Laadi tasu**, lisatakse nullist erinevad tasutegevuse read lehele **Töötaja põhipalk**.</span><span class="sxs-lookup"><span data-stu-id="0ab2b-177">Clicking **OK** in the **Load compensation** dialog will add the non-zero compensation action lines to the **Employee fixed compensation** page.</span></span>