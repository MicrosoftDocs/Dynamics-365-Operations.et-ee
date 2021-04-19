---
title: Kliendiportaali kasutajate loomine ja haldamine
description: Selles teemas selgitatakse, kuidas luua kliendiportaali kasutajakontosid ja seadistada neile lubasid.
author: dasani-madipalli
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4d6d88f69f9b958c9e8f49695d07d0b593da2258
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840697"
---
# <a name="create-and-manage-customer-portal-users"></a>Kliendiportaali kasutajate loomine ja haldamine

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Valmiskujul rakenduse puhul ei saa kasutajad ise kliendiportaali abil loodud veebisaitidesse registreerida. Sisselogimiseks ja veebisaidi kasutamiseks peab administraator kasutajatele kutse saatma. Microsoft on teadlikult blokeerinud kasutajate iseregistreerimise võimaluse.

Enne, kui kasutaja saab veebisaiti kasutada, tuleb luua sellele kasutajale kontakti kirje. See kirje näitab, millisele kliendikontole ja juriidilisele isikule kasutaja kuulub. See teave on oluline tagamaks, et kasutaja saab luua ja kuvada müügitellimusi.

Kasutajate iseregistreerumise korral luuakse neile automaatselt kontakti kirjed. Seega ei saa te tagada, et kasutaja valib õige kliendikonto ja juriidilise isiku. Kutseprotsess võimaldab aga administraatoril määrata kontakti kirjele õige kliendikonto ja juriidiline isik enne kutse saatmist. Kui mõtlete lahenduse kohandamisele, et kasutajad saaksid ise registreeruda, siis tasub kindlasti eelnevalt kaaluda võimalikke tagajärgi.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

Video [Klientide kutsumine registreeruma ja kliendiportaali kasutama](https://youtu.be/drGUYHX9QIQ) (kuvatud eespool) on kaasatud [Finance and Operationsi esitusloendisse](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube'is.

## <a name="prerequisite-setup"></a>Eeltingimuste seadistamine

Power Appsi portaalides salvestatakse kontaktid Microsoft Dataverse’is tabelina üksuses **Kontaktid**. Seejärel sünkroonib topeltkirjutus need kirjed vajaduse järgi teenuses Microsoft Dynamics 365 Supply Chain Management.

![Süsteemi diagramm kliendiportaali kontaktide jaoks](media/customer-portal-contacts.png "Süsteemi diagramm kliendiportaali kontaktide jaoks")

Enne uute klientide kutsumist veenduge, et oleksite lubanud topeltkirjutuses tabeli **Kontakt** vastendamise.

## <a name="the-invitation-process"></a>Kutseprotsess

Olemasoleva kontakti kliendiportaali kutsumiseks järgige Power Appsi portaalide dokumentatsioonis toodud teemat [Oma portaalidesse kontaktide kutsumine](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts).

Enne kliendi kliendiportaaliga liituma kutsumist veenduge, et kliendi [kontakti kirje](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) oleks saadaval ja seadistatud järgmisel moel.

1. Seadke välja **Ettevõte** väärtuseks juriidiline isik, kellele klient peab rakenduses Supply Chain Management kuuluma.
2. Seadke välja **Kontonumber** väärtuseks kliendi kontonumber, mis teie arvates peab kliendil rakenduses Supply Chain Management olema.

Pärast kontakti loomist peaksite nägema seda rakenduses Supply Chain Management.

Lisateavet leiate teemast [Kontakti konfigureerimine portaalis kasutamiseks](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) Power Appsi portaalide dokumentatsioonis.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Valmiskujul veebirollid ja tabeli load

Power Appsi portaalides määratletakse kasutajarollid [veebirollide](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) ja [tabeli lubade](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) alusel. Mõned kliendiportaali rollid on määratletud valmiskujul. Te saate luua uusi rolle ja muuta või eemaldada olemasolevaid rolle.

### <a name="out-of-box-web-roles"></a>Valmiskujul veebirollid

Selles jaotises kirjeldatakse kliendiportaaliga kaasatulevaid veebirolle.

Lisateavet valmiskujul kasutajarollide muutmise kohta vt teemadest [Portaalidele veebirollide loomine](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) ja [Portaalidele kirjepõhise turbe lisamine tabeli lubade abil](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) Power Appsi portaalide dokumentatsioonis.

#### <a name="administrator"></a>Administraator

Administraator korraldab veebisaidi järelevalvet ja haldab seda. See isik loob ja seadistab kliendiportaali. Administraator haldab portaali IT ja turbega seotud aspekte ning veendub, et kõik toimib sujuvalt. Samuti võib administraator portaali kohandada ja/või muuta, lisades uusi funktsioone, luues uusi rolle ja tehes muud.

#### <a name="customer-representative"></a>Kliendi esindaja

Kliendi esindaja töötab kliendi ettevõtte jaoks ja vastutab ettevõtte tellimuste haldamise eest. Kliendi esindaja näeb kõiki ettevõtte nimel esitatud tellimusi ja neid esitanud kasutajaid. Lisaks näeb kliendi esindaja teavet üleüldise konto ning selle kohta, millised kontaktid saavad selle konto nimel tellimusi esitada.

#### <a name="authorized-users"></a>Autoriseeritud kasutajad

Volitatud kasutajad saavad esitada tellimusi ja vaadata enda esitatud tellimuste olekut. Samas ei näe nad teiste enda ettevõtte kasutajate esitatud tellimuste olekut.

#### <a name="unauthorized-users"></a>Volitamata kasutajad

Volitamata kasutajad ei saa andmeid vaadata. Nad näevad ainult avalikku teavet, nagu näiteks tingimused ja kliendiportaali juhtiva ettevõtte üksikasjad.

#### <a name="example"></a>Näide

Järgmises tabelis on näidatud, milliseid müügitellimusi iga veebirolli kasutaja süsteemis näeb.

| Müügitellimus | Administraator | Kliendi &nbsp;X esindaja | Volitatud kasutaja: Jane | Volitatud kasutaja: Sam | Volitamata kasutaja: May |
|---|---|---|---|---|---|
| Klient&nbsp;X Tellija:&nbsp;Jane | Jah | Jah | Jah | Ei | Ei |
| Klient&nbsp;X Tellija:&nbsp;Sam | Jah | Jah | Ei | Jah | Ei |
| Klient&nbsp;Y Tellija:&nbsp;May | Jah | Ei | Ei | Ei | Ei |

> [!NOTE]
> Kuigi nii Sam kui ka Jane on kliendi X jaoks töötavad kontaktid, näevad nad ainult iseenda esitatud tellimusi ja ei midagi muud. Kuigi Mayl on süsteemis tellimus, siis ei näe ta seda tellimust kliendiportaalis, kuna ta on volitamata kasutaja. (Lisaks peab ta olema esitanud tellimuse mõne muu kanali, mitte kliendiportaali kaudu.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]