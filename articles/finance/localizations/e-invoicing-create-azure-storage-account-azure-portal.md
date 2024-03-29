---
title: Azure'i salvestusruumi konto loomine Azure'i portaalis
description: See artikkel selgitab, kuidas luua elektrooniliseks arveldamiseks Azure’i salvestuskonto.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291632"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure'i salvestusruumi konto loomine Azure'i portaalis

[!include [banner](../includes/banner.md)]

Kõik elektroonilised failid, mille genereerib elektroonilise arveldamise teenus või mis lähevad teenusesse töötlemise ajal, talletatakse teie ladustamiskonto Microsoft Azure konteinerites. Tagamaks, et elektroonilisel arveldamisel on neile konteineritele juurdepääs, peate andma elektroonilise arveldamise teenusele ladustamise konto ühise juurdepääsu allkirja (SAS). Lisaks, et tagada loa turvamine, ärge esitage SAS-i luba otse. Selle asemel ladustage see Azure’i võtme hoidlasse ja sisestage Azure’i võtme hoidla saladus.

1. Avage ladustamise konto, mida plaanite kasutada elektroonilise arvelduse teenusega.
2. Minge **sätete** \> **konfiguratsiooni** ja veenduge, et bloobi lubamise **avaliku juurdepääsu** parameeter on seatud väärtusele **Lubatud.**
3. Minge **andmesalvestuskonteineritesse** \> **ja** looge konteiner.
4. Sisestage konteineri nimi ja seadke välja **Avaliku juurdepääsu tase** väärtuseks **Privaatne(anonüümse juurdepääsuta)**.
5. Avage uus konteiner ja minge sätete **juurdepääsu** \> **poliitikasse.**
6. Valige **Lisa poliitika**, et lisada talletamise juurdepääsupoliitika.
7. Seadistage **sobiv väli** Identifikaator.
8. **Valige väljal Õigused** kõik õigused.

    ![Kõik õigused, mis on dialoogiakna Lisa poliitika väljal Õigused valitud.](media/e-invoicing-azure-1.png)

9. Sisestage algus- ja aegumiskuupäev. Aegumiskuupäev peab olema tulevikus.
10. Valige **OK** poliitika salvestamiseks ja seejärel salvestage muudatused konteineris.
11. Minge sätete **jagatud** \> **juurdepääsutõendeid ja** seadke välja väärtused.
12. Sisestage algus- ja aegumiskuupäev. Aegumiskuupäev peab olema tulevikus.
13. **Valige väljal Õigused** järgmised õigused:

    - Loe
    - Lisamine
    - Loomine
    - Kirjuta
    - Kustutusklahv
    - Loend

14. Valige **Loo SAS-luba ja URL**.
15. Kopeerige ja salvestage väärtus **Bloobi SAS-i URL-i** väljale. Seda väärtust kasutatakse selles protseduuris hiljem ja seda nimetatakse ühiskasutuses juurdepääsu *allkirja URI-ks*.
16. Avage võtmehoidla, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.
17. Minge sätete **saladuste** \> **kausta** ja valige käsk **Loo/Impordi**, et luua saladus.
18. Valige lehel **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.
19. Sisestage saladuse nimi. Seda nime kasutatakse teenuse seadistamisel regulatiivses konfiguratsiooniteenuses (RCS) *ja seda nimetatakse võtme vault-salanimeks*. Lisateavet RCS-i seadistamise kohta vt [seadistamine Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md)
20. Sisestage **väljale Väärtus** varem kopeeritud ühiskasutusega juurdepääsu allkirja URI.
21. Valige **Loo**.
