---
title: "Hledání za účelem navigace"
description: "Tento článek vysvětluje, jak pomocí funkce vyhledávání přejděte na stránky 365 Microsoft Dynamics pro operace."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Hledání za účelem navigace

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak pomocí funkce vyhledávání přejděte na stránky 365 Microsoft Dynamics pro operace.

Dynamics 365 pro operace poskytuje funkce pro široké škály průmyslových odvětví a pocházejícími. Aplikace obsahuje několik oblastí a stránek můžete provádět různé úlohy. Rychle najít stránky, kterou potřebujete k dokončení úkolů, použijte vyhledávací funkce navigace. Chcete-li tuto funkci použít, kliknutím na ikonu **Hledat** zobrazíte pole **hledání**. Poté můžete zadat nejméně jedno slovo do pole. Systém vyhledá okamžitě příslušné stránky v aplikaci, které obsahují zadaná slova. Například můžete zadat jako vstup "fakturu dodavatele" a pak systém zobrazí výsledky odpovídající tomuto zadání. **Poznámka:** Pole **hledání** usnadňuje hledání a přechod na stránky. Neslouží k hledání konkrétních dat nebo akcí. 

[![vyhledávací pole](./media/search-box.png)](./media/search-box.png) funkce vyhledávání navigace slouží také jako skvělý způsob můžete rychle přejít na konkrétní stránku. Například, pokud jste závazky úředník který často používá **deníku plateb** stránky, můžete zadat "deník plateb" do vyhledávacího pole. Vzhledem k tomu, že vstup je přesná shoda nadpisu stránky, stránky je uveden v horní části výsledků hledání a můžete rychle přejít k němu. 

[![vyhledávání pro--deník plateb](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Seznam výsledků hledání zobrazí název stránky, jakož i navigační cesty. To vám umožní zjistit umístění stránky v aplikaci. Rovněž pomáhá rozlišovat mezi dvěma nebo více podobnými stránkami ve výsledcích. Při hledání stránky jsou zadané hodnoty porovnávány s nadpisem stránky a jeho cestou navigace. Například pokud zadáte "pohledávky" ** ** vyhledávací pole, zobrazí se výsledky pro stránky, které jsou k dispozici v oblasti Pohledávky – Přestože nadpisy stránek neobsahují slovo "pohledávky". 

[![hledání pro word pohledávky](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Od správy a zabezpečení výhledu hledat navigace se projeví pouze:

-   Stránky, které jsou povoleny v aktuální konfiguraci (pomocí konfiguračních klíčů).
-   Stránky, ke kterým má uživatel přístup na základě role uživatele.

Seznam výsledků hledání je omezen na 10 položek. Pokud ve výsledcích nenaleznete, co jste hledali, doporučujeme upřesnit nebo aktualizovat zadání. Z pohledu vývoje je funkce hledání navigace velmi jednoduchá, protože nevzniká téměř žádná prodleva mezi nasazením položek nabídky a možnosti jejich zobrazení ve výsledcích hledání. Dokud jsou položky nabídky propojeny z navigačního podokna nebo řídicího panelu, je možné je automaticky prohledávat. Funkce hledání navigace také zahrnuje velmi žádanou funkci pro pokročilé uživatele: schopnost rychle přejít na stránku na základě technického názvu formuláře. Mnoho uživatelů je tak obeznámeno se systémem, že znají přesné názvy formulářů, se kterými pracují. Pokud jste jedním z těchto uživatelů, můžete zadat **formulář:** a poté název formuláře, které hledáte. Zadáte-li například **formulář: vendinvoice**, výsledky hledání zobrazí všechny stránky, na kterých název formuláře začíná na **vendinvoice**. 

[![hledání pro formulář vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)




